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
* Na **Versão B**, foi adicionado o botão `Pular` no topo superior direito de todas as telas introdutórias. Embora agilize o avanço, o botão pequeno no canto superior exige maior precisão motora e pode levar utilizadores iniciantes a saltar explicações importantes sobre o pareamento e o modo offline.
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
