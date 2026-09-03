<p align="right"><a href="README.pt-BR.md">🇧🇷 Português</a></p>

# Constellation Method

Three documents you fill in once, so an AI does not lose the thread between sessions. The instance reads the three at the start and already knows who you are, what matters now, and what role it takes on.

---

## The problem

The method came out of my own wish to get better at working with AI, in every sense. So I kept looking for ways to get better and better results with less effort, starting with simple things and scaling from there.

Mapping by what comes out of the system, I wrote working rules, an agreement that has to be set for the goal of the project to be met. In other words, I contextualized in a methodical way.

And the observation that led me to the logic of how to contextualize with minimum effort, split into 3 taxonomies, is that sycophancy has a function when it is tied to the goal of the work. Without a goal, it becomes noise in the conversation.

## Minimum context

Three documents, three layers:

- **the door** (`start_here`): where the instance enters. The topic, the goal, why it matters now = context of the goal;
- **the manual** (`how_to_work_with_me`): how your head works. Your criteria for collaboration = context of the human/AI communication;
- **the function** (`agents/`), **thinker**/**manager**/**worker**, or analysis/audit/execution = context of what is indispensable for meeting the goal.

## The triad of functions

The minimum quality starts from having at least two independent layers of checking, one deterministic and one probabilistic, or if you prefer, one auditing and one analytical.

- **Operationalized execution** (worker): runs the task without the bias of whoever designed the process.
- **auditing check** (manager): checks what came back against what was agreed.
- **analytical check** (thinker): stresses the hypothesis before it becomes a decision, and plans the next one.

## Two ways to use it (same architecture, different investments)

1. **As a project.** The three documents inside a workspace in the interface of the company that provides the AI service. It is the manual way, low maintenance cost, good for short to medium term projects.
2. **As a configured agent.** The same documents turned into agent configuration on the platform. Same effect, but scalable, for the long term, and it seems to depend on how you organize context navigation inside the project space.

The table in [`ONDE_CONFIGURAR.md`](ONDE_CONFIGURAR.md) shows where each layer lives on each platform I tested, for anyone who wants the second way. Two layers that reinforce each other:

- **Deterministic guardrails**: walls that do not depend on the model (what it cannot run, where it cannot write), mechanical.
- **Epistemic floor**: rules in prose that steer the behavior and narrow the range of the answers, because they act as criteria for being right, reinforcing the focus on the goal.

### The two rules that carry the honesty

The full floor (the cup and the columns) sits in the analytical role (thinker). The manager and the worker carry the lean version: the coin toss and the "failed if". Each role carries a floor sized to its function.

- **The cup 🍷**: the instance marks in one line what it notices but could not verify. The unverified is named, not hidden.
- **The coin toss**: before checking, the instance bets on the result, then scores whether it was right. It is a redundancy of checking over what it predicted, and the parameters of the prediction are adjusted at each miss.

  > **Example.** The instance bets before finishing: *"it states the probability it calculated, then either records the hit or recalculates"*. It is a way of asking for a check over its own conclusion, trying to work around sycophancy instead of forbidding it. I do not claim it solves the problem. It is an observation of mine, not a proof.

## More context = more tokens

More context means more tokens, the same logic as why long conversations cost more tokens. But I believe that in the short term it is a price paid in precision and quality, and in the long term I believe it is likely that it pays off. And the knowledge I gained working on this is part of that calculation for me.

## Where it works, and where it does not

It does not apply well to **software development and backend**. There the agents take on other roles, directed and bounded in chains, deterministic locks only, aimed at testing and checking code at scale.

What the triad brings that is specific is the **scalable analytical role**, and it pays off where the work involves **decision**, not just verifiable execution, such as:

- design and front-end development;
- data analysis and auditing;
- indicator monitoring;
- creative processes.

## What rung this method is on

**method** (formalized and applicable) → **reproducible** (others repeat it) → **effective** (evaluation measures the result) → **generalizable** (result observed by others)

The Triad places itself on the **first rung**: a formalized method, in daily use, with reproducibility and effectiveness still under test. Naming the ladder is the invitation, whoever wants to help knows which rung is open.

## What I lean on

I am not inventing a new discipline, I am **translating** old engineering practice into a new medium. Tools and methods for analyzing, mapping and managing processes also need context applied to them:

- **Poka-Yoke**: prevent the error through structure, not through the system's energy.
- **PDCA**: improve by checking the result, analytically and through auditing, before the next action.

On the idea that "the structure around the model moves the result", there is measurement recording the same model varying by dozens of points from one structure to another ([Harness-Bench, 2026](https://arxiv.org/abs/2605.27922), preprint). And sycophancy is a product of training on human preference ([Sharma et al., 2023](https://arxiv.org/abs/2310.13548)), grows with scale and RLHF ([Perez et al., 2022](https://arxiv.org/abs/2212.09251)), and a profile of the user in memory amplifies it (up to +45% in the measured case, with cases showing no significant change; [Jain et al., CHI 2026](https://doi.org/10.1145/3772318.3791915)). Maybe sycophancy does not have to be eliminated but directed, to lower the chance of error.

## Scale in folders (maximum scale + context navigation)

When the documents move to folders on your computer, this is the minimum structure I use:

```
Documents/
└── vault_[name]/
    ├── _to_delete/                 ← pre-trash: nothing is deleted for good
    ├── projects/
    │   └── project_[name]/
    │       └── start_here.md       ← the project door
    ├── neighborhood/               ← one home per agent
    │   ├── home_thinker/
    │   │   └── memory/             ← states
    │   ├── home_manager/
    │   └── home_worker/
    └── work_tables/
        └── work_table_[project]/   ← handoff between agents
            ├── _task/
            ├── _output/
            └── _states/
```

What each piece does: the **home** (`home_[agent]`) is where each agent is bound, and in some services the folder ties to the agent's identifier; the **work_table** is where one agent delivers and another picks up; the **memory** keeps the states of where the work stopped; the **pre-trash** avoids deletion and allows recovery; and `start_here.md` in the project folder is the door.

## Reading

- Anthropic, *Effective context engineering for AI agents* (2025).
- Liu et al., *Lost in the Middle* (2023), [arXiv:2307.03172](https://arxiv.org/abs/2307.03172).
- Yao et al., *Harness-Bench* (2026, preprint), [arXiv:2605.27922](https://arxiv.org/abs/2605.27922).
- Sharma et al., *Towards Understanding Sycophancy in Language Models* (2023), [arXiv:2310.13548](https://arxiv.org/abs/2310.13548).
- Perez et al., *Discovering Language Model Behaviors with Model-Written Evaluations* (2022), [arXiv:2212.09251](https://arxiv.org/abs/2212.09251).
- Jain et al., *Interaction Context Often Increases Sycophancy in LLMs* (2025), [arXiv:2509.12517](https://arxiv.org/abs/2509.12517).

## License

- **Method, templates and text:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Any code or script:** MIT.
