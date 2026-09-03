<p align="right"><a href="MANIFESTO.pt-BR.md">🇧🇷 Português</a></p>

# Manifesto | Constellation Method


I was at the start of my journey with language models, on everyday tasks: data analysis, audits, content creation (2025). And one thing always bothered me: the visible risks of **hallucination** and of **sycophancy** (the AI's tendency to agree with you just to please). That took the predictability and the trust out of the deliverables.

That pain turned into curiosity. Instead of investigating why the AI got things wrong, I went after **why it got things right**. Intuitively, I landed on **Context Engineering**, which I am not even sure is really a discipline, but I agree with the idea that the way you organize and deliver information shapes the model's behavior. The **Document Triad** came out of that, before any formal research.

**Structure changing the model's behavior is one thing**: models are steerable by context. **Does that make the result significantly better?** For me it has been working, but either I use it and study it, or I set up a laboratory, and I have a day job, I have not yet earned the superpower of controlling time. So I treat it as a **hypothesis**, not a proven fact, and I keep studying.

I went to read the scientific whys, careful to understand model behavior better so I would not reimplement a solution already discarded. Two points guided the adjustments: sycophancy **does not shrink** with better models, it grows with scale and with more training on human feedback (Perez et al., 2022); and giving the AI a profile of yours in memory **amplifies** agreement (up to +45% in the measured case; Jain et al., CHI 2026). That is when I better understood what I had been feeling my way toward by creating epistemic floors, guardrails, rules: I was **working around** the problem of imprecise agreement (the sycophancy that makes it err) with context. After all, if the bias is born in the training objectives themselves, I **choose** not to rely on the model policing itself by instruction alone, and I treat the check as **external structure**. That is also why the Triad **separates the Manual from the Role**: the Manual personalizes, and personalization can amplify agreement; the rules keep their taxonomies organized in the context.

My home field is **Production Engineering**, so I look at this with the eye of someone who designs workflows. I use two main concepts from there, in plain terms: **Poka-Yoke** (preventing the error through structure, not through willpower, which is what the cup and the coin game do) and **PDCA** (improving by checking the result, not just inspecting at the end). Nothing new, I am **translating** old engineering practice into a new medium.

Everything here comes from a focus on **self-improvement**, and I use it every day (_dogfooding_): I am user number one of my own method. I document to learn and to contribute, even if by getting things wrong.

🍷 I was organizing some processes...

---
*Living document. This repository's commit trail is the dated record of its evolution.*
