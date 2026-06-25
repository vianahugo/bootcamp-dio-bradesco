# 📖 Guia de Estudo: Cibersegurança, Prevenção a Fraudes e Proteção de Dados

## 1. Introdução
A Internet e as inovações tecnológicas trouxeram inúmeros benefícios, mas também criaram novas vulnerabilidades. O primeiro passo para a segurança é entender que a Internet não tem nada de "virtual": os dados, as empresas, as pessoas e os riscos são reais. As empresas investem muito em segurança técnica (firewalls, criptografia, antivírus), mas muitas vezes o fator mais vulnerável é o comportamento humano. Este guia aborda as principais ameaças, com foco especial na manipulação psicológica (engenharia social), nos ataques técnicos e nos controles corporativos para a proteção da informação.

## 2. Pontos Principais

### A. Engenharia Social e Golpes
*   **O que é:** É a técnica usada por golpistas (engenheiros sociais) para manipular pessoas, utilizando persuasão e influência para que revelem dados pessoais ou corporativos.
*   **Gatilhos Psicológicos:** Os ataques exploram emoções humanas como medo, ganância, curiosidade, vaidade, urgência e solidariedade.
*   **Principais Vetores:**
    *   **Phishing:** Uso de mensagens eletrônicas (e-mails, SMS) que parecem ser de fontes legítimas para "pescar" informações do usuário ou induzir o clique em links maliciosos.
    *   **Vishing e Smishing:** Vishing é o golpe aplicado por telefone (falsa central de atendimento), enquanto o Smishing ocorre via SMS (mensagens ameaçadoras ou promoções irreais).
    *   **Sites Falsos:** Páginas que imitam o layout de grandes instituições ou comércio eletrônico para roubar dados de cartão de crédito e senhas.

### B. Ameaças Técnicas (Malware e Ataques)
*   **Códigos Maliciosos (Malware):** Softwares desenvolvidos para executar ações danosas. Incluem Vírus, Worms, Trojans (Cavalos de Troia, que roubam dados bancários), Ransomware (sequestro de dados mediante resgate) e Spywares.
*   **Ataques na Rede:** Cibercriminosos utilizam técnicas como exploração de vulnerabilidades, ataques de força bruta (para descobrir senhas), negação de serviço (DDoS) e interceptação de tráfego (Sniffing).

### C. Segurança Corporativa e Proteção de Dados
*   **Gestão de Vulnerabilidades:** É o processo contínuo de identificar, avaliar e remediar vulnerabilidades em sistemas e redes corporativas (gestão de patches e scans automatizados).
*   **Controles de Proteção:**
    *   **Criptografia:** Protege dados em trânsito (redes, internet) e dados em repouso (armazenados), tornando-os ilegíveis para usuários não autorizados.
    *   **Controle de Acesso e Segmentação:** Garantir que o acesso seja restrito apenas a quem precisa (privilégio mínimo) e separar fisicamente ou logicamente os sistemas críticos.
    *   **DLP (Data Loss Prevention):** Estratégias e ferramentas para detectar e evitar o vazamento ou a exfiltração de dados sensíveis.
*   **Normas e Frameworks:** Organizações baseiam-se em padrões reconhecidos como ISO 27001/27002, LGPD, CIS Controls, NIST e PCI-DSS (focado em cartões de pagamento) para criar seus sistemas de gestão de segurança.

### D. Mecanismo Especial de Devolução do Pix (MED)
*   **O que é:** Recurso do Banco Central que facilita a devolução de valores em casos de fraude ou falha operacional.
*   **Prazos:** A vítima tem até 80 dias após a transação para solicitar a abertura do MED. O banco do recebedor tem 7 dias para analisar a fraude e bloquear os fundos. Confirmada a fraude, a devolução aos bancos envolvidos é finalizada em até 96 horas.

---

## 3. Passo a Passo de Prevenção

### Para o Usuário (Pessoa Física):
1.  **Fortaleça a Autenticação:** Crie senhas fortes e sempre ative a Verificação em Duas Etapas (2FA) em seus aplicativos (como WhatsApp e e-mails). Nunca repasse o código recebido por SMS.
2.  **Verifique a Fonte:** Desconfie de mensagens que exigem urgência, ameaçam bloquear contas ou oferecem grandes vantagens. Na dúvida, não clique; acesse o site oficial digitando o endereço no navegador.
3.  **Atenção nas Compras e Transferências:** Em compras online, pesquise a reputação da loja e verifique se o site possui conexão segura (HTTPS). No Pix, confira sempre os dados do recebedor antes de confirmar a senha.
4.  **Limite a Exposição Social:** Configure a privacidade das suas redes sociais e evite compartilhar sua localização rotineira ou detalhes do trabalho. Golpistas usam essas informações contra você.

### Para o Ambiente Corporativo:
1.  **Educação Contínua:** Implemente um programa contínuo de conscientização em segurança. Realize campanhas simuladas de phishing e testes para garantir que todos entendam os riscos.
2.  **Ambiente Seguro:** Adote políticas de Mesa Limpa e Tela Limpa: bloqueie o computador ao se ausentar e não deixe documentos sensíveis com senhas, crachás ou dados expostos sobre a mesa.
3.  **Desenvolvimento e Monitoramento:** Aplique o Ciclo de Vida Seguro de Desenvolvimento de Software (SSDLC), faça o gerenciamento constante de acessos administrativos e utilize ferramentas de monitoramento em tempo real (como SIEM e antivírus atualizados).

### O que fazer em caso de Incidente (Golpe/Fraude):
1.  **Contate as Instituições:** Comunique o seu banco imediatamente usando canais oficiais. Em caso de Pix, solicite a abertura de uma notificação de infração via MED pelo seu aplicativo ou telefone.
2.  **Proteja seus Acessos:** Mude as senhas de e-mails, bancos e redes sociais envolvidas. Se seu celular for roubado, solicite o bloqueio do chip e dos cartões.
3.  **Gere Provas Legais:** Faça sempre um Boletim de Ocorrência (B.O.), especialmente se houver prejuízo financeiro ou suspeita de furto de identidade (uso do seu CPF por terceiros). Monitore seu nome em serviços como o "Registrato" do Banco Central.