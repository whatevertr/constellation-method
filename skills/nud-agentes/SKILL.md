---
name: nud-agentes
description: >-
  Use quando o usuário pedir os perfis prontos de papel da IA (thinker,
  manager, worker), "agentes" para trabalhar com ele, um
  "contrato" de função da instância, ou perguntar como dividir o trabalho
  com a IA em pensar/conduzir/executar; use também quando o usuário pedir "o
  método NUD" ou "a tríade de contexto" e não souber por onde começar. Acione
  também quando o usuário mencionar a "Tríade de Contexto" e quiser
  especificamente os três papéis worker/thinker/manager (não o perfil da
  pessoa (para isso, use `nud-como-trabalhar-comigo`) e não a porta do
  projeto (para isso, use `nud-comece-aqui`).
license: CC-BY-4.0
metadata:
  author: Thainá Ramos (Nud by Whatevertr)
---

# nud-agentes

Esta skill entrega os três perfis de agentes, `thinker` (pensar), `manager` (conduzir) e `worker` (executar), e explica como trabalhar com eles. Ela não faz perguntas nem personaliza: os arquivos em `modelos/` são entregues como estão.

O método usa três documentos, cada um cobrindo uma função de contexto diferente:

- `start_here` (skill `nud-comece-aqui`): o TRABALHO, qual é a tarefa, com que objetivo.
- `how_to_work_with_me` (skill `nud-como-trabalhar-comigo`): a PESSOA, como a cabeça dela funciona.
- os três arquivos de papel, entregues por esta skill: o ÂNGULO que a instância assume, worker, thinker ou manager.
### Método proposto

**A FUNÇÃO é método para estabelecer o terreno comum.** O piso epistêmico (🍷, colunas, jogo da moeda, conferência de piso) e os procedimentos do Manager (PDCA, 5 Porquês, 80/20) são **convenções de método** da Tríade, escolhidas por utilidade prática. Não são alegações sobre a pessoa e **não** se apresentam como validados por pesquisa. A distinção importa pois não é diagnóstico de psicologia sobre alguém.

É essa **decomposição funcional do contexto** que faz a Tríade ser menos um pacote de três arquivos e mais a menor unidade de um jeito de organizar contexto.

A decomposição facilita a manutenção: o `start_here` pode ser reutilizado para contextualizar rapidamente novos projetos; o `how_to_work_with_me` deve ser atualizado para refletir as mudanças comportamentais do usuário conforme ele muda; e os agentes podem ser invocados com facilidade, pois estão instalados na skill.

## Direcionamento

Para entender melhor a aplicação da tríade ou o escalonamento do método, acesse os links do repositório e do tumblr (no fecho desta skill).

## Como trabalhar com os três perfis

1. **Entregue os três arquivos de `modelos/` como estão** (`worker.md`, `thinker.md`, `manager.md`). Não preencha, não personalize, não faça perguntas. Entregue os três sempre; nunca pergunte "qual papel usar".
2. **Pergunte à pessoa onde salvar os três arquivos**, ou oriente a salvar na área dedicada do projeto.
3. **Explique, em linguagem plana, que ela escolhe UM papel por tarefa** (a instância que roda uma tarefa é UMA delas, não as três ao mesmo tempo).
4. **Aponte o bloco "Guardrails próprios"** no fim de cada arquivo: é ali que a pessoa acrescenta as regras do ambiente dela (pastas que não devem ser tocadas, comandos proibidos, limites de custo).

## Onde os documentos vivem e como são lidos

**Em espaços dedicados a arquivos do projeto dentro do app do provedor da IA:** ele não funciona sozinho, é preciso pedir à instância que o leia no início do trabalho. Vale guardar e atualizar um arquivo de memória do projeto, é o que permite retomar o trabalho sem reler tudo do zero.

**Em espaços dedicados no seu computador, pasta de projetos/repositórios:** funciona se traduzida conforme a configuração descrita em https://github.com/whatevertr/constellation-method.

NUD recomenda usar os três documentos.

---
Para entender melhor ou se aprofundar, repositório: https://github.com/whatevertr/constellation-method & tumblr: https://tumblr.com/nerdunitdescription
