# 💻 Caderno de Prompts

## Categoria 1: Sistema Financeiro e Pix (Foco MED)
Estes prompts são cruciais para o contexto bancário, focando na regulamentação do Banco Central para devolução de valores.

*   **Prompt de Fluxo:** "Com base no Guia do MED, descreva passo a passo o fluxo de 'Devolução em caso de fundada suspeita de fraude'. Inclua as ações do usuário, do PSP do pagador e do PSP do recebedor, destacando todos os prazos em horas e dias."
*   **Prompt de Regras e Exceções:** "Quais são os cenários em que o banco do recebedor (PSP do recebedor) pode rejeitar uma notificação de infração ou solicitação de devolução no âmbito do MED? Explique como fica a responsabilização nesses casos."
*   **Prompt de Funcionalidade:** "Como deve funcionar o 'Autoatendimento do MED' nos aplicativos bancários, segundo os Requisitos Mínimos para a Experiência do Usuário?"

## Categoria 2: Engenharia Social e Prevenção a Fraudes
Foco na manipulação psicológica dos usuários, essencial para entender como os golpes começam.

*   **Prompt de Conceituação:** "Quais são os gatilhos psicológicos (como medo, urgência, ganância) explorados pelos golpistas na Engenharia Social? Dê um exemplo prático de golpe associado a cada gatilho, utilizando as cartilhas da FEBRABAN e do CERT.br."
*   **Prompt de Diferenciação:** "Crie uma tabela comparativa explicando as diferenças entre Phishing, Vishing e Smishing. Inclua os vetores de ataque utilizados e as principais dicas de prevenção para cada um."
*   **Prompt Corporativo:** "Liste 5 boas práticas e comportamentos seguros que um funcionário do banco deve ter para proteger as informações corporativas contra ataques de engenharia social."

## Categoria 3: Ameaças Técnicas (Malware e Redes)
Para revisar o lado técnico das invasões e sequestro de dados.

*   **Prompt de Comparação:** "Use a Cartilha de Segurança para a Internet e elabore um resumo comparativo das características dos principais códigos maliciosos: Vírus, Worm, Trojan, Ransomware, Spyware e Backdoor. Foco em 'como se propagam' e 'ações maliciosas'."
*   **Prompt de Criptografia e 2FA:** "Explique, em linguagem simples, o que é Autenticação de Múltiplos Fatores (MFA/2FA) e como a criptografia de dados (em trânsito e em repouso) ajuda a proteger contas e dispositivos em caso de roubo."

## Categoria 4: Governança Corporativa e Cibersegurança
Ideal para o entendimento de processos internos de segurança de TI exigidos em grandes instituições financeiras.

*   **Prompt de SSDLC:** "Descreva as 6 etapas do Ciclo de Vida Seguro de Desenvolvimento de Software (SSDLC) mencionadas no Guia de Boas Práticas. O que é 'Modelagem de Ameaças' na fase de Design e por que ela é importante?"
*   **Prompt de Gestão de Crise:** "Quais são as fases do processo de Gestão de Incidentes (Detecção, Avaliação, Resposta, Comunicação e Lições Aprendidas)? Explique a importância da etapa de 'Lições Aprendidas' para a segurança da organização."
*   **Prompt de Segurança em Nuvem (Cloud):** "Quais são as principais ameaças à segurança de aplicações em nuvem (Cloud Security) e quais são as soluções ou boas práticas recomendadas para mitigar falhas de configuração e vazamento de dados?"
*   **Prompt sobre IA:** "De acordo com o Guia de Boas Práticas, quais são os principais riscos de segurança introduzidos pelo uso de Inteligência Artificial Generativa e quais os princípios fundamentais para mitigá-los no ambiente corporativo?"

## Prompts de "Geração de Material de Estudo" (Utilidade Geral)
Se você quiser usar o NotebookLM para gerar exercícios dinâmicos, use estes modelos:

*   **Gerador de Flashcards:** "Atue como um professor de segurança da informação. Crie 10 perguntas e respostas curtas (estilo flashcards) sobre os conceitos de Criptografia, Phishing e o fluxo do MED do Pix."
*   **Gerador de Casos (Simulado):** "Crie um cenário hipotético em que um cliente do banco sofreu um golpe de Falsa Central de Atendimento (Vishing) e teve seu dinheiro transferido via Pix. Com base nesse cenário, faça 3 perguntas de múltipla escolha sobre como o cliente e o banco deveriam agir segundo as regras do Banco Central."
*   **Resumo para Executivos:** "Atue como um CISO (Chief Information Security Officer). Faça um resumo executivo de no máximo 3 parágrafos sobre a importância de realizar 'Testes de Invasão (Pentests)' e ter um 'Security Operations Center (SOC)' estruturado na empresa."