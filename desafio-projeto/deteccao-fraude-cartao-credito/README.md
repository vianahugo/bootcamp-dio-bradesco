# Detecção de Fraude em Transações de Cartão de Crédito

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vianahugo/bootcamp-dio-bradesco/blob/main/desafio-projeto/deteccao-fraude-cartao-credito/deteccao_fraude_cartao_credito.ipynb)

Este projeto desenvolve um modelo preditivo para sinalizar transações potencialmente fraudulentas. Devido ao extremo desbalanceamento do cenário (fraudes representam menos de 0,2% do volume), o foco da solução vai além da escolha do algoritmo, priorizando técnicas robustas de validação, engenharia de features e otimização do limiar de decisão (threshold) orientado a custos de negócio.

## Dados

Utiliza um dataset público de transações de cartão de crédito europeias contendo 284.807 registros distribuídos ao longo de dois dias. 

*   As features numéricas `V1` a `V28` são resultantes de transformação PCA (preservando o anonimato). 
*   As variáveis originais mantidas são `Time` (segundos desde a primeira transação) e `Amount` (valor da transação). 
*   A variável alvo é `Class` (1 = fraude, 0 = legítima).

Base: [Credit Card Fraud Detection (ULB)](https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv)

## Abordagem Técnica

*   **Out-of-Time Validation (Split Temporal):** Divisão de treino e teste baseada na ordem cronológica (`Time`). Isso evita o vazamento de dados do futuro para o treino, refletindo com fidelidade como o modelo performaria em produção.
*   **Penalização vs. Oversampling:** Comparação técnica entre a reponderação de erros (`class_weight='balanced'`) e a geração de dados sintéticos (`SMOTE`). O SMOTE foi restrito isoladamente ao conjunto de treino para garantir uma avaliação limpa.
*   **Threshold Direcionado por Negócio:** O limiar de decisão não utiliza o padrão estático de 0.5. O projeto varre probabilidades e define o ponto de corte minimizando o custo financeiro esperado (peso do prejuízo de um Falso Negativo vs. custo de atrito de um Falso Positivo).
*   **Detecção de Anomalias como Feature:** Uso de um modelo não-supervisionado (`IsolationForest`) para avaliar comportamentos atípicos. O *anomaly score* gerado é incorporado como uma feature adicional para o modelo final.
*   **Feature Engineering (Frequência):** Criação de variáveis baseadas na variável tempo (ex: transações na última hora) usando janela temporal retroativa para não inflar o modelo.
*   **Interpretabilidade:** Uso da biblioteca SHAP para análise de importância global e decomposição de decisões de fraudes específicas (fundamental para times de auditoria).
*   **Métricas de Operação:** Adoção de leituras via Precision@k, simulando a capacidade de revisão diária de um time de prevenção a fraudes.

## Resultados

Desempenho obtido no dataset completo, focado no trade-off entre precisão e capacidade de captura (recall):

| Modelo | Precision (fraude) | Recall (fraude) | F1-Score |
|---|---|---|---|
| Random Forest (class_weight, threshold 0.5) | 0.883 | 0.769 | 0.822 |
| Random Forest + SMOTE (threshold 0.5) | 0.458 | 0.806 | 0.584 |
| Random Forest (threshold por custo = 0.57) | 0.932 | 0.759 | 0.837 |
| XGBoost final (threshold por custo = 0.03) | 0.366 | 0.806 | 0.503 |

*Nota:* O XGBoost com threshold otimizado de 0.03 reduz a precisão intencionalmente para maximizar o recall. Essa escolha é forçada pela função de custo de negócio, onde o prejuízo de permitir fraudes de alto valor supera o custo operacional da investigação.


## Limitações e Próximos Passos

*   **Conjunto de Validação:** O threshold de custo foi avaliado diretamente no conjunto de teste. Em um pipeline definitivo, o ideal é construir um terceiro conjunto (validação) dedicado unicamente à otimização deste limiar.
*   **Granularidade de Features:** As features de frequência foram agregadas sistemicamente. A presença de um ID de cliente/cartão permitiria a construção de features comportamentais muito mais assertivas.
*   **Calibração de Probabilidades:** Utilizar a técnica de `CalibratedClassifierCV` antes de fixar os thresholds de negócio em ambiente produtivo.