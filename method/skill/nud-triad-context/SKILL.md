---
name: nud-triad-context
description: >-
  Use SEMPRE que o usuário quiser criar, montar ou preencher um "como trabalhar
  comigo", um "perfil de trabalho", documentos de contexto para colaboração
  humano-IA, ou a "Tríade de Contexto" (porta + manual + função). Acione
  também quando pedir para "montar meu contexto para IA", "ensinar a IA a
  trabalhar do meu jeito", "criar meu manual de uso", "perfil cognitivo de
  trabalho", ou quando trouxer um novo colaborador/instância e quiser gerar os
  documentos que orientam a relação de trabalho. A skill conduz uma
  entrevista curta de cerca de 15 perguntas — a maioria de múltipla escolha, as do
  projeto abertas — ou um único .md para preencher em lote, e entrega os cinco
  arquivos da Tríade mais um manual de uso em PDF.
  NÃO use para diagnóstico psicológico, teste de personalidade recreativo
  (MBTI/eneagrama) nem para avaliar terceiros sem a presença da pessoa.
license: CC-BY-4.0
metadata:
  author: Thainá Ramos (Nud by Whatevertr)
  version: 1.4.0
---

# Tríade de Contexto — gerador de "como trabalhar comigo"

**Versão 1.4.0 · 23.08.2026.** O manual de uso passou para a **via editorial arredondada** (lê melhor que a geometria reta quando o objetivo é explicar) e teve o claim suavizado para "princípios de psicologia cognitiva". Três acréscimos conceituais: a **decomposição funcional do contexto** (EU / TRABALHO / VOCÊ) foi nomeada, a **escada de alegações** (método → reproduzível → eficaz → generalizável) foi escrita, e o **link da frase de entrega** passou a apontar para o repositório do método, não para o perfil.

**Versão 1.3.0 · 17.08.2026.** Substitui a 1.2.0. **A entrevista deixa de depender de popup** e passa a ser em texto normal, para rodar em qualquer modelo. A contagem de perguntas foi corrigida (são ~15, não "uma dúzia"), a entrega do `manual_de_uso.pdf` foi propagada para o roteiro, e a bibliografia foi auditada. **A dimensão 7 foi reescrita:** ela agora fala de *preferência e eficiência de comunicação*, não de compreensão — a redação anterior contradizia a própria refutação dos estilos de aprendizagem que a skill cita. Com a origem corrigida, a Regra Universal que remendava isso saiu, e são **5** Regras Universais.

> **1.2.0 · 16.08.2026** — entrou o `manual_de_uso.pdf` como 6º entregável.

Esta skill produz a **Tríade** — 3 peças, entregues em **5 arquivos .md** — que ensinam qualquer instância de IA a colaborar com uma pessoa específica, com base **exclusivamente** em construtos da psicologia cognitiva validados por método científico:

1. **`comece_aqui`** — A PORTA. Onde a instância entra: objetivo do trabalho e para onde ir.
2. **`como_trabalhar_comigo`** — O MANUAL. Como a cabeça da pessoa funciona (7 dimensões validadas).
3. **A FUNÇÃO** — três **personas** que a pessoa pode usar: `worker` (executar), `thinker` (pensar), `manager` (conduzir). A skill **gera as três** como opções (não se pergunta qual papel — geram-se todas); **a pessoa escolhe qual usar** em cada tarefa (a instância que roda uma tarefa é UMA delas, não as três ao mesmo tempo). Os três arquivos têm o mesmo layout; muda só o bloco do papel.

**Por que três peças, e não um bloco só.** Elas separam o contexto pela *função* que ele exerce: o **EU** (o manual — quem é a pessoa), o **TRABALHO** (a porta — qual é a tarefa, com que objetivo e restrições) e o **VOCÊ** (a função — que ângulo a instância assume). É essa **decomposição funcional do contexto** que faz a Tríade ser menos um pacote de três arquivos e mais a menor unidade de um jeito de organizar contexto. Os nomes das camadas são para quem monta a Tríade; o usuário final nunca precisa ouvi-los (linguagem plana, sempre).

## Regra suprema — e o que ela governa
**Extremamente proibido inserir no PERFIL qualquer coisa não validada cientificamente.** As sete dimensões, os cenários e as frases prontas são o único material permitido para o **MANUAL** (`como_trabalhar_comigo`). Você **não** cria dimensões, **não** improvisa frases de perfil, **não** usa tipologias populares sem validade preditiva (MBTI, eneagrama, estilos de aprendizagem/VARK). Base científica em `referencias.md`.

**A FUNÇÃO é método, não ciência — e isso é declarado.** O piso epistêmico (🍷, colunas, jogo da moeda, conferência de piso) e os procedimentos do Manager (PDCA, 5 Porquês, 80/20) são **convenções de método** da Tríade, escolhidas por utilidade prática. Não são alegações sobre a pessoa e **não** se apresentam como validados por pesquisa. A distinção importa: a regra suprema existe para impedir que se invente psicologia sobre alguém — não para proibir procedimento de trabalho. **Nunca cite pesquisa para sustentar a FUNÇÃO.**

**Em que degrau o método está.** As alegações sobre o método sobem uma escada, e cada degrau pede mais evidência que o anterior: **método** (formalizado e aplicável) → **reproduzível** (terceiros repetem) → **eficaz** (avaliação mede o resultado) → **generalizável** (vale além da autora). A Tríade se declara no primeiro degrau: método formalizado, em uso diário, com reprodutibilidade e eficácia ainda em teste. Nomear a escada é o convite — quem quiser ajudar sabe qual degrau está vago.

## O usuário não conhece a skill
A pessoa **não sabe** o que está escrito aqui dentro. **Fale em linguagem plana**, como conversa normal. Nunca narre decisões internas em jargão ("Q2×Q3", "Object/Spatial", "leitura conjunta") nem fale como se ela conhecesse o método — aplique a lógica **em silêncio**. Detalhes em `regras/regras_de_preenchimento.md`.

## Como preencher (motor anti-interpretação)
O ponto onde um modelo mais erra é interpretar. Por isso o perfil é preenchido **só por múltipla escolha**: você faz uma pergunta-cenário, recebe UMA letra (A/B/C/D) e **cola a frase EXATA** correspondente — sem parafrasear. Mecanismo em **`regras/perguntas_e_frases.md`**.

- **Texto normal, uma pergunta por vez.** Escreva o enunciado e as opções no chat e espere a resposta. **Não dependa de popup nem de nenhum recurso de interface** — esta skill roda em qualquer modelo, não só no Claude. Se a resposta vier fora das letras, **aproxime à opção mais próxima** ou faça uma pergunta curta para aproximar. Não trave nem peça confirmação.
- **Perguntas imutáveis:** as 7 perguntas e suas opções são FIXAS. Não reescreva, não reordene, não invente. Alternativa só se a pessoa realmente não conseguir responder.

## Passo a passo (ordem clara — não se confunda)
1. **Leia** `regras/regras_de_preenchimento.md` e `regras/perguntas_e_frases.md` antes de começar.
2. **Abra com o roteiro fixo.** A redação canônica mora em `regras/regras_de_preenchimento.md` — **copie de lá**, não daqui. Existia uma segunda versão neste arquivo e as duas divergiam; agora há uma só.
3. **Conduza a entrevista, uma pergunta por vez, nesta ordem** (com "resposta → arquivo"):
   - **Q0a — nome da PESSOA** + **Q0b — como referir.** ⚠️ O nome da pessoa é diferente do **apelido da instância** (passo do QF). Não confunda.
   - **Q1 → Q7 (as 7 dimensões)** → alimentam SÓ o `como_trabalhar_comigo`.
   - **Perguntas do projeto** (objetivo prático, fundamentação, objetivo abstrato) → alimentam SÓ o `comece_aqui`. **Não pule.**
   - **QF-Tom + QF-Evitar** (múltipla escolha) → o tom dos três papéis.
   - **Apelido da instância (opcional)** → nome da IA. **Se a pessoa não quiser, fica sem apelido** (use "instância").
   - **Refinamento opcional:** se a pessoa marcou C ou D na Q7, pergunte se o apoio útil é exemplo/mockup ou diagrama de sistema.
   - **Nunca pergunte "qual é a função".**
4. **Preencha os arquivos** de `modelos/` colando as frases exatas:
   - `como_trabalhar_comigo.md` ← frases de REGRA (positivas) + NÃO-FUNCIONA (negativas) + as 5 Regras Universais.
   - `comece_aqui.md` ← respostas do projeto + versionamento + memória (`_memoria`).
   - `worker.md` / `thinker.md` / `manager.md` (espelhos) ← Worker e Thinker **derivados do manual** (positivo + negativo); Manager **fixo do método** + negativo; cada um com seu piso de papel. Base (tom + piso) idêntica nos três.
   - Cabeçalho de todos: `nome_do_arquivo — versão — DD/MM/AAAA` (versão no cabeçalho, não no nome).
   - Rodapé de todos: *"Gerado com a Tríade de Contexto — método de Thainá Ramos (Nud by Whatevertr) · https://github.com/whatevertr · Licenciado sob CC-BY-4.0."*
   - Nomes canônicos, sem nome de pessoa, sem versão no nome.
5. **Gere o manual em PDF** a partir de `modelos/manual_de_uso.html` (ver seção **"Manual em PDF"** abaixo). É o 6º arquivo entregue.
6. **Nunca infira gênero pelo nome** — use Q0b; na dúvida, só o nome.
7. **Entregue tudo numa resposta só:** os 5 `.md` **+ o `manual_de_uso.pdf`** **+ a frase de entrega** (`regras/frase_de_entrega.md`) juntos, **sem esperar aprovação** (esperar cria ruído). Feche com um convite leve: "se algo não te representar, me diz que eu ajusto". A pessoa pode **editar livremente** depois; você ajuda sem avisar nada sobre "regras".

## Manual em PDF (o 6º arquivo — sempre entregue junto)
Além dos 5 `.md`, a Tríade entrega um **`manual_de_uso.pdf`**: um mini-manual de **uma página**, no estilo NUD, na via editorial arredondada (**estado dia**, por ser peça para impressão), que explica o que é cada arquivo e como usá-los. O template já vem pronto e **autocontido** em `modelos/manual_de_uso.html`.

**Como gerar:**
1. Copie `modelos/manual_de_uso.html` para o diretório de trabalho e **substitua os três marcadores**: `[NOME]` (nome da pessoa), `[Vx]` (versão) e `[DD/MM/AAAA]` (data). Nada mais muda — o resto do manual é fixo.
2. **Renderize para PDF** com um navegador headless (Chrome ou Edge):
   ```
   chrome --headless=new --disable-gpu --no-pdf-header-footer --print-to-pdf="manual_de_uso.pdf" "file:///CAMINHO/manual_de_uso.html"
   ```
   No Windows o executável costuma ser `msedge.exe` ou `chrome.exe` em `Program Files`. O template já traz `print-color-adjust: exact`, então as cores do estado dia saem certas no PDF.
3. **Entregue o `manual_de_uso.pdf`** junto dos 5 `.md`, na mesma resposta.
4. **Fallback:** se nenhum navegador headless estiver disponível, entregue o `manual_de_uso.html` preenchido (abre no navegador e imprime como PDF pelo próprio usuário). Nunca deixe o manual de fora.

> Uma amostra renderizada (com os campos ainda como `[NOME]`) fica em `method/manual_de_uso_exemplo.pdf`, **um nível acima da skill** — serve só de referência visual para quem lê o repositório, não vai no pacote da skill nem é o arquivo final. (Ficava dentro da skill e pesava 42% do pacote sem a instância nunca usar; movido para fora em 17/08/2026, como o Rocky recomendou.)

## O que fica fixo (não se pergunta)
- O **piso epistêmico** (🍷, colunas observação/inferência/desconhecido, jogo da moeda, conferência de piso) já vem nos templates `modelos/worker.md`, `thinker.md`, `manager.md` — base idêntica + piso específico de cada papel.
- As **5 Regras Universais** já vêm no MANUAL. São o piso de boa prática — não preferência da pessoa. A 6ª saiu na 1.3.0: ela existia para remendar a redação antiga da dimensão 7, que foi corrigida na origem.

## Estrutura do pacote
```
nud-triad-context/
├── SKILL.md                       (este arquivo)
├── referencias.md                 (base científica — o compromisso de rigor)
├── LICENSE
├── modelos/
│   ├── comece_aqui.md             (PORTA)
│   ├── como_trabalhar_comigo.md   (MANUAL)
│   ├── worker.md                  (FUNÇÃO — papel Worker)
│   ├── thinker.md                 (FUNÇÃO — papel Thinker)
│   ├── manager.md                 (FUNÇÃO — papel Manager)
│   └── manual_de_uso.html          (template do MANUAL EM PDF — autocontido, só texto, uma página)
└── regras/
    ├── perguntas_e_frases.md      (motor: 7 cenários → frases prontas + QF + porta)
    ├── regras_de_preenchimento.md (roteiro da entrevista + avisos)
    └── frase_de_entrega.md        (mensagem final + assinatura)
```

---
© 2026 Thainá Ramos (Nud by Whatevertr) · https://github.com/whatevertr · Licenciado sob [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) — uso livre mediante atribuição.
