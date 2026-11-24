# Mapa de Objetivos 🎯

<div align="justify">

Após a definição da metamensagem, a equipe construiu o **Mapa de Objetivos** para representar graficamente as metas principais de cada perfil de usuário ao interagir com o sistema, identificando tanto objetivos exclusivos quanto objetivos compartilhados entre as personas.

</div>

## 1. Legenda de Papéis (Personas) 🏷️

<div align="justify">

Para manter a rastreabilidade com as personas definidas na etapa anterior e seguir a notação recomendada pela disciplina, adotaram-se os seguintes papéis no diagrama:

</div>

* **U (Usuários):** Qualquer usuário do sistema (abrangendo tanto emissores quanto interlocutores em fluxos gerais de acesso e conta).
* **U-CAA (Usuário de Comunicação Aumentativa e Alternativa):** Representa os emissores com necessidades comunicacionais (**José Felipe** e **Beatriz Almeida**).
* **U-INT (Usuário Interlocutor):** Representa os interlocutores não familiarizados com CAA (**Fernanda Lima** e demais profissionais/atendentes).

<div align="justify">

*(Notação: `Papel | Objetivo Final`, com setas indicando quais subobjetivos instrumentam diretamente o objetivo principal, sem detalhar ainda planos operacionais)*.

</div>

## 2. Visão Geral do Mapa de Objetivos 🗺️

<img width="7442" height="10521" alt="Mapa de Objetivos drawio_page-0001 (1)" src="https://github.com/user-attachments/assets/f75606fc-9422-4f01-8d6b-47e8aaf1e03c" />

## 3. Detalhamento dos Objetivos por Grupo Funcional 🧩

### 3.1. Gestão de Acesso e Autenticação

* **Objetivo Final:** `U | Autenticar e acessar o sistema`
* **Subobjetivos associados:**
* `U | Escolher entre criar ou entrar em uma conta`
* `U | Escolher o meio de login`
* `U | Recuperar palavra-passe ("esqueceu sua senha?")`
* `U | Alterar palavra-passe`
* `U | Escolher tipo de perfil (Usuário CAA ou Interlocutor)`

### 3.2. Navegação e Contextos (Home CAA)

* **Objetivo Final:** `U-CAA | Acessar Contextos de Comunicação`
* **Subobjetivos associados:**
* `U-CAA | Selecionar o contexto/lugar`
* `U-CAA | Visualizar contextos sugeridos por geolocalização`
* `U-CAA | Selecionar vocabulário geral e rotinas salvas (favoritos)`
* `U-CAA | Acessar Configurações e Perfil`

### 3.3. Comunicação — Pareamento de Sessão (Modo Online / Duas Telas)

* **Objetivo Final:** `U-CAA e U-INT | Estabelecer conexão pareada`
* **Subobjetivos associados:**
* `U-INT | Gerar o QR Code de sessão temporária`
* `U-CAA | Escanear QR Code do dispositivo interlocutor`

### 3.4. Comunicação Assistida por IA

* **Objetivo Final:** `U-CAA e U-INT | Realizar Comunicação Bidirecional`
* **Subobjetivos associados:**
* `U-CAA | Formular frases com pictogramas`
* `U-CAA | Enviar mensagens remotamente`
* `U-INT | Receber mensagem formatada no próprio dispositivo`
* `U-INT | Gravar resposta natural por voz (Microfone)`
* `U-CAA | Visualizar resposta traduzida em pictogramas (IA)`

### 3.5. Comunicação de Contingência (Modo Offline / Tela Única)

* **Objetivo Final:** `U-CAA e U-INT | Comunicar em Dispositivo Único`
* **Subobjetivos associados:**
* `U-CAA | Acessar banco de pictogramas local (Cache)`
* `U-CAA | Formular mensagem no dispositivo`
* `U-CAA | Acionar interface física de interlocutor (Tela interlocutor)`
* `U-INT | Fornecer feedback visual/tátil via botões de resposta rápida`

### 3.6. Gerenciamento de Conta

* **Objetivo Final:** `U-CAA | Gerenciar perfil`
* **Subobjetivos associados:**
* `U | Visualizar dados cadastrais`
* `U | Atualizar informações pessoais (Nome, e-mail)`
* `U | Ajustar preferências de acessibilidade do sistema`
* `U | Encerrar sessão (Logout)`
