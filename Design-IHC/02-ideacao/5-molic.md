# Diagramas de Interação (MoLIC) 🗨️

<div align="justify">

Após a modelagem das tarefas nos HTAs, a equipa representou a interação entre os utilizadores e o sistema através da linguagem **MoLIC (*Modeling Language for Interaction as Conversation*)**, evidenciando as cenas de diálogo, as falas do utilizador (`u:`), as respostas do sistema (`d:`), os processamentos internos e as transições de ruptura.

</div>

<br>

## Visão Geral do Diagrama MoLIC Completo 🌐

<img width="6229" height="1752" alt="image" src="https://github.com/user-attachments/assets/6d067ad3-e507-4270-8250-98c5dc8be3fc" />

<br>

## Detalhamento do Diagrama por Fluxos Ampliados 🔍

<br>

### Fluxo 1 — Autenticação, Criação de Conta e Escolha de Perfil (HTA 01) 🔐

<img width="790" height="1632" alt="image" src="https://github.com/user-attachments/assets/c74ad890-f08b-4a5f-9ce8-2db3968c1418" />

* **Descrição Geral:** Modela a entrada no aplicativo desde o ponto de abertura até à definição do papel do utilizador na sessão (**Usuário CAA** ou **Interlocutor**), contemplando o cadastro com validação de e-mail, o acesso via e-mail ou conta Google e a recuperação de palavra-passe.
* **Cenas e Transições:**
* **Ponto de Abertura $\rightarrow$ Decisão Inicial:** Inicia com `u: escolhi o método de acesso`, direcionando o fluxo para a criação de conta (`u: escolhi criar conta`) ou para o acesso a uma conta existente (`u: escolhi acessar conta`).
* **Cena `Criar conta` e Cena `Ver email`:** O utilizador informa nome, e-mail e senha (`u: inserir dados`). Caso o sistema detete erro, ocorre a transição de ruptura `d: email inválido`. Com os dados validados (`u: dados inseridos`), segue para a cena `Ver email` (abrir e-mail e aceder ao link) e para a cena `Perfil de usuário` (`XOR` entre **Usuário CAA** e **Interlocutor**).
* **Cena `Acessar conta`, `Logar com email` e `Senha esquecida`:** O utilizador escolhe entre conta Google ou e-mail (`XOR`). Na cena `Logar com email`, pode regressar (`u: mudou de método`), seguir para validação (`d: validar email`) ou acionar a recuperação (`u: esqueceu a senha`), que conduz à cena `Senha esquecida` e retorna à tela de acesso após redefinição (`senha criada`).

<br>

### Fluxo 2 — Navegação e Seleção de Contextos (HTA 02) 🧭

<img width="4044" height="7013" alt="image" src="https://github.com/user-attachments/assets/f859e32d-c3fb-4fc7-9202-d370669a53d3" />

* **Descrição Geral:** Representa a jornada do **Usuário CAA** na tela inicial para escolher o ambiente comunicativo e o tipo de vocabulário que deseja utilizar.
* **Cenas e Transições:**
* **Cena `Selecionar contexto`:** Apresenta três opções exclusivas (`XOR`): procurar na lista de contextos, pesquisar contexto pelo nome ou utilizar o contexto sugerido via localização.
* **Cena `Contexto sugerido por localização` e Cena `Interagir com contexto`:** Caso opte pela sugestão automática (`u: contexto via localidade`), visualiza o cartão do local sugerido. Caso pesquise manualmente (`u: pesquisa o contexto`), o sistema verifica a existência do termo, exibindo a ruptura `d: contexto não achado` em caso de falha ou avançando (`u: contexto encontrado`) para a seleção do ambiente (ex.: restaurante, hospital).
* **Cena `Opção de vocabulário`:** Após confirmar o ambiente (`u: contexto selecionado`), o utilizador escolhe (`XOR`) entre **vocabulário geral** ou **rotinas salvas** (`u: opção de vocabulário definida`), acedendo à prancha correspondente (`d: acesso a seção definida`).

<br>

### Fluxo 3 — Pareamento de Sessão e Contingência Offline (HTA 03) 📲

<img width="4964" height="5173" alt="image" src="https://github.com/user-attachments/assets/5f38de66-d256-441d-b571-c51776842fbc" />

* **Descrição Geral:** Detalha o estabelecimento da ligação entre o **Interlocutor** e o **Usuário CAA** no modo online, bem como a transição alternativa para o modo offline caso o tempo de espera expire ou não haja conexão.
* **Cenas e Transições:**
* **Processamento de Pareamento $\rightarrow$ Cena `Leitura do CAA`:** A partir de `d: pareamento da sessão`, o sistema gera o código (`d: QR code gerado`) e exibe-o na cena `Leitura do CAA`, aguardando a leitura pelo dispositivo do Usuário CAA para abrir o chat partilhado (`u: entrou no chat`).
* **Rupturas para a Cena `Modo offline`:** Caso ocorra falha de conexão ou demora na leitura (`d: tempo de espera expirou`), uma transição pontilhada redireciona o interlocutor para a cena `Modo offline` (tela de respostas rápidas/textos), permitindo também sair desse modo (`u: sair do modo offline`).

<br>

### Fluxo 4 — Comunicação Bidirecional Assistida por IA (HTA 04) 🤖

<img width="4964" height="7013" alt="image" src="https://github.com/user-attachments/assets/7281f3d3-5107-4377-83c7-b9eeed455c2c" />

* **Descrição Geral:** Modela o ciclo contínuo de diálogo em tempo real entre dois dispositivos pareados, utilizando Inteligência Artificial para traduzir pictogramas em linguagem natural e voz em pictogramas.
* **Cenas e Transições:**
* **Cena `Mensagem do usuário CAA`:** Após `u: entrou no chat`, o emissor seleciona os pictogramas do contexto, valida a frase estruturada pela IA e envia (`u: enviar mensagem`).
* **Cena `Ler a mensagem` e Cena `Gravar a resposta`:** O interlocutor recebe a mensagem (`d: recebe a mensagem`) e escolhe (`XOR`) entre leitura por texto ou por voz. Em seguida, acede à cena `Gravar a resposta`, fala pelo microfone e confirma o áudio (`u: confirma o audio`).
* **Processamento da IA $\rightarrow$ Cena `Ver os Pictogramas`:** O sistema converte a fala em símbolos (`d: a IA cria pictogramas baseados na fala`) e apresenta-os ao Usuário CAA, fechando o ciclo (`d: mensagem emitida`) para novas interações.

<br>

### Fluxo 5 — Comunicação de Contingência em Tela Única (HTA 05) 📴

<img width="4339" height="7013" alt="image" src="https://github.com/user-attachments/assets/69dcb161-7425-432b-ad31-746e775ef196" />

* **Descrição Geral:** Apresenta o fluxo de interação offline num único dispositivo partilhado, organizado por passagens explícitas de turno entre emissor e interlocutor.
* **Cenas e Transições:**
* **Cena `Selecionar contexto` $\rightarrow$ Cena `Interagir com contexto`:** O utilizador pesquisa ou navega na lista local de contextos (com transições de ruptura `d: contexto não encontrado` caso a busca falhe) até selecionar o ambiente desejado (`u: encontrou o contexto`).
* **Cena `Enviar mensagem do usuario CAA`:** O emissor escolhe os pictogramas locais, valida a sequência e toca em *"Pronto"* (`u: manda mensagem`).
* **Cena `Recebe mensagem` $\rightarrow$ Cena `Receber pictogramas`:** No mesmo aparelho (`d: recebe mensagem`), o interlocutor lê os pictogramas, escolhe uma resposta rápida predefinida e toca em *"Pronto"* (`u: confirmar envio`), permitindo que o sistema exiba a resposta em pictogramas (`d: transformar em pictogramas`) para o feedback final do Usuário CAA.

<br>

### Fluxo 6 — Gerenciamento de Perfil, Acessibilidade e Saída (HTA 06) ⚙️

<img width="812" height="1002" alt="image" src="https://github.com/user-attachments/assets/3e3baa42-0e4e-47c7-929e-29e0dcc7ee81" />

* **Descrição Geral:** Agrupa as ações de consulta e edição de conta, personalização de acessibilidade e encerramento de sessão.
* **Cenas e Transições:**
* **Cena `Ver dados`:** Permite visualizar nome, e-mail e palavra-passe (`u: confirmar acao`).
* **Cena `Atualizar dados`, `Alterar os campos` e `Alterar email`:** Permite editar nome ou e-mail; caso o e-mail seja modificado (`u: alterar email`), aciona a cena `Alterar email` para definição, confirmação e validação via link no Gmail.
* **Cena `Acessibilidade do sistema` $\rightarrow$ Cena `Definições de acessibilidade`:** Permite configurar tamanho de fonte/pictogramas, contraste, velocidade e tom da voz TTS (`definiu as configurações`).
* **Cena `Sair do sistema` $\rightarrow$ Ponto de Encerramento:** Ao tocar em *"sair/deslogar"*, finaliza a sessão e encerra o diagrama.

<br>

## Conclusão

<div align="justify">

Os diagramas MoLIC representam a interação como uma conversa entre usuários e sistema, registrando cenas, falas, respostas, processamentos e caminhos de ruptura. Os seis fluxos documentados abrangem autenticação e escolha de perfil, seleção de contextos, pareamento online e contingência offline, comunicação bidirecional com IA, uso em dispositivo único e gerenciamento de perfil. Dessa forma, o material complementa os HTAs ao explicitar como a interação pode se desenvolver e como o sistema responde às ações ou a situações alternativas. Trata-se da especificação conceitual dos diálogos previstos, e não de um resultado de testes ou de implementação.

</div>
