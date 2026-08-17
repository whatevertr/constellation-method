# Regras de preenchimento — como a instância conduz a entrevista
*Instância: siga este roteiro à risca. Objetivo: preencher os **5 `.md`** da Tríade (porta + manual + 3 papéis) — e entregar junto o **`manual_de_uso.pdf`**, o 6º arquivo (procedimento na seção "Manual em PDF" do `SKILL.md`) — com o mínimo de perguntas e **zero interpretação sua** nas dimensões de perfil.*

---

## Princípio inegociável
**Extremamente proibido inserir no perfil qualquer coisa que não esteja validada por método científico.** As sete dimensões e as frases prontas em `perguntas_e_frases.md` são o único material permitido para o MANUAL. Você não cria dimensões novas, não improvisa frases de perfil, não puxa "tipos de personalidade" populares (MBTI, eneagrama, estilos de aprendizagem/VARK — todos sem validade preditiva).

## O usuário NÃO conhece a skill (regra forte)
A pessoa do outro lado **não sabe** o que está escrito aqui dentro — não conhece as dimensões, os nomes das perguntas (Q1, Q2…), "leitura conjunta", "Object/Spatial", nem o método. **Fale com ela em linguagem plana, como uma conversa normal.** Nunca:
- narre suas decisões internas em jargão ("marquei Q2×Q3", "Q7=B, não há refinamento Object/Spatial") — aplique a lógica **em silêncio**;
- fale como se a pessoa tivesse criado a skill ou conhecesse as regras;
- exponha "notas de montagem" com termos do método.
Se precisar explicar algo, traduza para o mundo dela ("montei teu perfil; se algo não bater, me fala").

## Passo a passo da entrevista (uma pergunta por vez — NÃO se confunda)
Siga esta ordem exata. Ao lado de cada passo, **qual arquivo aquela resposta alimenta** — não misture.

1. **Abertura (roteiro fixo — diga assim, sem inventar):** "Vou te fazer cerca de 15 perguntas curtas, a maioria de múltipla escolha, para montar 5 documentos que ensinam qualquer IA a trabalhar do seu jeito — mais um manual em PDF explicando cada um deles. Não há resposta certa — escolha o que mais parece você na maioria dos dias."
   *Esta é a **redação canônica** da fala de abertura. Se outro arquivo trouxer uma versão diferente, vale esta.*
2. **Q0a — o NOME da PESSOA.** "Como você quer ser chamada?" → grava `{NOME}`. **Atenção: este é o nome da PESSOA (a humana), não o apelido da IA.** Não confunda os dois.
3. **Q0b — como referir** (nome / ela / ele / elu). → alimenta o MANUAL e a função.
4. **Q1 → Q7 — as 7 dimensões**, uma de cada vez, esperando a letra. → alimentam **SÓ** o `como_trabalhar_comigo` (o MANUAL).
5. **Perguntas do projeto** (objetivo prático, fundamentação teórica, objetivo abstrato) — abertas, são sobre o trabalho. → alimentam **SÓ** o `comece_aqui` (a PORTA). **Não pule este passo:** sem ele, a porta fica vazia.
6. **QF-Tom** (múltipla escolha) + **QF-Evitar** (múltipla escolha). → alimentam o **tom** dos três papéis.
7. **Apelido da INSTÂNCIA (opcional).** "Quer dar um apelido pra mim (a IA)?" → é o nome da IA, **diferente do nome da pessoa** (passo 2). **Se a pessoa não quiser apelido, a instância fica simplesmente sem apelido** — não invente um.
8. (Opcional) refinamento Object/Spatial se a pessoa marcou C/D na Q7.
9. **Nunca pergunte "qual é a função".** Gere as três personas (worker, thinker, manager) como opções; a pessoa escolhe qual usar depois.

> **Nome da pessoa × apelido da instância — a confusão a evitar:** `{NOME}` (passo 2) é a humana; o apelido (passo 7) é a IA. No jogo da moeda o placar é "`{NOME}` X, `{APELIDO}` Y". Se não houver apelido, use "instância" no lugar.

## Formato das perguntas (texto puro) e imutabilidade
- **Uma pergunta por vez, sempre, em texto normal no chat — nunca em bloco.** Toda pergunta é feita direto no chat, uma de cada vez: enuncie, espere a resposta, só então vá à próxima. **Nunca despeje várias perguntas juntas.** As 7 dimensões e as QF são de **múltipla escolha** (a pessoa responde com a letra); as 3 perguntas da porta são **abertas**.
- **Resposta fora das letras — flexibilize.** Se a pessoa responder algo que não é uma das letras, **aproxime a resposta à letra mais próxima**; se não conseguir, **faça outra pergunta curta** para aproximar. Não trave nem peça confirmação.
- **Imutabilidade.** As 7 perguntas e suas opções são **FIXAS**. Não reescreva, não reordene, não invente. Alternativa só em **último caso**, quando a pessoa genuinamente não consegue responder.
- *(Alternativa opcional: se a pessoa preferir responder tudo de uma vez, entregue o questionário como um único `.md` para preencher e devolver — avisando que é para economizar tokens.)*

## Como transformar respostas em documentos
- **MANUAL (`como_trabalhar_comigo`).** Para cada letra, **copie a frase de REGRA** (seção positiva) e a de **NÃO-FUNCIONA** (seção negativa). Troque só `{NOME}` e `{PRON_*}`. Some as 5 Regras Universais.
- **PORTA (`comece_aqui`).** Preencha com as respostas do projeto (passo 5).
- **FUNÇÃO — 3 arquivos espelhos (`worker`, `thinker`, `manager`).** Mesma estrutura nos três; muda só o específico:
  - **Tom** e **piso-base** (colunas, conferência de piso, princípios da taça e do jogo da moeda): **idênticos** nos três.
  - **Worker e Thinker — conduta (positivo) e negativo DERIVADOS do MANUAL preenchido:** reagrupe as frases das dimensões por etiqueta ([WORKER] = Q2/Q3/Q4/Q7 + Universais; [THINKER] = Q1/Q5/Q6/Q4 + Q2 se polo baixo). O **negativo** é a função oposta que causa mais atrito (as frases de NÃO-FUNCIONA das mesmas dimensões). **Não deixe `[a preencher]` — derive de verdade.**
  - **Manager — positivo FIXO do método + negativo:** o texto canônico (piso de qualidade; PDCA para planejar→delegar→conferir; 80/20 condicional; 5 Porquês; decide Thinker vs Worker), ancorado ao perfil em 1 linha; o negativo são os anti-padrões do Manager.
  - **Piso de cada papel** (alvo da taça + árbitro da moeda + "falhou se"): já vem nos templates `modelos/worker.md`, `thinker.md`, `manager.md`.
  - Aplique a **leitura conjunta Q2×Q3** no papel onde couber (Worker/Manager).
- **Tom não declarado.** Se a pessoa não declarar tom, registre **"sem preferência declarada — padrão da instância"**. Não invente.
- **Cabeçalho de todos:** `nome_do_arquivo — versão — DD/MM/AAAA` (a versão mora aqui, não no nome do arquivo).
- **Rodapé de todos (regra):** toda saída leva o rodapé *"Gerado com a Tríade de Contexto — método de Thainá Ramos (Nud by Whatevertr) · https://github.com/whatevertr · Licenciado sob CC-BY-4.0."*
- **Nomeação dos arquivos.** Apenas nomes canônicos, **sem nome de pessoa** e **sem versão no nome**: `comece_aqui`, `como_trabalhar_comigo`, `worker`, `thinker`, `manager`. Total: **5 `.md`** — mais o **`manual_de_uso.pdf`**, que fecha a entrega em **6 arquivos**.

## Cuidados de linguagem
- **Nunca infira gênero pelo nome.** Use Q0b. Na dúvida, só o nome.
- Mantenha as frases sem adjetivo de gênero (já vêm assim).
- Escreva tudo **na linguagem para a instância** — como alguém explicando a outra IA onde começar, como é a pessoa e qual é o papel.

## Pré-registro do "preenchimento-válido" (anti-ad-hoc)
Defina — **por escrito e antes** — o que conta como **preenchimento-válido** (ex.: respondeu a MC pura em Q1–Q7, na primeira leitura, sem ajuda). **Um resultado ruim com preenchimento válido conta contra o método** — não vale desqualificar depois dizendo que "preencheu errado". O critério é fixado antes.

## Conferência de piso (falseabilidade obrigatória)
Todo piso epistêmico — a taça 🍷, o jogo da moeda, as colunas — precisa de um **"falhou se…" falseável escrito ANTES do uso**. Piso sem critério de falha é **decoração**. Confira que cada piso carrega sua condição de falha.

## Entrega (tudo numa resposta só — não espere aprovação)
Assim que os **5 `.md`** estiverem prontos, gere o **`manual_de_uso.pdf`** (o 6º arquivo — procedimento na seção **"Manual em PDF"** do `SKILL.md`; não repita o procedimento aqui) e entregue os **6 arquivos junto com a frase de entrega** (`frase_de_entrega.md`) na **mesma resposta**. **Não** espere a pessoa "aprovar" para mandar a frase de entrega — esperar cria ruído (ela só apareceria se a pessoa mandasse outra mensagem). Feche com um convite leve, em linguagem plana:
> "Dá uma olhada. Se algo não te representar, me diz qual e o que não ficou que eu ajusto — do jeito que for melhor pra você."

A pessoa **pode editar os arquivos livremente** depois, mesmo fora das regras; e você **ajuda sem precisar avisar nada** sobre "regras" ou "pesquisa".

## As Regras Universais (para colar no MANUAL)
São **5**, já redigidas na seção "Regras que valem sempre" do modelo `como_trabalhar_comigo.md`. Não vêm de perguntas — aplicam-se a todos.

| Regra | Âncora |
|---|---|
| 1 · estrutura e sinalização | carga cognitiva (Sweller) |
| 2 · fatiar e externalizar | memória de trabalho (Conway et al.) |
| 3 · reduzir andaimes com a experiência | expertise reversal (Kalyuga) |
| 4 · registrar em vez de confiar na lembrança | memória autobiográfica (Palombo et al.) |
| 5 · começar pelo essencial | *(ver `referencias.md`)* |

> A 6ª regra — sobre preferência de formato não ser modo de aprender — **saiu na 1.3.0**. Ela remendava a redação antiga da dimensão 7, que agora fala de preferência e eficiência, não de compreensão. A refutação dos estilos de aprendizagem (Pashler et al.) continua em `referencias.md` como o motivo de eles estarem fora da skill.
