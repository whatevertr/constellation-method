# Devlog — registro de conferência e correção

O que está publicado aqui muda quando a conferência manda. Este arquivo registra o que mudou, quando, e por quê — inclusive o que a minha própria conferência derrubou. Corrigir em público faz parte do método.

---

## 21/08/2026 — a conferência derrubou uma frase minha
O README dizia que o harness "move o resultado tanto quanto o próprio modelo". A fonte (Harness-Bench) não mede isso: mede o gap **entre harnesses** no mesmo modelo. Minha própria conferência cega (três juízes independentes) rebaixou a afirmação para insuficiente. A frase era maior que a evidência — corrigi para o que a fonte sustenta. O piso ("não afirmar o que não dá para verificar") vale principalmente contra mim.

*EN: my own blind review demoted a claim; the README now says what the source actually measures (a gap between harnesses, not harness vs. model).*

## 21/08/2026 — o absoluto virou decisão de engenharia
O MANIFESTO dizia "nenhuma defesa interna ao modelo é confiável". Isso alega uma impossibilidade que eu não provei (e há resultados de mitigação por inferência na literatura). A versão nova preserva a mesma decisão de projeto sem alegar o que não conferi — e torna explícito o porquê arquitetural: personalização pode amplificar concordância, então Manual e Função não moram no mesmo documento.

*EN: replaced an absolute ("no internal defense is reliable") with the engineering decision it always was; personalization and checking now explicitly live in separate documents.*

## 21/08/2026 — upgrade de citação + ressalva
O trabalho de Jain et al. sobre contexto de usuário e sycophancy saiu de preprint para publicação revisada (CHI 2026). Atualizei a referência, ajustei o número para "até +45% no caso medido" (topo da faixa, no Gemini 2.5 Pro; +33% no Claude Sonnet 4 e +16% no GPT 4.1 Mini para o mesmo tipo de contexto) e acrescentei que **o efeito não é universal**: dos cinco modelos testados no paper, o Llama 4 Scout não mostra mudança significativa com perfil de memória (só com interações do usuário), e o GPT 5.1 não mostra mudança significativa com nenhum dos dois contextos.

Um registro a mais, porque é o rastro mais valioso da rodada: uma conferência anterior tinha marcado "+33% Sonnet 4" e "+16% GPT 4.1 Mini" como inexistentes no paper; reabrir a fonte mostrou que existem (Abstract p. 2, §4.1 p. 8). A conferência corrigiu a própria conferência — é exatamente o erro que o piso existe para pegar.

*EN: Jain et al. citation upgraded to the peer-reviewed CHI 2026 version; the number was tightened to "up to +45% in the measured case" (top of the range, Gemini 2.5 Pro; +33% Claude Sonnet 4, +16% GPT 4.1 Mini for the same context type), and I added that the effect is not universal — of five tested models, Llama 4 Scout shows no significant change with memory profiles (only with user interactions) and GPT 5.1 shows no significant change with either. A note on the trail: an earlier check had marked "+33% Sonnet 4" and "+16% GPT 4.1 Mini" as absent from the paper; reopening the source showed they exist. The review corrected its own review — the kind of error the floor exists to catch.*
