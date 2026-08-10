<p align="right"><a href="README.md">🇺🇸 English</a></p>

# Método Constelação

Um harness leve, de três arquivos, para trabalhar com uma IA em tarefas longas sem perder o fio entre sessões. São três documentos que você preenche uma vez e a instância lê no começo de cada sessão.

> **O que é isto.** Pesquisa de auto-aprimoramento e de infraestrutura própria, validada em uso diário (_dogfooding_). Propor uma arquitetura nova e disponibilizá-la em público como forma legítima de gerar conhecimento, então abro esta como **hipótese de solução:** fundamentada, ainda não testada em escala, construída à vista. A trilha de commits é o registro datado da evolução.

---

## O problema

Trabalho longo com IA tem uma falha recorrente. A cada sessão nova, ou a cada reset de contexto, a instância esquece quem você é (mas as vezes não é perceptível), o que importa agora e como você trabalha, e você recomeça explicando tudo, e quando você não percebe que ela te esqueceu, ou esqueceu o objetivo, bom... Você vai descobrir só no meio da produção, aposto que vc já teve retrabalho ou gasto de tokens por isso. Pior: sem regras explícitas, o modelo tende a concordar com você **(bajulação)** e a preencher lacuna com palpite plausível em vez de dizer **"não sei"**.

Isso **não é um vício que se conserta esperando o próximo modelo**, porque a bajulação é produto previsível do treino por preferência humana e não diminui conforme os modelos melhoram (ver [Referências](#referências)). A conclusão é direta: já que o viés nasce no objetivo de treino, a defesa precisa ser estrutura **fora** do modelo.

O método monta o contexto em camadas antes de qualquer tarefa: o que é o projeto, como a sua cabeça funciona, e a postura epistêmica que a instância carrega. O estado do trabalho vive na memória.md que sobrevive ao reset. Você para de recomeçar do zero, e ganha eficiência. Os meus costumam lembrar do que eu tenho que fazer melhor do que eu 😏.

## A tríade: o harness mínimo

O ponto de entrada são três arquivos, três camadas:

- **a porta** (`comece_aqui`): onde a instância entra. O tema, a prioridade viva agora, e para onde ir em seguida.
- **o manual** (`como_trabalhar_comigo`): como a sua cabeça funciona. Os seus critérios de colaboração, escritos por você.
- **o contrato** (`a função`): como você quer que a instância seja. O ângulo dela e o piso epistêmico que não muda. Três funções prontas (thinker, worker, manager), uma por tarefa.

São três arquivos que executam os quatro movimentos canônicos de contexto: escrever, selecionar, comprimir, isolar. É o mínimo que já funciona.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/triad_nud_noite.svg">
  <img alt="A tríade: as três camadas do harness mínimo" src="assets/triad_nud_dia.svg">
</picture>

## Como cheguei ao harness

A tríade não nasceu pronta, foi destilada no uso ao longo de muitas instâncias. Cada sala testou uma peça, e o que sobrevivia à conferência ficava, porque sem um padrão estável não há como saber o que causou a melhora. Este mapa é a trilha do percurso, da primeira instância sem contexto até a estrutura de hoje:

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/mapa_cronologico_noite.svg">
  <img alt="Método Constelação: a trilha até o harness, ao longo do tempo" src="assets/mapa_cronologico_dia.svg">
</picture>

## O harness: onde eu trabalho agora

O que começou como três arquivos cresceu na estrutura que passo a operar a partir daqui: um cronista central que organiza e mantém o rastro, contextos isolados por assunto (uma sala não enxerga a outra), memória conectada que sobrevive ao reset, e uma parede entre o público e o privado. Este é o projeto do harness, a arquitetura completa:

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/harness_desenho_definitivo_noite.svg">
  <img alt="O harness completo do Constellation: a arquitetura" src="assets/harness_desenho_definitivo_dia.svg">
</picture>

## As regras epistêmicas

Duas peças carregam a honestidade do método, e as duas são estrutura, não força de vontade:

- **A taça 🍷**: a instância (e você) marca em uma linha o que percebe mas não consegue verificar. O não-conferido fica nomeado, não escondido.
- **O jogo da moeda**: a cada troca, você sinaliza certo ou errado e a instância aposta se o seu sinal foi sincero. São duas conferências, uma de cada lado. Isso desarma a bajulação porque a estrutura obriga a aposta, em vez de deixar o modelo apenas absorver o seu feedback.

## Em que ele se apoia

O método se lê como PDSA aplicado a contexto. A Engenharia de Produção dá o método (trabalho padronizado, poka-yoke, PDSA, desvio positivo), e duas frentes de pesquisa dão o embasamento:

- **Engenharia de Contexto**: o contexto é um orçamento finito com geometria, porque o modelo usa bem o começo e o fim da janela e perde o meio, e o harness em volta do modelo move o resultado tanto quanto o próprio modelo. Uma medição recente registra o mesmo modelo variando dezenas de pontos só pela troca do harness ([Harness-Bench, 2026](https://arxiv.org/abs/2605.27922), _preprint_).
- **Comportamento do modelo**: a bajulação é produto do treino por preferência humana ([Sharma et al., 2023](https://arxiv.org/abs/2310.13548)), aumenta com escala e mais RLHF ([Perez et al., 2022](https://arxiv.org/abs/2212.09251)), e um perfil do usuário na memória a amplifica (+45% de concordância no caso medido; [Jain et al., 2025](https://arxiv.org/abs/2509.12517)).

O texto formal, a tese, vem depois, à medida que a pesquisa firma.

## Como usar

1. Gere os seus três arquivos. O caminho mais rápido é a skill que acompanha o método, que entrevista você e preenche a tríade. Para preencher na mão, copie as versões em branco em [`method/templates/`](method/templates/); e, já que a tríade rende com capricho, ajuda pedir para um chat de contexto longo preencher com você.
2. Ponha os três na raiz do seu espaço de trabalho e peça para a instância lê-los antes de qualquer tarefa.
3. Mantenha um arquivo de memória **por projeto**, para o estado sobreviver ao reset. Evite uma memória global ativa, porque ela mistura o contexto entre projetos, que é justamente o oposto do isolamento que o método busca.

## Referências

- Anthropic — *Effective context engineering for AI agents* (2025).
- Liu et al. — *Lost in the Middle* (2023), [arXiv:2307.03172](https://arxiv.org/abs/2307.03172).
- Yao et al. — *Harness-Bench* (2026, preprint), [arXiv:2605.27922](https://arxiv.org/abs/2605.27922).
- Sharma et al. — *Towards Understanding Sycophancy in Language Models* (2023), [arXiv:2310.13548](https://arxiv.org/abs/2310.13548).
- Perez et al. — *Discovering Language Model Behaviors with Model-Written Evaluations* (2022), [arXiv:2212.09251](https://arxiv.org/abs/2212.09251).
- Jain et al. — *Interaction Context Often Increases Sycophancy in LLMs* (2025), [arXiv:2509.12517](https://arxiv.org/abs/2509.12517).

## Licença

- **Método, templates e textos:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), use, adapte e compartilhe, inclusive comercialmente, com atribuição.
- **Qualquer código ou script:** MIT.

## Construído em público

Isto evolui ao vivo. A trilha de commits é o registro de campo, datado e versionado, e o que você vê é o estado atual, não um produto fechado. Contribuições e replicações são bem-vindas, e o processo de submissão entra numa rodada seguinte.
