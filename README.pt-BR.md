<p align="right"><a href="README.md">🇺🇸 English</a></p>

# Método Constelação

Três arquivos que você preenche uma vez, pra uma IA não perder o fio entre sessões. A instância lê os três no começo de cada sessão e já sabe quem você é, o que importa agora e como você trabalha.

> **A forma como eu uso** tem funcionado bem e, eu gosto de organizar estruturas, resolvi documentar a minha, enquanto estudo e vou melhorando.

---

## O problema

A cada sessão nova, ou reset de contexto, a instância esquece quem você é, o que importa agora e como você trabalha, e você recomeça do zero. Pior: sem regras explícitas, o modelo tende a **concordar com você (bajulação)** e a preencher lacuna com palpite plausível em vez de dizer **"não sei"**, ou rejeitar o erro produzido. E às vezes você só descobre no meio da produção, com retrabalho e token gasto.

A bajulação **não é um vício que se conserta esperando o próximo modelo**: ela é produto previsível do treino por preferência humana e não diminui conforme os modelos melhoram (ver [Referências](#referências)). Já que nasce no objetivo de treino, eu **escolho** montar a defesa como estrutura **fora** do modelo, em vez de contar que ele se autovigie sozinho.

O método monta o contexto em camadas antes da tarefa: o que é o projeto, como a sua cabeça funciona, e a postura que a instância carrega. O estado do trabalho vive numa `memoria.md` que sobrevive ao reset. Você para de recomeçar do zero. (Os meus costumam lembrar do que eu tenho que fazer melhor do que eu 😏.)

Agora as interfaces já estão implementando seus gatilhos de salvar na memória dentro da pasta do app, recente eu vi acontecer na minha frente, mas ainda assim, eu ainda acho que para garantir conferências limpas, precisa separar o contexto até no nível da memória, então... Tem uma manutenção pra fazer quando o gerenciamento é em interface e não via terminal kkkk não faço ideia do trabalho que dá pra fazer isso via terminal.

## A tríade: o mínimo que eu uso

Três arquivos, três camadas:

- **a porta** (`comece_aqui`): onde a instância entra. O tema, a prioridade de agora, e pra onde ir em seguida.
- **o manual** (`como_trabalhar_comigo`): como a sua cabeça funciona. Os seus critérios de colaboração, escritos por você.
- **a função** (`method/agents/`): que papel a instância assume. Três perfis prontos e genéricos, **thinker**, **manager**, **worker**, um por tarefa, cada um com o piso epistêmico que não muda.

🍷Seria um mínimo para começar a fazer tarefas mais complexas de forma mais rápida.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/triad_nud_noite.svg">
  <img alt="A tríade: as três camadas do método" src="assets/triad_nud_dia.svg">
</picture>

## Como cheguei aqui

A tríade não nasceu pronta, foi destilada no uso ao longo de muitas instâncias. Eu observava, mudava, testava, conferia, nada muito elaborado, fui mapeando pelo comportamento. Este mapa é a trilha do percurso, da primeira instância sem contexto até a estrutura da tríade:

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/mapa_cronologico_noite.svg">
  <img alt="Método Constelação: a trilha ao longo do tempo" src="assets/mapa_cronologico_dia.svg">
</picture>

## Pra onde estou indo (ainda um esboço)

O desenho maior abaixo, um cronista central que mantém o rastro, salas isoladas por assunto (uma não enxerga a outra), memória consistente, é onde estou trabalhando hoje e colocando aqui aos poucos, um esboço da arquitetura, é o modelo de interface que eu gostaria de ter. Se tiver alguém querendo construir, seria interessante.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/harness_desenho_definitivo_noite.svg">
  <img alt="O desenho maior (esboço): a arquitetura pretendida" src="assets/harness_desenho_definitivo_dia.svg">
</picture>

## As regras que carregam a honestidade

Duas peças, e as duas são estrutura, não força de vontade:

- **A taça 🍷**: a instância (e você) marca em uma linha o que percebe mas não consegue verificar. O não-conferido fica nomeado, não escondido.
- **O jogo da moeda**: a cada troca, você sinaliza se o que veio estava certo ou errado, e a instância já tinha apostado nisso. É uma redundância de conferência sobre o contexto do que está sendo pedido ou reportado.

  > **Exemplo concreto.** A instância aposta antes de terminar ou antes de conferir: *"aposto que X vai precisar de ajuste"*. Depois de conferir, ela pontua: *"não precisou de ajuste, não pontuei"*. É um jeito criativo de pedir conferência sobre o que ela mesma concluiu, tentando circundar a sycophancy em vez de proibi-la. Não afirmo que resolve: numa conversa de trabalho, onde o modelo ajuda com análise e pesquisa, a linha entre conferência sincera e concordância é tênue demais. É uma tentativa, não uma prova. 

## Em que eu me apoio

Eu não estou inventando disciplina nova: estou **traduzindo** prática velha de engenharia pra um meio novo. Minha área é **Engenharia de Produção**, e uso dois conceitos dela, em português simples:

- **Poka-Yoke**: evitar o erro pela estrutura, não pela energia do sistema.
- **PDSA**: melhorar estudando o resultado, não só inspecionando no fim.

E sobre a ideia de que "a estrutura em volta do modelo move o resultado": há medição registrando o mesmo modelo variando dezenas de pontos **de uma estrutura pra outra** ([Harness-Bench, 2026](https://arxiv.org/abs/2605.27922), _preprint_). E a bajulação é produto do treino por preferência humana ([Sharma et al., 2023](https://arxiv.org/abs/2310.13548)), cresce com escala e RLHF ([Perez et al., 2022](https://arxiv.org/abs/2212.09251)), e um perfil do usuário na memória a amplifica (até +45% no caso medido, com casos sem mudança significativa; [Jain et al., CHI 2026](https://doi.org/10.1145/3772318.3791915)).

## Como usar

1. Gere os seus três arquivos. O jeito mais rápido é a skill que acompanha o método (ela te entrevista e preenche). Os **perfis prontos** dos agentes/função estão em [`method/agents/`](method/agents/); (aliás, já nem sei mais o que chamo de agente). A porta e o manual saem preenchidos.
2. A tríade você calibra o agente, a descrição do projeto e um contexto mínimo sobre você para ajudar a diminuir o atrito de conversas de trabalho longo. A calibração pode ser feita por chat, numa interface própria pra isso ou simplesmente deixando numa pasta e pedindo pra instância ler, se preferir, traduz e usa via terminal.
3. Mantenha uma `memoria.md` **por projeto**, para garantir a continuidade do contexto "limpo" por projeto.

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

