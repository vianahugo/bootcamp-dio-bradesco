# 🛡️ Governança e Cibersegurança: Caderno Temático Contra Fraudes Digitais

Projeto desenvolvido para o Desafio do **Bootcamp Bradesco - NotebookLM** na DIO.

Este repositório contém a documentação e os resultados do desafio de criação de um caderno temático utilizando o Google NotebookLM. O projeto foi estruturado para servir como um guia prático e de consulta rápida sobre cibersegurança bancária.

## 🎯 Contexto e Objetivos
O foco do estudo foi o mapeamento de fraudes financeiras modernas (com ênfase em engenharia social) e protocolos de segurança digital baseados em fontes oficiais.
*   **Objetivo:** Sistematizar o conhecimento sobre prevenção de golpes no ecossistema financeiro (Pix/MED) e definir um plano de ação pós-incidente.
*   **Ferramenta:** Google NotebookLM (IA de síntese e conexão de fontes).

## 📚 Curadoria de Fontes
Para alimentar o NotebookLM e garantir a precisão dos dados, foram utilizados os seguintes documentos oficiais:
1.  [Guia do Mecanismo Especial de Devolução (MED) - Banco Central](https://www.bcb.gov.br/content/estabilidadefinanceira/pix/Guia_MED.pdf)
2.  [Cartilha de Engenharia Social - FEBRABAN](https://cmsarquivos.febraban.org.br/Arquivos/documentos/PDF/cartilha_eng_social_atualizada_20.pdf)
3.  [Guia de Boas Práticas de Segurança da Informação - FEBRABAN](https://cmsarquivos.febraban.org.br/Arquivos/documentos/PDF/guia%20boas%20praticas%20seguran%C3%A7a.pdf)
4.  [Cartilha de Segurança para Internet - CERT.br](https://cartilha.cert.br/livro/cartilha-seguranca-internet.pdf)

## 🧠 Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Para extrair o melhor da IA, estruturei a interação em três frentes: **Sintético** (red flags de mensagens), **Processual** (passo a passo do MED) e **Educativo** (tradução de termos técnicos).

**🚨 A Cicatriz (Ajuste de Rota):**
*   **Prompt Inicial (Falho):** *"Faça um resumo sobre como funciona a devolução de dinheiro do Pix."*
*   **O Problema:** A IA gerou um texto genérico, misturando devoluções amigáveis com fraudes, e não citou os prazos regulatórios do Banco Central.
*   **Prompt Refinado (Sucesso):** *"Com base no Guia do MED, descreva passo a passo o fluxo de 'Devolução em caso de fundada suspeita de fraude'. Inclua as ações do usuário, do PSP do pagador e do PSP do recebedor, destacando todos os prazos em horas e dias."*
*   **Resultado:** A IA isolou perfeitamente o cenário de fraude, detalhando a regra dos 80 dias para notificação e as 96 horas para devolução.

## 📦 Entregáveis (Miniguia de Estudo)

Os resultados consolidados da interação com a IA foram extraídos e organizados nos arquivos PDF anexados neste repositório:

*   📖 **[Guia de Estudo.md](./entregaveis/Guia_de_Estudo.md):** Resumo estruturado com os principais insights das fontes (Ameaças Técnicas, Prevenção e Pós-Incidente).
*   📚 **[Glossário de Conceitos.md](./entregaveis/Glossário_de_Conceitos.md):** Lista detalhada de termos como Phishing, Ransomware, SIEM e SSDLC.
*   💻 **[Caderno de Prompts.md](./entregaveis/Caderno_de_Prompts.md):** Registro dos comandos avançados utilizados, categorizados para revisões futuras.
