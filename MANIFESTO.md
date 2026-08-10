# Manifesto — Constellation Method

Eu ainda estava no início da minha jornada com grandes modelos de linguagem, principalmente Anthropic e OpenAI, em tarefas do dia a dia: análise de dados, auditorias, desenvolvimento de conteúdo. E um obstáculo técnico me incomodava sempre: os riscos visíveis de **alucinação** e de **_sycophancy_** (a tendência da IA a concordar com o usuário só para agradá-lo). Isso destruía a previsibilidade e a confiança nas entregas.

Essa dor virou curiosidade. Entrei numa _sidequest_ para mapear a causa-raiz dos acertos: **investiguei por que a IA acertava, não por que errava.** De forma totalmente intuitiva, caí na cadeira emergente da **Engenharia de Contexto**, percebendo como a estrutura e a governança das informações moldam diretamente a performance do modelo. Foi assim que criei a minha **Tríade de Documentos**, antes de fazer qualquer pesquisa teórica formal.

Ao notar o salto de precisão que a Tríade trouxe, fui investigar os porquês científicos, e assumo um cuidado: estudo o comportamento dos modelos para não implementar solução já descartada. Dois achados moldaram a estrutura. Primeiro, a _sycophancy_ **não diminui** com modelos melhores; ela cresce com a escala e com mais treino por feedback humano (Perez et al., 2022). Segundo, dar à IA um perfil seu na memória **amplifica** a bajulação (+45% de concordância no caso medido; Jain et al., 2025). A conclusão de projeto é direta: se o viés nasce no próprio objetivo de treino, nenhuma defesa interna ao modelo é confiável, e a proteção precisa ser **estrutura fora do modelo**. É o que a Tríade faz de forma barata, e é o que estou escalando no harness permanente do meu método.

Como a minha área-mãe é a **Engenharia de Produção**, percebi que o que eu tinha construído era, na verdade, um **_harness_** industrial adaptado para o software, aplicando conceitos consolidados: **Poka-Yoke** (blindar o erro pela estrutura, não pela força de vontade) e **PDSA** (melhoria contínua por _estudo_, não por inspeção).

E há um movimento que o mercado começa a enxergar: quanto mais os modelos melhoram, mais a **estrutura em volta deles** pesa no resultado. Uma medição recente mostra o mesmo modelo variando dezenas de pontos só pela troca do harness (Harness-Bench, 2026, com a ressalva de _preprint_). Montar um harness é montar um contexto, que é montar um **fluxo de trabalho**. E criar ou corrigir fluxos para que fiquem seguros e mais eficientes é justamente o que o meu olho de engenheira é treinado para fazer.

Desenvolvi essa estrutura com foco em **auto-aprimoramento** e a valido diariamente via **_dogfooding_**: sou a usuária número um do meu próprio método. Agora abro o projeto como proposta _open-source_ e **hipótese de solução**, e convido especialistas e pesquisadores a testarem esse _framework_ comigo, com ferramentas de medição de verdade, para levá-lo ao limite.

🍷O futuro da tecnologia não está só nos modelos brutos: está na **Engenharia de Contexto**. A IA vai ser a memória do trabalhador do futuro, e governar essa relação é a profissão que eu quero construir.

---
*Documento vivo. A trilha de commits deste repositório é o registro datado da sua evolução.*
