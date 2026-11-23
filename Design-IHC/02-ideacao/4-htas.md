
# Análise Hierárquica de Tarefas (HTAs) 🌳

Com base nos objetivos principais definidos no Mapa de Objetivos, a equipe modelou **06 diagramas HTA (Hierarchical Task Analysis)**. Cada diagrama abaixo é apresentado **lado a lado** com o recorte correspondente do Mapa de Objetivos para evidenciar a rastreabilidade e a consistência hierárquica entre o planejamento e o detalhamento das tarefas.

---

## 1. HTA 01 — Autenticar e Acessar o Sistema 🔐

*(Correspondente ao bloco **Gestão de Acesso e Autenticação** do Mapa de Objetivos)*

| Recorte do Mapa de Objetivos | Diagrama HTA 01 |
| :---: | :---: |
| ![Recorte Mapa - Autenticação](../assets/recorte-mapa-01.png) | ![HTA 01 - Autenticar e Acessar o Sistema](../assets/hta-01.png) |

* **Propósito:** Modelar o fluxo inicial de entrada na aplicação, garantindo um processo de autenticação seguro, acessível e flexível para ambos os perfis de usuário antes do início da comunicação.
* **Descrição das Tarefas e Decisões de Design:** A tarefa principal inicia com a abertura do aplicativo (`1`), seguida pela escolha condicional (**Plano 0:** `1 > (2 / 3) > 5`) entre realizar um novo cadastro (`2`) ou acessar uma conta existente (`3`). No fluxo de cadastro, o usuário insere seus dados básicos (`2.1` a `2.3`) e realiza a validação obrigatória por link enviado ao e-mail (`2.4.1` e `2.4.2`) antes de concluir o registro (`2.5`). Para usuários já cadastrados, o sistema oferece tanto o login tradicional por e-mail e senha (`3.1` e `3.2`) quanto a autenticação social via Google ou Apple (`3.3`), decisão tomada para reduzir a carga cognitiva e o esforço de digitação. Caso o usuário esqueça sua credencial, o fluxo alternativo de recuperação (`4`) permite redefinir a senha via e-mail (`4.1` a `4.4`) e retornar ao login. Por fim, o usuário define seu papel na sessão (`5`), escolhendo entre o perfil de **Usuário CAA** (`5.1`) ou **Interlocutor** (`5.2`), o que direciona a interface para as funcionalidades específicas de cada ator. *(Nota: O sub-objetivo de alteração de senha previsto no Mapa de Objetivos ocorre após o login, sendo contemplado na gestão de conta)*.

---

## 2. HTA 02 — Tela Principal: Navegação e Contextos (Usuário CAA) 🧭

*(Correspondente ao bloco **Navegação e Contextos (Home CAA)** do Mapa de Objetivos)*

| Recorte do Mapa de Objetivos | Diagrama HTA 02 |
| :---: | :---: |
| ![Recorte Mapa - Navegação e Contextos](../assets/recorte-mapa-02.png) | ![HTA 02 - Tela Principal Usuário CAA](../assets/hta-02.png) |

* **Propósito:** Estruturar a navegação inicial do Usuário CAA após a autenticação, permitindo que ele alcance rapidamente o conjunto de pictogramas mais adequado à sua situação comunicativa atual.
* **Descrição das Tarefas e Decisões de Design:** A partir da tela inicial, o Usuário CAA dispõe de quatro caminhos independentes (**Plano 0:** `1 / 2 / 3 / 4`) adaptados a diferentes cenários de uso. Ele pode selecionar manualmente um ambiente na grade de contextos ou filtrar pela barra de pesquisa (`1.1` a `1.3.2`), aceitar uma sugestão automática exibida por geolocalização (`2.1` e `2.2`), acessar diretamente o vocabulário geral ou suas rotinas favoritas salvas (`3.1` e `3.2`), ou navegar até as configurações do perfil (`4`). A decisão de combinar sugestões baseadas em GPS com atalhos de rotinas favoritas visa minimizar o número de toques necessários e reduzir a fadiga motora, permitindo que a comunicação seja iniciada com agilidade em ambientes dinâmicos.

---

## 3. HTA 03 — Pareamento de Sessão (Interlocutor) 📲

*(Correspondente ao bloco **Pareamento de Sessão (Modo Online / Duas Telas)** do Mapa de Objetivos)*

| Recorte do Mapa de Objetivos | Diagrama HTA 03 |
| :---: | :---: |
| ![Recorte Mapa - Pareamento](../assets/recorte-mapa-03.png) | ![HTA 03 - Pareamento de Sessão](../assets/hta-03.png) |

* **Propósito:** Definir como o Interlocutor estabelece a conexão de diálogo com o Usuário CAA, oferecendo tanto o pareamento sincronizado entre dois dispositivos quanto uma alternativa imediata de contingência offline.
* **Descrição das Tarefas e Decisões de Design:** Ao entrar no perfil de Interlocutor, o usuário escolhe entre duas modalidades exclusivas (**Plano 0:** `1 / 2`). No modo online padrão (`1`), o sistema gera e exibe automaticamente na tela um QR Code temporário em destaque (`1.1`), aguardando apenas a leitura pela câmera do dispositivo do Usuário CAA para abrir o chat pareado (`1.2`). Caso não haja conexão com a internet ou o interlocutor não disponha de um segundo aparelho, ele pode acionar o modo offline (`2.1`), abrindo imediatamente a interface compartilhada de respostas rápidas e texto (`2.2`). A geração automática do QR Code sem cliques intermediários foi projetada para eliminar atritos e constrangimentos em atendimentos reais, enquanto o botão de contingência visível na mesma tela assegura que a comunicação nunca seja interrompida.

---

## 4. HTA 04 — Realizar Comunicação Bidirecional (Assistida por IA) 🤖

*(Correspondente ao bloco **Comunicação Assistida por IA** do Mapa de Objetivos)*

| Recorte do Mapa de Objetivos | Diagrama HTA 04 |
| :---: | :---: |
| ![Recorte Mapa - Comunicação IA](../assets/recorte-mapa-04.png) | ![HTA 04 - Comunicação Bidirecional IA](../assets/hta-04.png) |

* **Propósito:** Representar o ciclo completo de diálogo em tempo real entre o Usuário CAA e o Interlocutor em dispositivos pareados, utilizando Inteligência Artificial como mediadora bidirecional entre pictogramas e linguagem natural.
* **Descrição das Tarefas e Decisões de Design:** A interação ocorre em um ciclo sequencial de quatro etapas (**Plano 0:** `1 > 2 > 3 > 4`) que se repete ao longo da conversa. Primeiro, o Usuário CAA seleciona pictogramas na grade de contexto (`1.1`), confere a frase estruturada gramaticalmente pela IA (`1.2`) e realiza o envio (`1.3`). Na sequência, o Interlocutor lê a mensagem formatada em texto claro em seu próprio aparelho (`2.1`), tendo a opção complementar de acionar a síntese de voz (`2.2`). Para responder, o Interlocutor grava sua fala pelo microfone (`3.1` a `3.3`), que é transcrita e convertida em pictogramas pela IA. Por fim, o Usuário CAA visualiza a resposta traduzida em sequência visual (`4.1`), podendo tocar nos pictogramas para ouvir a pronúncia individual (`4.2`). Essa arquitetura permite que o interlocutor se comunique naturalmente sem precisar dominar sistemas pictográficos, ao mesmo tempo em que oferece suporte visual e auditivo redundante ao usuário CAA.

---

## 5. HTA 05 — Comunicação de Contingência (Modo Offline / Tela Única) 📴

*(Correspondente ao bloco **Comunicação de Contingência (Modo Offline / Tela Única)** do Mapa de Objetivos)*

| Recorte do Mapa de Objetivos | Diagrama HTA 05 |
| :---: | :---: |
| ![Recorte Mapa - Contingência Offline](../assets/recorte-mapa-05.png) | ![HTA 05 - Comunicação de Contingência](../assets/hta-05.png) |

* **Propósito:** Assegurar que a interação comunicativa entre o Usuário CAA e o Interlocutor funcione de forma autônoma em um único aparelho, sem dependência de conexão com a internet ou processamento em nuvem.
* **Descrição das Tarefas e Decisões de Design:** O fluxo organiza o compartilhamento físico do dispositivo em quatro etapas sequenciais de passagem de turno (**Plano 0:** `1 > 2 > 3 > 4`). Inicialmente, o Usuário CAA seleciona o contexto local (`1.1` a `1.3`), monta sua sequência de pictogramas e confirma sua vez tocando em *"Pronto"* (`2.1` a `2.3`). Na mesma tela, o Interlocutor lê a transcrição local dos pictogramas (`3.1`), escolhe uma resposta rápida por meio de botões predefinidos (`3.2`) e toca em *"Pronto"* (`3.3`) para devolver o turno. Por último, o Usuário CAA interpreta a resposta convertida em pictograma (`4.1`) e pode emitir um feedback visual imediato (`4.2`). O uso de botões explícitos de passagem de turno e respostas predefinidas evita toques acidentais durante o manuseio compartilhado do smartphone e mantém a fluidez do diálogo em locais sem cobertura de dados.

---

## 6. HTA 06 — Gerenciar Perfil ⚙️

*(Correspondente ao bloco **Gerenciamento de Conta** do Mapa de Objetivos)*

| Recorte do Mapa de Objetivos | Diagrama HTA 06 |
| :---: | :---: |
| ![Recorte Mapa - Gerenciar Perfil](../assets/recorte-mapa-06.png) | ![HTA 06 - Gerenciar Perfil](../assets/hta-06.png) |

* **Propósito:** Permitir que os usuários consultem e atualizem seus dados cadastrais, personalizem parâmetros de acessibilidade da interface e encerrem sua sessão de forma segura.
* **Descrição das Tarefas e Decisões de Design:** Ao acessar a área de perfil, o usuário visualiza seus dados cadastrais (`1`) e pode optar por atualizar informações pessoais (`2`), ajustar preferências de acessibilidade (`3`) ou encerrar a sessão (`4`). Na edição de perfil (`2.1` a `2.4`), a alteração do endereço de e-mail dispara um subfluxo obrigatório de verificação por link (`2.3.1` a `2.3.4`) para manter a integridade da conta. Na seção de acessibilidade (`3.1` e `3.2`), o usuário configura elementos críticos como tamanho da fonte e dos pictogramas, contraste de cores e velocidade ou tom da síntese de voz (TTS). Já o encerramento de sessão exige uma etapa dupla de confirmação (`4.1` e `4.2`), decisão adotada para prevenir saídas acidentais causadas por dificuldades motoras.
