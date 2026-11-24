# Protótipos de Baixa Fidelidade (Sketches) ✏️

<div align="justify">

Com base nos diagramas **MoLIC** e nos **HTAs** definidos na etapa de ideação, a equipe desenvolveu os esboços de telas em baixa fidelidade para representar o fluxo inicial do sistema. Além das telas individuais que compõem a jornada do utilizador, foram elaboradas **duas versões alternativas de fluxo e layout (Versão A e Versão B)** para comparar decisões de navegação, acessibilidade e comunicabilidade.

</div>

<br>

## 1. Visão Geral das Telas Projetadas 📱

<br>

### 1.1. Fluxo de Boas-Vindas e Introdução (Onboarding — 05 Telas) 👋

<div align="justify">

*(Apresentação inicial dos recursos de CAA, pareamento por QR Code, tradução por IA e modo offline)*

</div>

<img width="1150" height="1357" alt="image" src="https://github.com/user-attachments/assets/d7efeca8-dde9-4ae9-926b-c69db8db9a00" />

* **Descrição e Correspondência com o Modelo:** Apresenta ao novo utilizador os pilares do sistema em cinco cartões sequenciais (`Bem-vindo`, `Existem várias formas de falar`, `Dois aparelhos, uma conexão`, `Mais compreensão, menos barreiras` e `Funciona mesmo sem internet`), reduzindo o receio inicial antes do acesso à conta.
* **Análise de Design:**
* **Usabilidade:** Indicadores de progresso na base e botões únicos de avanço (`Conhecer >`, `Continuar`, `Vamos lá?`) tornam a navegação linear e previsível.
* **Comunicabilidade:** Textos curtos aliados a ícones ilustrativos explicam de forma direta como o aplicativo funciona sem exigir leitura técnica.
* **Experiência do Usuário (UX):** Transmite acolhimento e clareza logo no primeiro contacto com o sistema.

<br>

### 1.2. Telas Principais de Acesso, Perfil, Home CAA e Pareamento (05 Telas) 🔐

<div align="justify">

*(Alinhamento: **HTAs 01, 02 e 03** e **Fluxos 1, 2 e 3 do MoLIC**)*

</div>

<img width="1050" height="1180" alt="image" src="https://github.com/user-attachments/assets/cb7e7cf0-e6df-4b8a-9e9c-9596970181b4" />

* **Tela 01 — Acesso (`Bem-vindo`):** Corresponde à cena `Acessar conta` do MoLIC, oferecendo login por e-mail e palavra-passe, recuperação (`Esqueci minha senha`), acesso social (`Continuar com Google` / `Continuar com Apple`) e atalho para criação de conta.
* **Tela 02 — Cadastro (`Crie sua conta`):** Corresponde à cena `Criar conta` do MoLIC, com campos claros e lista visual de requisitos mínimos da palavra-passe (8 caracteres, letra maiúscula e número) para prevenir erros de preenchimento.
* **Tela 03 — Escolha de Papel (`Vamos personalizar sua experiência`):** Corresponde à cena `Perfil de usuário` do MoLIC, permitindo escolher entre **Sou comunicador** (Usuário CAA) e **Sou ouvinte** (Interlocutor).
* **Tela 04 — Tela Inicial (`Home CAA`):** Corresponde às cenas `Selecionar contexto` e `Opção de vocabulário` do MoLIC, reunindo barra de pesquisa, botão de pareamento por QR Code (`Comunique-se à distância`), sugestão automática por geolocalização (`Você parece estar em um restaurante...`), acesso rápido a `Rotinas salvas`, lista de `Contextos` (`Hospital`, `Restaurante`, `Transporte`, `Social`) e barra inferior (`Início`, `Prancha`, `Offline`, `Ajustes`).
* **Tela 05 — Leitura de Código (`Escaneie o QR Code`):** Corresponde ao fluxo de pareamento do **HTA 03**, exibindo área centralizada da câmara com orientação objetiva (`Mantenha o QR Code dentro da área de leitura`).


<br>

### 1.3. Fluxo de Boas-Vindas e Introdução — Versão B (05 Telas) 👋

<div align="justify">

*(Apresentação alternativa do onboarding, com slides informativos sobre comunicação por CAA, conexão à distância, tradução das respostas por IA e funcionamento offline)*

</div>

<img width="1050" height="1180" alt="onboarding_melhorado" src="https://github.com/user-attachments/assets/e4b5cfc6-9cd7-4c4a-a0e2-d714ba63a6b2" />

* **Descrição e Correspondência com o Modelo:** O fluxo é composto por cinco telas. A primeira apresenta a mensagem de boas-vindas (`Bem-vindo!`) e oferece as ações `Conhecer` e `Sair`. As quatro telas seguintes apresentam, em sequência, os principais recursos do aplicativo: comunicação por meio do toque em figuras para reproduzir mensagens em voz; conexão à distância por meio da leitura de um QR Code no aparelho do interlocutor; interpretação das respostas do interlocutor por IA, convertendo voz em figuras; e funcionamento mesmo sem conexão com a internet.
* **Análise de Design:**
  * **Usabilidade:** Nas telas informativas, a seta no canto superior esquerdo permite retornar ao slide anterior, enquanto a opção `Pular`, no canto superior direito, possibilita avançar diretamente para o acesso. O indicador de quatro pontos, com o ponto atual alongado, informa o progresso da apresentação. A primeira tela não possui os controles de voltar ou pular, oferecendo apenas as opções `Conhecer` e `Sair`. O texto de apoio é curto e favorece uma leitura rápida.
  * **Comunicabilidade:** Cada slide procura transmitir uma ideia central — comunicação, conexão, compreensão das respostas e uso offline. Os títulos em duas linhas, com palavras-chave em negrito, reforçam visualmente o benefício apresentado. Entretanto, há repetição do texto de apoio sobre a IA traduzir a voz em figuras nas telas 4 e 5; na última tela, o conteúdo deveria explicar o funcionamento sem internet.
  * **Experiência do Usuário (UX):** A sequência apresenta os recursos de forma gradual e oferece alternativas de navegação para diferentes níveis de familiaridade com o aplicativo. O botão final `Vamos lá` funciona como chamada clara para iniciar a utilização. A duplicação do texto de apoio nas duas últimas telas, assim como o pequeno texto ilegível abaixo do botão final, reduz a consistência e pode gerar dúvidas sobre o conteúdo offline.

<br>

### 1.4. Telas de Acesso, Cadastro, Perfil, Home CAA e Pareamento — Versão B (05 Telas) 🔐

<div align="justify">

*(Alternativa de organização das telas principais, com abas de autenticação, cartões de seleção de perfil e disposição dos contextos em grade)*

</div>

<img width="1050" height="1180" alt="wireframes_melhorado" src="https://github.com/user-attachments/assets/576f3f2a-717d-45e8-b947-8426324cfa26" />

* **Tela 01 — Login (`Entrar`):** Apresenta as abas `Entrar` e `Criar conta`, com a primeira selecionada. Disponibiliza campos de e-mail e senha, recuperação de senha (`Esqueci minha senha`), botão principal `Entrar` e opções de autenticação social por Google e Apple.
* **Tela 02 — Cadastro (`Criar conta`):** Mantém as mesmas abas de autenticação, com `Criar conta` selecionada. Reúne campos para nome completo, e-mail, senha e confirmação de senha, além de uma lista de requisitos da senha com marcadores de verificação e o botão `Criar conta`.
* **Tela 03 — Escolha do Tipo de Usuário:** Pergunta `Que tipo de usuário você é?` e apresenta dois cartões grandes empilhados: `Sou comunicador`, acompanhado de um ícone de pessoa com ondas sonoras, e `Sou Ouvinte`, representado por um ícone de pessoa.
* **Tela 04 — Home CAA:** Apresenta cabeçalho com menu hambúrguer, saudação personalizada (`Olá, Carlos`), indicador de estado `online` e ícone de perfil. Abaixo, reúne campo de pesquisa (`Pesquisar contexto...`), cartão de conexão à distância (`Comunique-se à distância`, com botão `Conectar`), sugestão por localização (com ação `Abrir`), atalhos para `Vocabulário Geral` e `Rotinas Salvas`, além da seção `Contextos`, com opção `Ver mais` e grade 2x2 para Restaurante, Hospital, Transporte e Social. A barra inferior apresenta quatro opções, incluindo Início, Offline e Ajustes.
* **Tela 05 — Pareamento:** Exibe o título `Escaneie o QR Code`, com o código em tamanho grande e centralizado dentro de um cartão, além de uma seta de retorno no canto superior esquerdo.
* **Análise de Design:**
  * **Usabilidade:** As abas agrupam login e cadastro em uma mesma área, e as opções de acesso por Google e Apple podem agilizar a entrada. No cadastro, a lista de requisitos da senha antecipa critérios e ajuda a prevenir erros de preenchimento. Na Home CAA, a busca permanece no topo e os contextos estão destacados; o QR Code amplo favorece a leitura pela câmera. Em contrapartida, a quantidade de elementos na tela inicial e o tamanho reduzido de alguns cartões podem dificultar a interação de pessoas com limitações motoras.
  * **Comunicabilidade:** Os rótulos das abas deixam explícitas as ações de entrar e criar conta. Na seleção de perfil, a pergunta direta e os ícones acompanhados de texto ajudam a diferenciar os papéis de comunicador e ouvinte. Na Home, os nomes dos contextos tornam as opções reconhecíveis e o indicador `online` comunica o estado da conexão.
  * **Experiência do Usuário (UX):** A Home concentra recursos relevantes — pesquisa, conexão remota, sugestão por localização, vocabulário, rotinas e contextos — reduzindo a necessidade de navegar entre várias telas para encontrar funções frequentes. Por outro lado, essa concentração torna a interface visualmente mais densa. A grade 2x2 e os cartões menores podem reduzir a área de toque, enquanto a barra inferior com múltiplos itens acrescenta opções simultâneas à navegação.


<br>

## 2. Comparação e Validação de Versões Alternativas (Versão A vs. Versão B) ⚖️

<div align="justify">

*(Evidência obrigatória de discussão entre alternativas de design)*

</div>

<div align="justify">

Para validar a melhor organização visual e de navegação, a equipe prototipou duas variantes completas do fluxo de entrada e da tela principal:

</div>

| Versão A (Escolhida — Lista Vertical e Fluxo Guiado) |
| :---: |
| <img width="1440" height="1084" alt="image" src="https://github.com/user-attachments/assets/c6cbb14b-ef09-4da6-a58f-7ec79e70c5b0" /> |
| Versão B (Alternativa — Abas Superiores e Grade 2x2) |
| :---: |
|<img width="27701" height="7341" alt="Entrar (1)_page-0001" src="https://github.com/user-attachments/assets/a0977432-7a2d-43ad-9e92-9b704d12087a" />|

<br>

### Análise Comparativa e Decisão da Equipe

1. **Onboarding (`Versão A` vs. `Versão B`):**
* Na **Versão B**, o botão `Pular` aparece no canto superior direito das quatro telas informativas (2 a 5), mas não na tela inicial de boas-vindas. Embora agilize o avanço, sua posição e dimensão podem exigir maior precisão motora e levar utilizadores iniciantes a saltar explicações importantes sobre o pareamento e o modo offline. A análise do protótipo também identificou a repetição do texto de apoio sobre IA nas duas últimas telas.
* A **Versão A** mantém o foco em botões amplos na base da tela (`Continuar` / `Vamos lá?`) e o botão `Sair` logo na primeira tela para quem já conhece o sistema.
2. **Autenticação e Cadastro (`Versão A` vs. `Versão B`):**
* A **Versão B** utiliza abas alternáveis no topo (`Entrar` | `Criar conta`), enquanto a **Versão A** apresenta telas dedicadas com títulos grandes (`Bem-vindo` e `Crie sua conta`) e links explícitos na base (`Ainda não tem conta? Criar conta` / `Já tem uma conta? Entrar`), oferecendo melhor **comunicabilidade** e menor ambiguidade visual.
3. **Tela Principal — Home CAA (`Versão A` vs. `Versão B`):**
* Na **Versão B**, os contextos (`Restaurante`, `Hospital`, `Transporte`, `Social`) estão organizados em grade 2x2 ao lado de dois cartões menores (`Vocabulário Geral` e `Rotinas Salvas`), aumentando a densidade de elementos próximos na metade inferior do ecrã.
* A **Versão A** (adotada como solução final) organiza `Rotinas salvas` e os `Contextos` em cartões horizontais largos de largura total, proporcionando **alvos de toque maiores** (essencial para utilizadores com dificuldades motoras), leitura vertical previsível e melhor ergonomia para uso com uma só mão.

<br>

## Conclusão

<div align="justify">

Os sketches materializam, em baixa fidelidade, parte dos fluxos definidos nos HTAs e nos diagramas MoLIC. O documento reúne cinco telas de onboarding e cinco telas relacionadas a acesso, cadastro, escolha de perfil, Home CAA e leitura do QR Code, além de comparar duas alternativas de organização. A equipe registra a escolha da Versão A por favorecer botões e cartões maiores, uma navegação vertical guiada e telas dedicadas para acesso e cadastro. Essa decisão está fundamentada na análise apresentada no próprio documento; os sketches, por serem protótipos de baixa fidelidade, não equivalem a uma comprovação empírica de usabilidade.

</div>
