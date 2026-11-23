# Diagramas de Interação (MoLIC) 🗨️

Após a modelagem das tarefas nos HTAs, a equipa representou a interação entre os utilizadores e o sistema através da linguagem **MoLIC (*Modeling Language for Interaction as Conversation*)**, evidenciando as cenas de diálogo, as falas do utilizador (`u:`), as respostas do sistema (`d:`), os processamentos internos e as transições de ruptura.

---

## 1. Visão Geral do Diagrama MoLIC Completo 🌐

![Diagrama MoLIC Completo](../assets/molic-completo.png)

---

## 2. Detalhamento do Diagrama por Fluxos Ampliados 🔍

Para garantir a legibilidade e demonstrar o alinhamento direto com cada HTA definido anteriormente, o diagrama completo foi dividido em seis partes correspondentes aos fluxos principais do sistema:

---

### 2.1. Fluxo 1 — Autenticação, Criação de Conta e Escolha de Perfil (HTA 01) 🔐

![MoLIC - HTA 01](../assets/molic-hta-01.png)

* **Descrição Geral:** Modela a entrada no aplicativo desde o ponto de abertura até à definição do papel do utilizador na sessão (**Usuário CAA** ou **Interlocutor**), contemplando o cadastro com validação de e-mail, o acesso via e-mail ou conta Google e a recuperação de palavra-passe.
* **Cenas e Transições:**
  * **Ponto de Abertura $\rightarrow$ Decisão Inicial:** Inicia com `u: escolhi o método de acesso`, direcionando o fluxo para a criação de conta (`u: escolhi criar conta`) ou para o acesso a uma conta existente (`u: escolhi acessar conta`).
  * **Cena `Criar conta` e Cena `Ver email`:** O utilizador informa nome, e-mail e senha (`u: inserir dados`)[cite: 44]. Caso o sistema detete erro, ocorre a transição de ruptura `d: email inválido`[cite: 44]. Com os dados validados (`u: dados inseridos`), segue para a cena `Ver email` (abrir e-mail e aceder ao link) e para a cena `Perfil de usuário` (`XOR` entre **Usuário CAA** e **Interlocutor**)[cite: 44].
  * **Cena `Acessar conta`, `Logar com email` e `Senha esquecida`:** O utilizador escolhe entre conta Google ou e-mail (`XOR`)[cite: 44]. Na cena `Logar com email`, pode regressar (`u: mudou de método`), seguir para validação (`d: validar email`) ou acionar a recuperação (`u: esqueceu a senha`), que conduz à cena `Senha esquecida` e retorna à tela de acesso após redefinição (`senha criada`)[cite: 44].

---

### 2.2. Fluxo 2 — Navegação e Seleção de Contextos (HTA 02) 🧭

![MoLIC - HTA 02](../assets/molic-hta-02.png)

* **Descrição Geral:** Representa a jornada do **Usuário CAA** na tela inicial para escolher o ambiente comunicativo e o tipo de vocabulário que deseja utilizar.
* **Cenas e Transições:**
  * **Cena `Selecionar contexto`:** Apresenta três opções exclusivas (`XOR`): procurar na lista de contextos, pesquisar contexto pelo nome ou utilizar o contexto sugerido via localização[cite: 45].
  * **Cena `Contexto sugerido por localização` e Cena `Interagir com contexto`:** Caso opte pela sugestão automática (`u: contexto via localidade`), visualiza o cartão do local sugerido[cite: 45]. Caso pesquise manualmente (`u: pesquisa o contexto`), o sistema verifica a existência do termo, exibindo a ruptura `d: contexto não achado` em caso de falha ou avançando (`u: contexto encontrado`) para a seleção do ambiente (ex.: restaurante, hospital)[cite: 45].
  * **Cena `Opção de vocabulário`:** Após confirmar o ambiente (`u: contexto selecionado`), o utilizador escolhe (`XOR`) entre **vocabulário geral** ou **rotinas salvas** (`u: opção de vocabulário definida`), acedendo à prancha correspondente (`d: acesso a seção definida`)[cite: 45].

---

### 2.3. Fluxo 3 — Pareamento de Sessão e Contingência Offline (HTA 03) 📲

![MoLIC - HTA 03](../assets/molic-hta-03.png)

* **Descrição Geral:** Detalha o estabelecimento da ligação entre o **Interlocutor** e o **Usuário CAA** no modo online, bem como a transição alternativa para o modo offline caso o tempo de espera expire ou não haja conexão[cite: 46].
* **Cenas e Transições:**
  * **Processamento de Pareamento $\rightarrow$ Cena `Leitura do CAA`:** A partir de `d: pareamento da sessão`, o sistema gera o código (`d: QR code gerado`) e exibe-o na cena `Leitura do CAA`, aguardando a leitura pelo dispositivo do Usuário CAA para abrir o chat partilhado (`u: entrou no chat`)[cite: 46].
  * **Rupturas para a Cena `Modo offline`:** Caso ocorra falha de conexão ou demora na leitura (`d: tempo de espera expirou`), uma transição pontilhada redireciona o interlocutor para a cena `Modo offline` (tela de respostas rápidas/textos), permitindo também sair desse modo (`u: sair do modo offline`)[cite: 46].

---

### 2.4. Fluxo 4 — Comunicação Bidirecional Assistida por IA (HTA 04) 🤖

![MoLIC - HTA 04](../assets/molic-hta-04.png)

* **Descrição Geral:** Modela o ciclo contínuo de diálogo em tempo real entre dois dispositivos pareados, utilizando Inteligência Artificial para traduzir pictogramas em linguagem natural e voz em pictogramas[cite: 47].
* **Cenas e Transições:**
  * **Cena `Mensagem do usuário CAA`:** Após `u: entrou no chat`, o emissor seleciona os pictogramas do contexto, valida a frase estruturada pela IA e envia (`u: enviar mensagem`)[cite: 47].
  * **Cena `Ler a mensagem` e Cena `Gravar a resposta`:** O interlocutor recebe a mensagem (`d: recebe a mensagem`) e escolhe (`XOR`) entre leitura por texto ou por voz[cite: 47]. Em seguida, acede à cena `Gravar a resposta`, fala pelo microfone e confirma o áudio (`u: confirma o audio`)[cite: 47].
  * **Processamento da IA $\rightarrow$ Cena `Ver os Pictogramas`:** O sistema converte a fala em símbolos (`d: a IA cria pictogramas baseados na fala`) e apresenta-os ao Usuário CAA, fechando o ciclo (`d: mensagem emitida`) para novas interações[cite: 47].

---

### 2.5. Fluxo 5 — Comunicação de Contingência em Tela Única (HTA 05) 📴

![MoLIC - HTA 05](../assets/molic-hta-05.png)

* **Descrição Geral:** Apresenta o fluxo de interação offline num único dispositivo partilhado, organizado por passagens explícitas de turno entre emissor e interlocutor.
* **Cenas e Transições:**
  * **Cena `Selecionar contexto` $\rightarrow$ Cena `Interagir com contexto`:** O utilizador pesquisa ou navega na lista local de contextos (com transições de ruptura `d: contexto não encontrado` caso a busca falhe) até selecionar o ambiente desejado (`u: encontrou o contexto`)[cite: 48].
  * **Cena `Enviar mensagem do usuario CAA`:** O emissor escolhe os pictogramas locais, valida a sequência e toca em *"Pronto"* (`u: manda mensagem`)[cite: 48].
  * **Cena `Recebe mensagem` $\rightarrow$ Cena `Receber pictogramas`:** No mesmo aparelho (`d: recebe mensagem`), o interlocutor lê os pictogramas, escolhe uma resposta rápida predefinida e toca em *"Pronto"* (`u: confirmar envio`), permitindo que o sistema exiba a resposta em pictogramas (`d: transformar em pictogramas`) para o feedback final do Usuário CAA[cite: 48].

---

### 2.6. Fluxo 6 — Gerenciamento de Perfil, Acessibilidade e Saída (HTA 06) ⚙️

![MoLIC - HTA 06](../assets/molic-hta-06.png)

* **Descrição Geral:** Agrupa as ações de consulta e edição de conta, personalização de acessibilidade e encerramento de sessão.
* **Cenas e Transições:**
  * **Cena `Ver dados`:** Permite visualizar nome, e-mail e palavra-passe (`u: confirmar acao`).
  * **Cena `Atualizar dados`, `Alterar os campos` e `Alterar email`:** Permite editar nome ou e-mail; caso o e-mail seja modificado (`u: alterar email`), aciona a cena `Alterar email` para definição, confirmação e validação via link no Gmail[cite: 49].
  * **Cena `Acessibilidade do sistema` $\rightarrow$ Cena `Definições de acessibilidade`:** Permite configurar tamanho de fonte/pictogramas, contraste, velocidade e tom da voz TTS (`definiu as configurações`)[cite: 49].
  * **Cena `Sair do sistema` $\rightarrow$ Ponto de Encerramento:** Ao tocar em *"sair/deslogar"*, finaliza a sessão e encerra o diagrama[cite: 43, 49].
