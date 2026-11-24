# Matriz CSD (Certezas, Suposições e Dúvidas) 💡

<div align="justify">

Após a realização do briefing com o representante do cliente, a equipe organizou as informações coletadas na Matriz CSD abaixo para distinguir os fatos já comprovados das hipóteses e lacunas que precisam ser investigadas com os usuários finais.

</div>

## 1. Visão Geral da Matriz 📝

<img width="1600" height="718" alt="image" src="https://github.com/user-attachments/assets/752953e0-cd75-4630-bfa6-c1a67728ede7" />

| Certezas (C) | Suposições (S) | Dúvidas (D) |

| :--- | :--- | :--- |

| **C1.** O app deve melhorar a comunicação entre pessoas que usam CAA e interlocutores que não conhecem esses recursos. | **S1.** O celular (ou tablet) é o dispositivo principal tanto do usuário de CAA quanto do interlocutor. | **D1.** Existe necessidade de login? Que informações de caracterização seriam coletadas? |

| **C2.** O foco é o “outro lado da conversa”: ajudar o interlocutor leigo a entender pictogramas e mensagens do emissor. | **S2.** Interlocutores leigos conseguem entender a mensagem só com pictograma + texto + áudio, sem treinamento prévio. | **D2.** O app precisa funcionar sem internet? |

| **C3.** O público inclui usuários de CAA, familiares, cuidadores, professores, profissionais e pessoas não familiarizadas com CAA. | **S3.** Um conjunto de mensagens predefinidas por contexto atende às necessidades reais do usuário de CAA. | **D3.** Quais sistemas de pictogramas os usuários já conhecem e usam? |

| **C4.** Os cenários de uso são restaurantes, hospitais, escolas, transportes e outros ambientes do dia a dia. | **S4.** As respostas rápidas predefinidas bastam para o interlocutor responder. | **D4.** Quais apps de CAA são usados hoje, e vale integrar com eles no futuro? |

| **C5.** Os problemas centrais são: dificuldade de compreensão das mensagens, falta de familiaridade com pictogramas, interpretações equivocadas, dependência de terceiros e dificuldade de comunicação recíproca. | **S5.** O áudio é útil nos ambientes de uso, mesmo os barulhentos (restaurante, transporte). | **D5.** Quem é o usuário principal: crianças, adultos, idosos? Com quais deficiências? |

| **C6.** As prioridades do cliente são facilitar a compreensão, permitir respostas simples e rápidas, evitar falhas, dar controle ao usuário sobre sua expressão e promover autonomia. | **S6.** O usuário de CAA conseguirá confirmar, corrigir ou rejeitar a interpretação de forma autônoma. | **D6.** A interação acontece em um único aparelho (passado entre as pessoas) ou em dois aparelhos? |

| **C7.** O MVP terá: seleção de contexto, mensagens predefinidas (texto + pictograma), modo interlocutor simplificado, respostas rápidas, confirmação/correção/rejeição da interpretação, reprodução de áudio e interface para dispositivo móvel (ou similar). | **S7.** O app precisa de login/cadastro com informações de caracterização do usuário (consta na síntese). | **D7.** O interlocutor responde só com respostas rápidas ou também precisa de texto livre? |

| **C8.** Não há integrações externas definidas para o MVP. | **S8.** Os usuários de CAA têm perfis variados (idade, alfabetização, habilidade motora) que exigem diferentes níveis de adaptação. | **D8.** Quais mensagens são essenciais em cada contexto (restaurante, hospital, escola, transporte)? |

| **C9.** Os dados tratados são: mensagens selecionadas, respostas dos interlocutores, confirmações de entendimento e preferências de contexto. | **S9.** O app será usado em situações com pressa ou estresse (atendimento no hospital, fila), então precisa ser rápido. | **D9.** Quais cuidados de privacidade e segurança são necessários, principalmente em contextos de saúde? |

| — | — | **D10.** Que limitações dos dispositivos (tela, áudio, acessibilidade motora) podem afetar o uso? |

| — | — | **D11.** Como medir na prática “maior compreensão” e “menos falhas”? |

## 2. Detalhamento e Justificativa dos Pontos 📌

### Certezas 💡

- **C1 (Objetivo central do produto):** Confirmado no briefing como a motivação principal do projeto — preencher a lacuna comunicativa entre pessoas que utilizam Comunicação Aumentativa e Alternativa (CAA) e interlocutores que não conhecem esses recursos.

- **C2 (Diferencial e foco no interlocutor):** Estabelecido pelo cliente como o recorte estratégico da solução, direcionando o design não apenas para quem emite a mensagem, mas para tornar a leitura e a resposta imediatas para quem não domina CAA.

- **C3 (Atores e público-alvo):** Definido no levantamento inicial de envolvidos, abrangendo tanto os emissores (usuários de CAA) quanto sua rede de apoio (familiares, cuidadores, professores) e interlocutores externos (profissionais e pessoas não familiarizadas com CAA).

- **C4 (Contextos reais de aplicação):** Mapeado durante o briefing como os ambientes cotidianos onde ocorrem trocas comunicativas rápidas e funcionais (restaurantes, hospitais, escolas, transportes e outros ambientes do dia a dia).

- **C5 (Dores e gargalos atuais):** Relatado pelo cliente como o diagnóstico do problema atual: dificuldade de compreensão das mensagens, falta de familiaridade com pictogramas, interpretações equivocadas, dependência de terceiros e dificuldade de comunicação recíproca.

- **C6 (Critérios de prioridade):** Definido pelo cliente como norteador das decisões de design, priorizando facilitar a compreensão, permitir respostas simples e rápidas, evitar falhas, dar controle ao usuário sobre sua expressão e promover autonomia.

- **C7 (Escopo funcional do MVP):** Acordado no briefing como o conjunto mínimo de recursos necessários para validar a proposta em dispositivos móveis (seleção de contexto, mensagens predefinidas com texto + pictograma, modo interlocutor simplificado, respostas rápidas, confirmação/correção/rejeição da interpretação e reprodução de áudio).

- **C8 (Restrição de integração):** Confirmado como restrição técnica inicial — o MVP operará de forma independente, sem integrações externas definidas nesta primeira versão.

- **C9 (Escopo de dados):** Delimitado no briefing quanto às informações manipuladas durante o fluxo de uso (mensagens selecionadas, respostas dos interlocutores, confirmações de entendimento e preferências de contexto).

### Suposições 💭

- **S1 (Uso predominante de smartphones/tablets):** A equipe parte da premissa de que dispositivos móveis pessoais (celular ou tablet) são o meio principal tanto do usuário de CAA quanto do interlocutor. Precisa ser confirmado com o público-alvo.

- **S2 (Compreensão intuitiva sem treinamento):** Supõe-se que a combinação multimodal (pictograma + texto + áudio) seja suficiente para que um interlocutor leigo entenda a intenção do usuário sem treinamento prévio. Precisa ser testado na prática.

- **S3 (Suficiência das mensagens predefinidas):** Acredita-se que organizar mensagens predefinidas por contexto atenda às necessidades reais do usuário de CAA sem exigir construção complexa de frases.

- **S4 (Suficiência das respostas rápidas):** Supõe-se que botões de respostas rápidas predefinidas (ex.: *"Entendi"*, *"Aguarde um momento"*, *"Não temos"*) bastem para o interlocutor responder na dinâmica da conversa.

- **S5 (Eficácia do áudio em locais ruidosos):** Presume-se que a reprodução de áudio seja útil nos ambientes de uso, mesmo em locais barulhentos como restaurantes e transportes.

- **S6 (Autonomia no ciclo de validação):** A equipe supõe que o usuário de CAA conseguirá confirmar, corrigir ou rejeitar a interpretação do interlocutor de forma autônoma.

- **S7 (Necessidade de cadastro/perfil):** Embora o registro de caracterização do usuário tenha sido citado na síntese inicial, a equipe trata como suposição a real necessidade de login/cadastro frente ao uso imediato.

- **S8 (Heterogeneidade de perfis e adaptações):** Parte-se da hipótese de que perfis variados (idade, alfabetização e habilidade motora) exigirão diferentes níveis de adaptação na interface.

- **S9 (Uso sob pressão e restrição de tempo):** Supõe-se que o aplicativo será usado em situações com pressa ou estresse (como atendimento em hospital e filas), exigindo interação rápida.

### Dúvidas 🤔

- **D1 (Obrigatoriedade e escopo do login):** É preciso investigar se existe necessidade de login e quais informações de caracterização seriam coletadas sem criar barreira de entrada (conecta-se diretamente com `S7`).

- **D2 (Disponibilidade offline):** Importante para definir se o app precisa funcionar sem internet, já que hospitais, transportes e estabelecimentos podem ter sinal instável.

- **D3 (Padrões de pictogramas familiares):** Essencial para identificar quais sistemas de pictogramas (como ARASAAC, PCS, etc.) os usuários já conhecem e usam.

- **D4 (Ecossistema atual de apps de CAA):** Ajuda a entender quais apps de CAA são usados hoje e se vale a pena planejar integração com eles no futuro.

- **D5 (Recorte demográfico e clínico):** Fundamental para definir quem é o usuário principal (crianças, adultos ou idosos) e com quais deficiências ou necessidades específicas (conecta-se com `S8`).

- **D6 (Dinâmica física de uso do dispositivo):** Determina o modelo de interface — se a interação acontece em um único aparelho (passado entre as pessoas) ou em dois aparelhos distintos (conecta-se com `S1`).

- **D7 (Flexibilidade de resposta do interlocutor):** Necessário verificar se o interlocutor responde apenas com respostas rápidas ou se também precisa de campo de texto livre (conecta-se com `S4`).

- **D8 (Vocabulário prioritário por cenário):** Orienta a curadoria de quais mensagens são essenciais em cada contexto específico: restaurante, hospital, escola e transporte (conecta-se com `S3`).

- **D9 (Privacidade e dados sensíveis):** Crucial para definir quais cuidados de privacidade e segurança são necessários, principalmente em contextos de saúde.

- **D10 (Restrições de hardware e acessibilidade):** Permite mapear que limitações dos dispositivos (tamanho de tela, volume de áudio, acessibilidade motora) podem afetar o uso.

- **D11 (Métricas de sucesso da comunicação):** Necessário para definir como medir na prática os indicadores de “maior compreensão” e “menos falhas”.

## 3. Direcionamento para a Pesquisa com Usuários 🧷

<div align="justify">

As **Suposições** e **Dúvidas** levantadas nesta matriz foram agrupadas em quatro eixos de investigação para guiar o roteiro de entrevistas e questionários na etapa seguinte (`3-pesquisa-com-usuario.md`):

</div>

1. **Perfil, Acessibilidade e Ecossistema Atual (`S8`, `D3`, `D4`, `D5`, `D10`):** Investigar quem são os usuários principais (crianças, adultos ou idosos), quais aplicativos e sistemas de pictogramas já utilizam e quais barreiras motoras, visuais ou de dispositivo enfrentam.

2. **Dinâmica da Interação Presencial (`S1`, `S2`, `S5`, `S6`, `S9`, `D6`):** Compreender como ocorre a abordagem com interlocutores leigos em situações cotidianas e de pressa, verificando se a interação acontece em um único aparelho compartilhado ou em dois dispositivos e como o áudio e os pictogramas são recebidos.

3. **Conteúdo, Contextos e Reciprocidade (`S3`, `S4`, `D7`, `D8`):** Mapear as mensagens essenciais em restaurantes, hospitais, escolas e transportes, além de validar se respostas rápidas bastam ou se o interlocutor precisa de texto livre.

4. **Acesso, Privacidade e Funcionamento Técnico (`S7`, `D1`, `D2`, `D9`, `D11`):** Avaliar a necessidade de cadastro/login, a importância do uso sem internet e os cuidados de privacidade e segurança em contextos de saúde, bem como formas de medir maior compreensão e redução de falhas.
