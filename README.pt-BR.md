<p align="right"><a href="README.md">🇺🇸 English</a></p>

# Método Constelação

Três documentos que você preenche uma vez, para uma IA não perder o fio entre sessões. A instância lê os três no começo e já sabe quem você é, o que importa agora e que papel ela assume.

---

## O problema

O método surgiu da minha vontade de aperfeiçoar, melhorar a minha interação com a IA em todos os sentidos. Então fui vendo de quais formas eu conseguiria com menos esforços ter resultados cada vez melhores, começando por coisas simples e depois escalando.

Mapeando pelo que resulta do sistema, criei regras de trabalho, um acordo que precisa ser estabelecido para o objetivo do projeto ser cumprido, ou seja, contextualizei de forma metodológica.

E a minha observação que levou à lógica do como contextualizar com esforço mínimo, separando em 3 taxonomias, é que a bajulação tem função quando amarrada ao objetivo do trabalho, sem objetivo, ela vira ruído na conversa.
## Contexto mínimo:

Três documentos, três camadas:

- **a porta** (`start_here`): onde a instância entra. O tema, o objetivo, o porquê aquilo importa agora = contextualização do objetivo;
- **o manual** (`how_to_work_with_me`): como a sua cabeça funciona. Os seus critérios de colaboração = contextualização da comunicação humano/ia;
- **a função** (`agents/`), **thinker**/**manager**/**worker** ou análise/auditoria/execução = contextualização do que é indispensável para o cumprimento do objetivo.

## Tríade de função

A qualidade mínima parte de ter pelo menos duas camadas de conferência independente, uma determinística, e outra probabilística, ou se preferir, uma auditiva e outra analítica.

- **Execução operacionalizada** (worker): executa a tarefa sem o viés de quem desenhou o processo.
- **conferência auditiva** (manager): confere o que voltou contra o que foi combinado.
- **conferência analítica** (thinker): estressa a hipótese antes de ela virar decisão, e planeja o próximo.
## Dois modos de usar (mesma arquitetura, investimentos diferentes)

1. **Como projeto.** Os três documentos num espaço de trabalho da interface da empresa que fornece o serviço de IA. É o jeito manual, custo baixo de manutenção, bom para projetos de curto a médio prazo
2. **Como agente configurado.** Os mesmos documentos virando configuração de agente na plataforma. Mesmo efeito, só que escalável, para duração a longo prazo, e parece depender da organização de navegação do contexto no espaço do projeto.

A tabela em [`ONDE_CONFIGURAR.md`](ONDE_CONFIGURAR.md) mostra onde cada camada mora em cada plataforma que eu testei, para quem quiser o segundo modo. Duas camadas que se reforçam:

- **Guardrails determinísticos**: paredes que não dependem do modelo (o que ele não pode executar, onde não pode escrever), mecânico.
- **Piso epistêmico**: regras em prosa que direcionam o comportamento e diminui o range das respostas por se comportarem como critérios de acerto, que reforçam o foco ao objetivo.

### As duas regras que carregam a honestidade

O piso completo (taça e colunas) fica no papel analítico (thinker). O manager e o worker carregam a versão enxuta: a moeda e o "falhou se". Cada papel carrega o piso do tamanho da função dele.

- **A taça 🍷**: a instância marca em uma linha o que percebe mas não conseguiu verificar. O não conferido fica nomeado, não escondido.
- **O jogo da moeda**: antes de conferir, a instância aposta no resultado; depois pontua se acertou. É uma redundância de conferência sobre do que ela previu, os parâmetros da previsão são ajustados à cada erro.

  > **Exemplo.** A instância aposta antes de terminar: *"ela declara a probabilidade calculada, e ou registra o acerto, ou recalcula"*. É um jeito de pedir conferência sobre a própria conclusão, tentando circundar a bajulação em vez de proibi-la. Não afirmo que resolve. É uma observação minha, não uma prova.

## + contexto = + tokens 

Mais contexto significa mais tokens, mesma lógica do porque conversas longas gastam mais tokens. Mas acredito que a curto prazo é um preço se paga em precisão e qualidade, e alongo prazo... Acredito que a longo prazo é possível que compensa o custo. E o conhecimento que eu adquiri trabalhando nisso faz parte desse cálculo pra mim.
## Onde isso funciona, e onde não

Não se aplica bem a **desenvolvimento de software e backend**. Ali os agentes assumem outros papéis, direcionados e delimitados em cadeias, somente travas determinísticas, voltados a teste e conferência de código em escala.

O que a tríade traz de específico é o **papel analítico escalável**, e ele rende onde o trabalho envolve **decisão**, não só execução verificável, como por exemplo:

- design e desenvolvimento front-end;
- análise e auditoria de dados;
- monitoramento de indicadores;
- processos criativos.
## Em que degrau este método está

**método** (formalizado e aplicável) → **reproduzível** (terceiros repetem) → **eficaz** (avaliação mede o resultado) → **generalizável** (resultado observado por outros)

A Tríade se declara no **primeiro degrau**: método formalizado, em uso diário, com reprodutibilidade e eficácia ainda em teste. Nomear a escada é o convite, quem quiser ajudar sabe qual degrau está vago.

## Em que eu me apoio

Eu não estou inventando disciplina nova, estou **traduzindo** prática velha de engenharia para um meio novo. ferramentas e metodologias de análise/mapeamento/gerenciamento de processos, também precisam de aplicação de contexto:

- **Poka-Yoke**: evitar o erro pela estrutura, não pela energia do sistema.
- **PDCA**: melhorar checando o resultado analítica e auditiva, antes da próxima ação.

Sobre a ideia de que "a estrutura em volta do modelo move o resultado", há medição registrando o mesmo modelo variando dezenas de pontos de uma estrutura para outra ([Harness-Bench, 2026](https://arxiv.org/abs/2605.27922), preprint). E a bajulação é produto do treino por preferência humana ([Sharma et al., 2023](https://arxiv.org/abs/2310.13548)), cresce com escala e RLHF ([Perez et al., 2022](https://arxiv.org/abs/2212.09251)), e um perfil do usuário na memória a amplifica (até +45% no caso medido, com casos sem mudança significativa; [Jain et al., CHI 2026](https://doi.org/10.1145/3772318.3791915)). Talvez a bajulação não tenha que ser eliminada e sim direcionada para diminuir as chances de erro.

## Escala em pastas (escala máxima + navegação por contexto)

Quando os documentos passam a viver em pastas no seu computador, esta é a estrutura mínima que eu uso:

```
Documents/
└── vault_[name]/
    ├── _to_delete/                 ← pré-lixeira: nada é apagado de vez
    ├── projects/
    │   └── project_[name]/
    │       └── start_here.md       ← a porta do projeto
    ├── neighborhood/               ← uma casa por agente
    │   ├── home_thinker/
    │   │   └── memory/             ← estados
    │   ├── home_manager/
    │   └── home_worker/
    └── work_tables/
        └── work_table_[project]/   ← handoff entre agentes
            ├── _task/
            ├── _output/
            └── _states/
```

O que cada peça faz: a **casa** (`home_[agent]`) é onde cada agente é vinculado, e em alguns serviços a pasta se liga ao identificador do agente; a **work_table** é onde um agente entrega e outro pega; a **memory** guarda estados de onde o trabalho parou; a **pré-lixeira** evita exclusão e permite recuperar; e o `start_here.md` na pasta do projeto.

## Leituras

- Anthropic, *Effective context engineering for AI agents* (2025).
- Liu et al., *Lost in the Middle* (2023), [arXiv:2307.03172](https://arxiv.org/abs/2307.03172).
- Yao et al., *Harness-Bench* (2026, preprint), [arXiv:2605.27922](https://arxiv.org/abs/2605.27922).
- Sharma et al., *Towards Understanding Sycophancy in Language Models* (2023), [arXiv:2310.13548](https://arxiv.org/abs/2310.13548).
- Perez et al., *Discovering Language Model Behaviors with Model-Written Evaluations* (2022), [arXiv:2212.09251](https://arxiv.org/abs/2212.09251).
- Jain et al., *Interaction Context Often Increases Sycophancy in LLMs* (2025), [arXiv:2509.12517](https://arxiv.org/abs/2509.12517).

## Licença

- **Método, templates e textos:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Qualquer código ou script:** MIT.
