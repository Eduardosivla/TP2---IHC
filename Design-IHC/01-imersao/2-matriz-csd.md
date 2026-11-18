# Matriz CSD (Certezas, Suposições e Dúvidas)

Após a realização do briefing com o representante do cliente, a equipe organizou as informações coletadas na Matriz CSD abaixo para distinguir os fatos já comprovados das hipóteses e lacunas que precisam ser investigadas com os usuários finais.

## 1. Visão Geral da Matriz

| Certezas (C) | Suposições (S) | Dúvidas (D) |
| :--- | :--- | :--- |
| *(Fatos comprovados por evidências, falas do cliente, documentos ou normas)* | *(Hipóteses plausíveis da equipe que ainda precisam ser validadas)* | *(Questões em aberto que a equipe ainda não sabe responder)* |
| **C1.** O app deve melhorar a comunicação entre pessoas que usam CAA e interlocutores que não conhecem esses recursos. | **S1.** O celular (ou tablet) é o dispositivo principal tanto do usuário de CAA quanto do interlocutor. | **D1.** Existe necessidade real de login? Que informações de caracterização seriam coletadas? |
| **C2.** O foco é o “outro lado da conversa”: ajudar o interlocutor leigo a entender pictogramas e mensagens do emissor. | **S2.** Interlocutores leigos conseguem entender a mensagem só com pictograma + texto + áudio, sem treinamento prévio. | **D2.** O app precisa funcionar sem conexão com a internet (modo offline)? |
| **C3.** O público inclui usuários de CAA, familiares, cuidadores, professores, profissionais e pessoas não familiarizadas com CAA. | **S3.** Um conjunto de mensagens predefinidas por contexto atende às necessidades reais do usuário de CAA. | **D3.** Quais sistemas de pictogramas os usuários já conhecem e utilizam no dia a dia? |
| **C4.** Os cenários de uso abrangem restaurantes, hospitais, escolas, transportes e outros ambientes do cotidiano. | **S4.** As respostas rápidas predefinidas bastam para o interlocutor responder adequadamente. | **D4.** Quais apps de CAA são usados hoje, e vale a pena planejar integração futura com eles? |
| **C5.** Os problemas centrais são: dificuldade de compreensão, falta de familiaridade com pictogramas, interpretações equivocadas, dependência de terceiros e baixa reciprocidade. | **S5.** O recurso de áudio é útil nos ambientes de uso, mesmo nos mais barulhentos (como restaurantes e transportes). | **D5.** Quem é o perfil predominante de usuário (crianças, adultos, idosos) e com quais deficiências/necessidades? |
| **C6.** As prioridades do cliente são: facilitar a compreensão, permitir respostas simples e rápidas, evitar falhas, dar controle ao usuário e promover autonomia. | **S6.** O usuário de CAA conseguirá confirmar, corrigir ou rejeitar a interpretação do interlocutor de forma autônoma. | **D6.** A interação acontece em um único aparelho (compartilhado na hora) ou em dois aparelhos distintos? |
| **C7.** O MVP contará com: seleção de contexto, mensagens predefinidas (texto + pictograma), modo interlocutor simplificado, respostas rápidas, validação da interpretação, áudio e interface mobile. | **S7.** O app precisa de login/cadastro com informações de caracterização do usuário (conforme apontado na síntese inicial). | **D7.** O interlocutor responde apenas com opções rápidas ou também precisa de campo de texto livre? |
| **C8.** Não há integrações externas definidas para o escopo do MVP. | **S8.** Os usuários de CAA têm perfis variados (idade, alfabetização, habilidade motora) que exigem diferentes níveis de adaptação na interface. | **D8.** Quais mensagens são indispensáveis em cada contexto específico (restaurante, hospital, escola, transporte)? |
| **C9.** Os dados tratados são: mensagens selecionadas, respostas dos interlocutores, confirmações de entendimento e preferências de contexto. | **S9.** O app será usado em situações de pressa ou estresse (ex.: atendimento hospitalar, filas), exigindo interação rápida. | **D9.** Quais cuidados de privacidade e segurança são necessários, especialmente em contextos de saúde? |
| — | **S10.** O app funcionaria como complemento aos aplicativos de CAA que os usuários já utilizam. | **D10.** Que limitações dos dispositivos (tamanho de tela, volume de áudio, acessibilidade motora) podem afetar o uso? |
| — | — | **D11.** Como medir na prática os indicadores de “maior compreensão” e “menos falhas de comunicação”? |

---

## 2. Detalhamento e Justificativa dos Pontos

### Certezas
* **C1 (Objetivo central do produto):** Confirmado no briefing como a motivação principal do projeto — preencher a lacuna comunicativa entre pessoas que utilizam Comunicação Aumentativa e Alternativa (CAA) e o público geral.
* **C2 (Diferencial e foco no interlocutor):** Estabelecido pelo cliente como o recorte estratégico da solução, direcionando o design não apenas para quem emite a mensagem, mas para tornar a leitura e a resposta imediatas para quem não domina CAA.
* **C3 (Atores e público-alvo):** Definido no levantamento inicial de envolvidos, abrangendo tanto os emissores (usuários de CAA) quanto sua rede de apoio (familiares, cuidadores, professores) e interlocutores externos (atendentes, profissionais de saúde, motoristas).
* **C4 (Contextos reais de aplicação):** Mapeado durante o briefing como os ambientes cotidianos onde ocorrem trocas comunicativas rápidas e funcionais (restaurantes, hospitais, escolas e transportes).
* **C5 (Dores e gargalos atuais):** Relatado pelo cliente como o diagnóstico do problema atual: barreiras de entendimento mútuo, desconhecimento dos símbolos gráficos pelos leigos, ruídos de interpretação e dependência de acompanhantes para mediar conversas.
* **C6 (Critérios de prioridade):** Definido pelo cliente como norteador das decisões de design, priorizando clareza, agilidade na resposta, redução de erros interpretativos e autonomia do usuário de CAA.
* **C7 (Escopo funcional do MVP):** Acordado no briefing como o conjunto mínimo de recursos necessários para validar a proposta em dispositivos móveis (contextos, pranchas com texto + pictograma, modo interlocutor, respostas rápidas, mecanismo de confirmação/correção/rejeição e saída de áudio).
* **C8 (Restrição de integração):** Confirmado como restrição técnica inicial — o MVP operará de forma independente, sem acoplamento com APIs ou plataformas externas nesta primeira versão.
* **C9 (Escopo de dados):** Delimitado no briefing quanto às informações manipuladas durante o fluxo de uso (mensagens escolhidas, retornos do interlocutor, status de confirmação e contextos preferidos).

### Suposições
* **S1 (Uso predominante de smartphones/tablets):** A equipe parte da premissa de que dispositivos móveis pessoais já fazem parte da rotina de comunicação dos usuários de CAA e facilitam a abordagem presencial com interlocutores. Precisa ser confirmado com o público-alvo.
* **S2 (Compreensão intuitiva sem treinamento):** Supõe-se que a combinação multimodal (pictograma + texto claro + áudio) seja suficiente para que um atendente ou profissional entenda a intenção do usuário instantaneamente. Precisa ser testado na prática.
* **S3 (Suficiência das mensagens predefinidas):** Acredita-se que organizar mensagens prontas por ambiente (ex.: hospital, restaurante) cubra a maior parte das demandas comunicativas urgentes sem exigir construção complexa de frases.
* **S4 (Suficiência das respostas rápidas):** Supõe-se que botões de resposta curta para o interlocutor (ex.: *"Entendi"*, *"Aguarde um momento"*, *"Não temos"*) atendam à dinâmica da conversa sem gerar frustração.
* **S5 (Eficácia do áudio em locais ruidosos):** Presume-se que a síntese/reprodução de voz ajude a chamar atenção e reforçar a mensagem mesmo em ambientes movimentados, embora o ruído externo possa limitar sua audibilidade.
* **S6 (Autonomia no ciclo de validação):** A equipe supõe que o usuário de CAA terá condições motoras e cognitivas de operar o fluxo de confirmar, corrigir ou rejeitar o entendimento do interlocutor por conta própria.
* **S7 (Necessidade de cadastro/perfil):** Embora o registro de caracterização do usuário tenha sido citado na síntese inicial, a equipe trata como suposição o quanto um fluxo de login é realmente vantajoso frente à necessidade de acesso imediato.
* **S8 (Heterogeneidade de perfis e adaptações):** Parte-se da hipótese de que diferenças de idade, nível de letramento e coordenação motora exigirão ajustes visuais e de interação (como tamanho de botões e densidade de informação).
* **S9 (Uso sob pressão e restrição de tempo):** Supõe-se que muitas interações ocorrerão em filas, balcões ou triagens médicas, tornando o tempo de resposta e a baixa carga cognitiva fatores críticos de sucesso.
* **S10 (Caráter complementar da ferramenta):** Acredita-se que os usuários já possuam seus próprios sistemas/apps de CAA para comunicação profunda e usarão este aplicativo especificamente como ponte rápida com estranhos.

### Dúvidas
* **D1 (Obrigatoriedade e escopo do login):** É preciso investigar se exigir autenticação cria uma barreira de entrada em situações urgentes e quais dados de perfil realmente agregam valor à adaptação da interface (conecta-se diretamente com `S7`).
* **D2 (Disponibilidade offline):** Importante para definir a arquitetura de armazenamento local de pictogramas e áudios, já que hospitais, transportes e estabelecimentos podem ter sinal instável.
* **D3 (Padrões de pictogramas familiares):** Essencial para escolher bibliotecas visuais (como ARASAAC, PCS, etc.) que o usuário já reconheça, evitando curva de aprendizado desnecessária.
* **D4 (Ecossistema atual de apps de CAA):** Ajuda a entender quais ferramentas os usuários dominam hoje e quais boas práticas ou padrões de interação devem ser respeitados (conecta-se com `S10`).
* **D5 (Recorte demográfico e clínico):** Fundamental para orientar a criação das personas e definir requisitos específicos de acessibilidade visual, auditiva ou motora (conecta-se com `S8`).
* **D6 (Dinâmica física de uso do dispositivo):** Determina completamente o layout da tela — se o celular será virado/entregue ao interlocutor (tela única alternada) ou se haverá interação à distância/pareada (conecta-se com `S1`).
* **D7 (Flexibilidade de resposta do interlocutor):** Necessário verificar se há situações em que respostas prontas não bastam e o interlocutor precisa digitar ou falar algo específico (conecta-se com `S4`).
* **D8 (Vocabulário prioritário por cenário):** Orienta a curadoria inicial de frases e pictogramas para cada ambiente mapeado em `C4` (conecta-se com `S3`).
* **D9 (Privacidade e dados sensíveis):** Crucial para definir mecanismos de proteção, discrição na tela e descarte/armazenamento de histórico, sobretudo quando o usuário relata sintomas ou condições em hospitais.
* **D10 (Restrições de hardware e acessibilidade):** Permite mapear barreiras reais de uso, como toque involuntário, dificuldade de leitura em telas pequenas ou baixo volume de alto-falante.
* **D11 (Métricas de sucesso da comunicação):** Necessário para estabelecer critérios claros de avaliação nos testes de usabilidade e comunicabilidade das etapas seguintes.

---

## 3. Direcionamento para a Pesquisa com Usuários

As **Suposições** e **Dúvidas** levantadas nesta matriz foram agrupadas em quatro eixos de investigação para guiar o roteiro de entrevistas e questionários na etapa seguinte (`3-pesquisa-com-usuario.md`):

1. **Perfil, Acessibilidade e Ecossistema Atual (`S8`, `S10`, `D3`, `D4`, `D5`, `D10`):** Investigar quem são os usuários reais de CAA, quais aplicativos e sistemas de pictogramas já utilizam e quais barreiras motoras, visuais ou cognitivas enfrentam em dispositivos móveis.
2. **Dinâmica da Interação Presencial (`S1`, `S2`, `S5`, `S6`, `S9`, `D6`):** Compreender como ocorre a abordagem com interlocutores leigos em situações cotidianas e de pressa, verificando se o aparelho é compartilhado na mão e como o áudio e os pictogramas são recebidos.
3. **Conteúdo, Contextos e Reciprocidade (`S3`, `S4`, `D7`, `D8`):** Mapear as frases e situações mais críticas em restaurantes, hospitais, escolas e transportes, além de validar se respostas rápidas bastam ou se o interlocutor precisa de entrada livre.
4. **Acesso, Privacidade e Funcionamento Técnico (`S7`, `D1`, `D2`, `D9`, `D11`):** Avaliar a necessidade de cadastro/login, a importância do uso sem internet e os cuidados com a exposição de informações pessoais ou de saúde em locais públicos.
