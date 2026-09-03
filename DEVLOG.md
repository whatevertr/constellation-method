# Devlog — registro de mudança e correção

O que muda aqui, quando e por quê. Inclui o que a conferência derrubou, inclusive contra mim. Registro curto, sem narrativa.

---

## 02/09/2026 — três skills no lugar de uma, e a escala em pastas

**Mudou:** a skill única virou três, uma por peça da tríade. Entrou a tabela de onde configurar cada camada por plataforma, e uma prévia do modelo mínimo de fluxo de contexto em pastas. Os três perfis de agente ganharam guardrails e limite alinhado ao uso real. Saíram as ilustrações e o PDF de exemplo.

**Por quê:** cada peça precisa ser usável sozinha. A skill única obrigava a carregar as três para usar uma.

**O que a conferência derrubou:** a primeira montagem copiou os arquivos de regras inteiros para dentro de cada skill e acrescentou uma seção mandando a instância ignorar as partes que não eram dali. Instruir a ignorar não é separar. Refeita desmembrando os arquivos, cada skill com o trecho que é seu. A fidelidade das frases foi verificada por comparação byte a byte, não por leitura.

*EN: one skill became three, one per layer, so each can be used on its own. Added a table of where each layer is configured per platform, and a first sketch of the folder model. The three agent profiles gained guardrails and a realistic turn limit; illustrations and the sample PDF were removed. What the review rejected: the first build copied the rule files whole into each skill and told the instance to ignore what did not belong there. Instructing to ignore is not separating. Rebuilt by actually splitting the files; sentence fidelity verified by byte-level comparison, not by reading.*

## 21/08/2026 — uma frase minha, maior que a evidência

**Mudou:** o README dizia que o harness "move o resultado tanto quanto o próprio modelo". Corrigido para o que a fonte sustenta.

**Por quê:** Harness-Bench mede o gap **entre harnesses** no mesmo modelo, não harness contra modelo. Conferência cega (três juízes independentes) rebaixou a afirmação para insuficiente.

*EN: my own blind review demoted a claim; the README now says what the source actually measures (a gap between harnesses, not harness vs. model).*

## 21/08/2026 — um absoluto virou decisão de engenharia

**Mudou:** o MANIFESTO dizia "nenhuma defesa interna ao modelo é confiável". A versão nova preserva a decisão de projeto sem alegar impossibilidade.

**Por quê:** era uma alegação que eu não provei, e há resultados de mitigação por inferência na literatura. O porquê arquitetural fica explícito: personalização pode amplificar concordância, então Manual e Função não moram no mesmo documento.

*EN: replaced an absolute ("no internal defense is reliable") with the engineering decision it always was; personalization and checking now explicitly live in separate documents.*

## 21/08/2026 — citação atualizada e ressalva acrescentada

**Mudou:** Jain et al. saiu de preprint para publicação revisada (CHI 2026). O número virou "até +45% no caso medido" (topo da faixa, Gemini 2.5 Pro; +33% Claude Sonnet 4; +16% GPT 4.1 Mini). Acrescentada a ressalva de que o efeito não é universal: dos cinco modelos testados, o Llama 4 Scout não muda significativamente com perfil de memória e o GPT 5.1 não muda com nenhum dos dois contextos.

**Por quê:** citar o número de topo sem a faixa e sem as exceções é overclaim.

**O que a conferência derrubou:** uma conferência anterior marcou "+33% Sonnet 4" e "+16% GPT 4.1 Mini" como inexistentes no paper. Reabrir a fonte mostrou que existem (Abstract p. 2, §4.1 p. 8). A conferência corrigiu a própria conferência.

*EN: Jain et al. citation upgraded to the peer-reviewed CHI 2026 version; the figure is now "up to +45% in the measured case" (top of range, Gemini 2.5 Pro; +33% Claude Sonnet 4; +16% GPT 4.1 Mini), with the caveat that the effect is not universal. An earlier check had marked two of those figures as absent from the paper; reopening the source showed they exist. The review corrected its own review.*
