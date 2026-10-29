# Improving instruction following in small LLMs

Shared Claude conversation, created 2026-10-29.
Source: https://claude.ai/share/5c8f8c6a-5b47-4bca-815e-1c93f660f328

Raw data (all messages, tool calls and search results): [`conversation.json`](conversation.json)

---

## User

So there is a problem. I am using a chatbot, it is using an economically viable llm, small models like gemini 3.5flash, luna. It is given an overall instruction guide and promt but its not able to get all of the signals. It could be due to the following things: 
1.⁠ ⁠conflicting signal
2.⁠ ⁠⁠instruction bloat
3.⁠ ⁠⁠missing

how to fix this so that instruction following capability of the bot increases. 


I want you to tell me methods, also tell me how can this be done better how do i find the optimal method, cite research papers and good articles wherever necessary

---

## Claude

> **Web search:** How many instructions can LLMs follow at once IFScale

> - [How Many Instructions Can LLMs Follow at Once?](https://arxiv.org/pdf/2507.11538)
> - [How Many Instructions Can LLMs Follow at Once?](https://nips.cc/virtual/2025/122417)
> - [How Many Instructions Can LLMs Follow at Once?](https://neurips.cc/virtual/2025/122417)
> - [How Many Instructions Can LLMs Follow at Once?](https://arxiv.org/html/2507.11538v1)
> - [arxiv.org](https://arxiv.org/abs/2507.11538)
> - [alphaxiv.org](https://alphaxiv.org/overview/2507.11538v1)
> - [huggingface.co](https://huggingface.co/papers/2507.11538)
> - [papers.cool](https://papers.cool/arxiv/2507.11538)
> - [web3.arxiv.org](https://web3.arxiv.org/pdf/2507.11538)

> **Web search:** Curse of Instructions LLMs multiple instructions success rate decreases

> - [Large Language Models Can Follow Instructions, But Not Many at Once: Phase Transitions in Compositional Constraint Satisfaction](https://arxiv.org/pdf/2608.12426)
> - [KCIF: Knowledge-Conditioned Instruction Following](https://arxiv.org/html/2410.12972v3)
> - [alphaxiv.org](https://alphaxiv.org/overview/2507.11538v1)
> - [How LLMs Follow Instructions: Skillful Coordination, Not a Universal Mechanism](https://www.alphaxiv.org/abs/2604.06015)
> - [arxiv.org](https://arxiv.org/abs/2510.14842v1)
> - [the curse of instructions khi llm ngop tho vi qua nhieu yeu cau cung luc ymJXDDo6Jkq](https://viblo.asia/p/the-curse-of-instructions-khi-llm-ngop-tho-vi-qua-nhieu-yeu-cau-cung-luc-ymJXDDo6Jkq)
> - [arxiv.org](https://arxiv.org/abs/2509.21051?context=cs)
> - [huggingface.co](https://huggingface.co/papers/2507.11538)
> - [論文の概要: When Instructions Multiply: Measuring and Estimating LLM Capabilities of Multiple Instructions Following](https://fugumt.com/fugumt/paper_check/2509.21051v1)
> - [The SIFo Benchmark: Investigating the Sequential Instruction Following Ability of Large Language Models](https://preview.aclanthology.org/new-sigs/2024.findings-emnlp.92/)

> **Web search:** GEPA reflective prompt evolution outperforms reinforcement learning

> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://arxiv.org/pdf/2507.19457)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://arxiviq.substack.com/p/gepa-reflective-prompt-evolution)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://proceedings.iclr.cc/paper_files/paper/2026/hash/0e9e708b6f48e14fd0ac29e167413f76-Abstract-Conference.html)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://arxiv.org/html/2507.19457v1)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://www.iclr.cc/virtual/2026/oral/10009494)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://www.alphaxiv.org/abs/2507.19457v2)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://iclr.cc/virtual/2026/poster/10009493)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://www.alphaxiv.org/abs/2507.19457v1)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://signals.aktagon.com/articles/2026/02/gepa-reflective-prompt-evolution-can-outperform-reinforcement-learning/)
> - [GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning](https://mlanthology.org/iclr/2026/agrawal2026iclr-gepa/)

> **Web search:** Chroma context rot increasing input tokens LLM performance

> - [Chroma logo](https://trychroma.com/research/context-rot)
> - [context rot evaluating llm performance degradation with increasing input tokens](https://www.zenml.io/llmops-database/context-rot-evaluating-llm-performance-degradation-with-increasing-input-tokens)
> - [Video thumbnail](https://research.trychroma.com/context-rot)
> - [Chroma Research Warns of Context Rot as LLMs Falter with Long Inputs  VmlldzoxMzczMjQ4MQ](https://wandb.ai/byyoung3/ml-news/reports/Chroma-Research-Warns-of-Context-Rot-as-LLMs-Falter-with-Long-Inputs--VmlldzoxMzczMjQ4MQ)
> - [new post your llm gets dumber when you feed it more why context rot is quietly breaking production a](https://aiengsimplified.beehiiv.com/p/new-post-your-llm-gets-dumber-when-you-feed-it-more-why-context-rot-is-quietly-breaking-production-a)
> - [context rot](https://github.com/chroma-core/context-rot)
> - [Context Rot: How increasing input tokens impacts LLM performance](https://hn.svelte.dev/item/44564248)

> **Web search:** LLMs conflicting system user instructions priority benchmark instruction hierarchy fails

> - [Revisión de artículo Control Illusion: The Failure of Instruction Hierarchies in Large Language Models](https://www.themoonlight.io/es/review/control-illusion-the-failure-of-instruction-hierarchies-in-large-language-models)
> - [skip to main content](https://par.nsf.gov/search/author:%22Yin,%20Bing%22)
> - [Literature Review Control Illusion: The Failure of Instruction Hierarchies in Large Language Models](https://themoonlight.io//en/review/control-illusion-the-failure-of-instruction-hierarchies-in-large-language-models)
> - [IHEval: Evaluating language models on following the instruction hierarchy](https://amazon.science/publications/iheval-evaluating-language-models-on-following-the-instruction-hierarchy)
> - [arxiv.org](https://arxiv.org/abs/2502.08745v2)
> - [skip to main content](https://par.nsf.gov/search/author:"Tang, Xianfeng")
> - [Daily Arxiv](https://haebom.dev/943zqpmqr3r8v2wnvy87?tl=en)
> - [iheval evaluating language models on](https://sotaverified.org/papers/iheval-evaluating-language-models-on)
> - [Haodong Wang](https://preview.aclanthology.org/moar-dois/people/h/haodong-wang)
> - [IHEval: Evaluating Language Models on Following the Instruction Hierarchy](https://preview.aclanthology.org/setup/2025.naacl-long.425)

> **Web search:** Anthropic effective context engineering for AI agents right altitude system prompt

> - [Engineering at Anthropic](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
> - [anthropic just changed the rules for working with ai and prompting isnt the main game anymore](https://www.theneuron.ai/explainer-articles/anthropic-just-changed-the-rules-for-working-with-ai-and-prompting-isnt-the-main-game-anymore)
> - [brunch.co.kr](https://brunch.co.kr/@7a2e11fe067d43e/18)
> - [prompt engineering for agentic ai](https://machinelearningmastery.com/prompt-engineering-for-agentic-ai/)
> - [Anthropic Just Changed the Rules for Working With AI | eWeek](https://www.eweek.com/de/news/anthropic-context-engineering-building-ai-workflows/)
> - [Anthropic Just Changed the Rules for Working With AI | eWeek](https://www.eweek.com/news/anthropic-context-engineering-building-ai-workflows/)
> - [context engineering](https://docs.claude-mem.ai/context-engineering)
> - [Composable Intelligence Executed in Real Time](https://succubuns.com/naughty-bots/b4435193-3d10-4f39-8bd3-2c6f34337893?page=8)
> - [Effective context engineering for AI agents Anthropic 2ddba4011a868170ac2ddd9017afadde](https://laisky.notion.site/Effective-context-engineering-for-AI-agents-Anthropic-2ddba4011a868170ac2ddd9017afadde)

The key point is that your three suspected causes need different fixes, so diagnose before you change anything. Prompt tweaking without measurement is how most chatbot prompts end up bloated.

## Why this happens

With many instructions, the chance of getting all of them right drops roughly exponentially. If each instruction is followed with probability p, all n are followed with roughly pⁿ. ManyIFEval (Harada et al., ICLR 2025, "Curse of Instructions") showed this: performance consistently degrades as the number of instructions increases, and a logistic regression using only instruction count predicted multi-instruction performance with about 10% error. A 2026 study found something worse: a model passing individual constraints around 41% of the time at k=8 satisfied all eight only 5.7% of the time, and for 12 of 15 models, success fell below 50% at 3 or fewer simultaneous constraints. Its takeaway applies directly to you: rearranging constraints did not prevent the collapse; only raising the per-constraint pass rate helped.

Small models are hit hardest. IFScale (Distyl AI, NeurIPS 2025) found model size and reasoning ability correlate with distinct degradation patterns, plus a bias toward earlier instructions. Length alone also hurts. Chroma's Context Rot report found models don't use context uniformly, and performance becomes increasingly unreliable as input grows.

## Step 1: Diagnose which cause you have

1. **Build an eval set.** Use 50 to 200 real conversations, including the failing ones. Turn every instruction into a check. Use code where possible (format, length, banned phrases) and an LLM judge with a rubric for fuzzy ones (tone, escalation behavior). This is the foundation for everything below.
2. **Measure per instruction.** You'll usually find a few instructions failing badly rather than all failing a little. That tells you where to focus.
3. **Run a leave-one-out ablation.** Remove one instruction at a time and re-run. If removing X raises compliance on Y, they conflict. If many unrelated instructions improve as the prompt shrinks, the problem is bloat.
4. **Check for conflicts directly.** The Instruction Boosting paper (IBM, 2025) found that a major reason performance drops as instructions are added is the growing tension and conflict between them, and released a quantitative conflict-scoring tool. A cheap version is to have a strong model compare every pair of instructions and flag contradictions or unclear precedence.
5. **Separate "missing" from "not salient."** If the bot fails a case and no instruction covers it, the instruction is truly missing. If an instruction exists but is ignored, the problem is salience or bloat, and adding more text will make it worse.

## Step 2: Fixes by cause

**Instruction bloat** (usually the biggest factor with Flash-class models)
- **Route instructions instead of sending all of them every time.** Use a cheap intent classifier first, then inject only the instruction modules relevant to that intent. This is the most effective single change for small models because it reduces the instruction count directly, which matters given the pⁿ math.
- **Split one call into a pipeline.** For example: classify, then retrieve policy, then draft, then check. Each call carries 3 to 5 constraints instead of 40.
- **Replace rule lists with examples.** Anthropic's context engineering guide recommends prompts at the "right altitude," a middle ground between two common failure modes: brittle if-then rules on one side and vague goals on the other. Their advice is to show 3 to 5 strong examples of what you want instead of listing every edge case.
- **Put critical rules first.** IFScale found earlier instructions were followed more reliably, though this helps less at extreme loads where failure becomes uniform.
- **Compress.** Merge duplicate rules, delete rules the model already follows by default (your ablation will show these), and remove explanatory prose.

**Conflicting signals**
- **Resolve conflicts in the text yourself.** Don't count on the model to apply system-over-user priority. IHEval (NAACL 2025) found all evaluated models dropped sharply when instructions conflicted, and the best open-source model resolved conflicts correctly only 48% of the time.
- **Write scoped rules with explicit tie-breakers.** "Be concise" plus "explain thoroughly" is a conflict. "Be concise unless the user asks why; then explain in at most 5 sentences" is not.
- **Use authority framing when needed.** The "Control Illusion" paper found models follow constraints framed through social hierarchies such as authority, expertise, or consensus more reliably than constraints based on system versus user roles. "Company policy requires X" can work better than a bare "Always X."

**Missing instructions**
- Add instructions only in response to failures you observed, and re-run the full eval after each addition to catch regressions. Anthropic's guidance is to start with a minimal prompt and add to it based on failure modes.

**Verify and repair after generation** (works for all three causes)
- **Enforce hard rules in code.** Use structured output or JSON schemas, regex checks, and retry on failure. Don't spend the model's limited attention on rules a parser can enforce.
- **Add a check-and-revise pass.** In the Curse of Instructions work, self-refinement improved all-instructions compliance for GPT-4o from about 15% to 31%, and for Claude 3.5 from about 44% to 58%. A second Flash call that receives the draft plus only the 5 to 8 rules most likely to be violated is cheap and effective.

## Step 3: Finding the optimal configuration

Treat this as an optimization problem over your eval set, not a writing exercise.

1. **Baseline.** Score the current prompt per instruction and as an all-pass rate.
2. **Manual structural changes first.** Try routing, decomposition, and verify-repair. These change the architecture, and automated optimizers can't discover them for you.
3. **Then run an automated prompt optimizer.** GEPA (ICLR 2026) is the current strongest option. It samples execution traces, reflects on them in natural language to diagnose problems, proposes and tests prompt updates, and combines complementary improvements from the Pareto frontier of its attempts. It beat MIPROv2, the leading previous optimizer, by over 10 percentage points, and a single reflective update often gives large improvements. It's sample-efficient, so it suits a budget setup. Use a strong model as the reflection model and your actual cheap model as the task model, since prompts optimized on one model don't reliably transfer to another. It's available in DSPy and at github.com/gepa-ai/gepa.
4. **Choose on the Pareto front, not on accuracy alone.** Plot compliance against cost and latency per message. A two-call Flash pipeline often beats one call to a bigger model at lower cost.
5. **Fine-tune only as a last resort.** If you've done all of the above and still fall short, collect your failures plus corrected outputs and fine-tune a small open model with LoRA. That builds the rules into the weights so they no longer compete for attention in the prompt.

## Further reading

- Harada et al., *Curse of Instructions*, ICLR 2025 (openreview.net/forum?id=R6q67CDBCH)
- Jaroslawicz et al., *How Many Instructions Can LLMs Follow at Once?* (arXiv 2507.11538)
- *Instruction Boosting / SCALEDIF* (arXiv 2510.14842): conflict scoring
- Zhang et al., *IHEval* (arXiv 2502.08745); Geng et al., *Control Illusion*: conflicts and priority
- Agrawal et al., *GEPA* (arXiv 2507.19457)
- Chroma, *Context Rot* (trychroma.com/research/context-rot)
- Anthropic, *Effective context engineering for AI agents* (anthropic.com/engineering)

If you share the system prompt (redacted is fine), I can do the conflict audit and propose a routed, modular version.

---

## User

what does this mean. 

also another question is that whether we'll start the ablation using all of the instructions ?
if yes, then how will we know which instruction is causing problem and in leave one out we will leave only one ? if not, then a lot of permutation combinations are possible, how do we handle that

---

## Claude

## What it means

You measure how well the bot follows each instruction with the full prompt, then remove one instruction and measure again. Then you check what changed.

Say your prompt has instructions A, B, C, D. With the full prompt, compliance is:

| | A | B | C | D |
|---|---|---|---|---|
| Full prompt (baseline) | 90% | 60% | 85% | 88% |

Now remove A and re-run the same eval set. If B jumps from 60% to 85%, A was interfering with B. Maybe A says "be brief" and B says "always list all options." That's a **conflict**: two specific instructions fighting each other.

Now suppose that whichever instruction you remove, the others each improve a little (2 to 4 points) with no strong pairwise pattern. That means no single instruction is the problem; the prompt is simply too long for the model to track everything. That's **bloat**.

## Do you start with all instructions?

Yes. The full prompt is your baseline, and every comparison is made against it.

## How do you know which instruction causes the problem?

Leave-one-out means each run removes exactly one instruction and keeps all the others. With N instructions, that's N runs, not every possible combination.

Put the results in a grid. Each row is "which instruction I removed," each column is "how compliance on that instruction changed versus baseline":

| Removed ↓ / Effect on → | A | B | C | D |
|---|---|---|---|---|
| A | (gone) | **+25** | +1 | 0 |
| B | +2 | (gone) | -1 | +1 |
| C | 0 | +3 | (gone) | +2 |
| D | +1 | **+18** | 0 | (gone) |

How to read it:
- **A big positive number in a cell** means the removed instruction was hurting that column's instruction. Here, both A and D interfere with B. B is the victim and A and D are the culprits, so you rewrite them with scoping or tie-breakers.
- **Small positives spread everywhere** point to bloat.
- **Removing an instruction and its behavior doesn't drop** means the model does it by default anyway. That instruction is redundant, and deleting it is free compression.

## Handling the combinatorics

You're right that testing every subset is impossible: 2^N combinations, which for 40 instructions is about a trillion. You avoid that in four ways.

1. **Leave-one-out is linear.** 40 instructions means 40 runs plus the baseline. That's affordable on Flash-class models.

2. **Group first, then drill down.** If you have many instructions, cluster them into modules such as tone, formatting, escalation, product policy, and safety. Run leave-one-out on the groups (8 runs instead of 40). Only inside the groups that show strong effects do you go down to individual instructions. It works like a binary search.

3. **Test pairs only for suspects.** Leave-one-out has a blind spot called masking. If A and D both hurt B, removing only A might show a smaller gain than expected because D is still there causing the problem. So once the grid flags suspects, remove them together as a pair (A+D) to confirm. You only test the handful of pairs the grid points to, never all of them.

4. **Pre-screen with an LLM.** Before running anything, have a strong model read the prompt and list instruction pairs that contradict each other or have unclear priority. That gives you a hypothesis list for free, and the ablation then confirms or rejects it.

## Two practical cautions

- **Noise.** Small differences of 2 to 3 points can be random. Use the same eval set every run, set temperature to 0 or average several samples, and only trust large, consistent changes.
- **Measuring bloat directly.** A cleaner test than reading the grid: pick 5 target instructions you care about, then add increasing amounts of unrelated instructions (0, 10, 20, 40) and plot compliance on those 5. A steady downward curve confirms bloat and shows how many instructions your model handles before it breaks down. That tells you how aggressively to route or split.

---

## User

what is this, explain this in more detail. Also tell how it can be used

---

## Claude

> **Web search:** dspy.GEPA metric feedback reflection_lm example

> - [# `Dspy.GEPA`](https://hexdocs.pm/dspex/Dspy.GEPA.md)
> - [dspy integration](https://www.mintlify.com/gepa-ai/gepa/guides/dspy-integration)
> - [dspy gepa example](https://github.com/shcallaway/dspy-gepa-example)
> - [GEPA DSPy Optimizer in SuperOptiX: Revolutionizing AI Agent Optimization Through Reflective Prompt Evolution](https://medium.com/@shashikant.jagtap/gepa-dspy-optimizer-in-superoptix-revolutionizing-ai-agent-optimization-through-reflective-prompt-1bd2dd9a8349)
> - [dspy gepa](https://skillselion.com/skills/lebsral/dspy-programming-not-prompting-lms-skills/dspy-gepa)
> - [prompt optimization](https://www.mintlify.com/gepa-ai/gepa/use-cases/prompt-optimization)
> - [dspy gepa reflective](https://www.skill-gallery.jp/skills/OmidZamani/dspy-gepa-reflective)
> - [Back to list](https://www.skill-gallery.jp/en/skills/OmidZamani/dspy-gepa-reflective)
> - [optimize anything artifact](https://github.com/gepa-ai/optimize-anything-artifact)

## What GEPA is

GEPA (Genetic-Pareto) is a tool that rewrites your system prompt for you. It does what a good prompt engineer does by hand: run the bot, read the failures, figure out why they happened, edit the prompt, and test again. The difference is that it does this systematically and keeps a record of everything it has tried.

The paper, by researchers from Berkeley, Stanford, and Databricks among others, argues that language is a much richer learning signal for LLMs than the sparse scalar rewards used in reinforcement learning. An RL method like GRPO only sees "this answer scored 0.4." GEPA sees the full trace plus a written explanation such as "the bot gave a refund amount without asking for the order ID, which violates the escalation policy." One explanation like that tells you more than hundreds of bare scores. That's why it matched or beat GRPO while using up to 35x fewer rollouts.

## How it works

There are three parts.

**1. Reflective mutation.** GEPA runs your bot (the task model, e.g. Gemini Flash) on a small batch of examples. It then gives a strong model (the reflection model) the current prompt, the inputs, the outputs, and your feedback on what went wrong. The reflection model diagnoses the failure and writes an improved prompt. That new prompt is a candidate, and it's kept only if it scores better on that batch.

**2. Pareto selection.** This is the part that makes GEPA work well. A naive optimizer keeps only the single best-scoring prompt and keeps editing it, which tends to get stuck. GEPA instead keeps every prompt that is the best on at least one example. Prompt A might handle refund questions well while prompt B handles angry users well. Both survive, even if neither has the highest average. This set of "each best at something" prompts is the Pareto frontier. Choosing which prompt to improve next from this set keeps the search diverse.

**3. Merging (the "genetic" part).** GEPA can combine two candidates that learned different lessons into one prompt that has both. That's how prompt A's refund handling and prompt B's de-escalation end up in a single prompt.

The loop looks like this:

```
pick a prompt from the Pareto frontier
  → run it on a few examples with the cheap model
  → strong model reads traces + feedback, writes improved prompt
  → better on that batch? score it on the validation set, add to pool
  → update the Pareto frontier
  → repeat until budget runs out
```

## Why the reflection model and task model are different

The reflection model's job is diagnosis and writing, which needs a strong model. It's called only once per iteration, so it's cheap overall. The task model must be the model you actually deploy, because a prompt tuned for one model often doesn't transfer well to another. A prompt that works on a frontier model can still confuse Flash.

## How to use it for your chatbot

You need three things: a dataset, a metric that returns feedback, and a program. You already have most of this from the ablation eval.

**Step 1: Dataset.** Collect 50 to 200 real conversations, weighted toward failure cases, plus whatever reference information you have (expected behavior, which rules apply). Split them into train (about 60%) and validation (about 40%). GEPA proposes edits based on train and selects prompts based on validation, which prevents it from overfitting to a few examples.

**Step 2: A metric that returns feedback.** This matters most. The score tells GEPA whether a prompt is better; the feedback tells it why. One writeup of the paper reports that task-specific feedback produces noticeably better evolved prompts than generic feedback. Your per-instruction checks from the ablation turn directly into feedback strings.

**Step 3: Run it.**

```python
import dspy

flash = dspy.LM("gemini/<your-flash-model>")        # task model: what you deploy
strong = dspy.LM("<strong-model>", temperature=1.0, max_tokens=8000)  # reflection model
dspy.configure(lm=flash)

class SupportReply(dspy.Signature):
    """<paste your current system prompt here; GEPA evolves this text>"""
    conversation: str = dspy.InputField()
    reply: str = dspy.OutputField()

bot = dspy.Predict(SupportReply)

def metric(gold, pred, trace=None, pred_name=None, pred_trace=None):
    failures = []
    if len(pred.reply.split()) > 120:
        failures.append("Reply exceeded 120 words; rule says keep replies short.")
    if gold.needs_escalation and "human agent" not in pred.reply.lower():
        failures.append("User asked for a refund over the limit; bot should have offered a human agent.")
    # ... one check per instruction, code-based or LLM-judge
    score = 1 - len(failures) / TOTAL_CHECKS
    feedback = " ".join(failures) or "All instructions followed."
    return dspy.Prediction(score=score, feedback=feedback)

optimizer = dspy.GEPA(metric=metric, reflection_lm=strong, auto="light")
optimized = optimizer.compile(bot, trainset=train, valset=val)

print(optimized.signature.instructions)   # your new system prompt
```

Build the examples with `dspy.Example(conversation=..., needs_escalation=...).with_inputs("conversation")` so DSPy knows which fields are inputs.

**Step 4: Deploy the text.** The output is just a better system prompt. You don't need DSPy in production; copy the instructions into your existing bot. If you prefer to skip DSPy entirely, the standalone `gepa` package has an adapter interface where you implement evaluate and make_reflective_dataset and GEPA handles the rest.

## Fitting it into your plan

- **Do the structural fixes first.** GEPA optimizes text inside a fixed structure. It won't decide to split your bot into a router plus modules. Do routing and decomposition by hand first, then run GEPA on each module's prompt separately. Small, focused prompts optimize much better than one giant prompt.
- **Watch prompt length.** GEPA tends to produce long, detailed prompts. On a small model that can reintroduce bloat. Compare the length before and after, and if it grew a lot, try adding a length penalty to the metric.
- **Budget.** Start with `auto="light"`. Cost is roughly (number of metric calls × Flash cost) plus a few dozen strong-model calls. For a chatbot eval of this size, that's usually a small amount.
- **Check the result yourself.** Read the optimized prompt. GEPA sometimes learns rules that only make sense for your training examples. Your validation scores and a manual read will catch most of these.

---

## User

can I take inspiration of this idea and use something to improve instruction following capability

---

## Claude

Yes. GEPA's core ideas are general, and several of them map directly onto instruction following. The three ideas worth borrowing are: learn from written feedback instead of scores, keep candidates that are best at *something* instead of best on average, and merge candidates that learned different lessons. Here's how each can be applied.

## 1. Pareto over instructions instead of examples (most promising)

GEPA keeps a prompt if it's the best on at least one example. For instruction following, make each instruction its own objective instead. Keep a prompt version if it's the best at following at least one instruction, then merge versions.

This fits your problem better than plain GEPA because instruction following really is many objectives at once, and averaging them hides which rules are being dropped. It also gives you conflict detection for free. If no prompt version does well on both instruction X and instruction Y, and improving one always hurts the other, those two are in conflict. Your ablation finds conflicts by removing things; this approach finds them while optimizing.

## 2. A deletion operator to fight bloat

GEPA's reflection step mostly adds detail, which is the opposite of what a small model needs. Give the reflection model an explicit second operation: given the prompt and the traces, delete, merge, or shorten instructions without lowering the score. Alternate between "fix failures" steps and "compress" steps, and include prompt length in the score. You end up optimizing for the shortest prompt that still passes, which directly targets bloat.

## 3. Rulebook learning from failures

Run the bot, collect failures, and have a strong model write each one up as a short, scoped lesson ("when the user asks about refunds over the limit, offer a human agent before quoting policy"). Store these in a rulebook, deduplicate them, and inject only the relevant ones at runtime through your router. This is GEPA's reflection idea, but the output is a growing, organized rule library instead of one monolithic prompt. It handles "missing instructions" systematically instead of through ad-hoc patches. Agentic Context Engineering (ACE, 2025) explores a similar idea of evolving a playbook through small incremental edits, which is worth reading if you go this route.

## 4. Reflection at inference time

Use the same diagnose-and-fix loop at runtime. After the bot drafts a reply, a cheap checker call evaluates it against only the routed rules and writes specific feedback ("violated rule 3: no order ID requested"). The bot then revises using that feedback. This works better than a generic "check your answer" pass because the feedback names the exact violation.

## 5. Move the prompt into the weights

Once you have an optimized prompt that works well, generate many conversations with it, then fine-tune the small model on those outputs without the prompt (this is called context distillation). The model learns to behave as if it had the instructions without spending any attention on them. That removes the instruction-count problem entirely for the stable rules, leaving the prompt free for rules that change often.

## Which to start with

For fixing your chatbot quickly, use **2 and 4**. They're cheap and directly address bloat and dropped rules. **3** is the best long-term setup once your instruction set keeps growing.

Idea **1** combined with **2** is also a real research contribution, not just engineering. Per-instruction Pareto optimization with built-in conflict detection and a length objective hasn't been studied much. You could evaluate it on ManyIFEval and IFScale, both of which already have per-instruction checks, against GEPA and MIPROv2 as baselines. It's a manageable scope for a workshop paper.

---

## User

what more fixes do you propose, lets ideate on this, what more can be done for this

---

## Claude

Here are fixes beyond what we've covered, grouped by where they act in the pipeline. I've skipped what's already discussed (routing, decomposition, GEPA, verify-and-repair, the earlier variants).

## 1. How instructions are written

- **Write rules as condition and action, not prose.** "IF user mentions refund AND amount > limit THEN offer human agent" is easier for a small model to match than a paragraph. A consistent structure (YAML, numbered rules, XML sections) also makes rules easier to find within the prompt.
- **Phrase rules positively.** "Don't use jargon" makes the model think about jargon. "Use words a 12-year-old knows" states the target directly. Small models are noticeably weaker at following negations.
- **Split MUST from SHOULD.** Label every rule. MUST rules get enforced in code or by the verifier; SHOULD rules are left to the model. This stops you from relying on the model's attention for rules that can't fail.
- **Set a rule budget.** Cap each module at around 8 to 10 rules. Adding a rule requires removing or merging another. This keeps prompts from slowly growing over time.

## 2. Where instructions sit in the context

- **Add a per-turn reminder.** Right before the latest user message, inject the 2 or 3 rules most relevant to this turn. Models pay most attention to the start and end of context, and the system prompt is far away by turn 10.
- **Fix multi-turn drift.** Instruction following usually gets worse as conversations get longer. Replace raw history with a short structured state (user goal, facts collected, open questions) plus the last few turns. That reduces context rot and keeps rules closer in relative terms.
- **Plan before answering.** Ask the model to first output (hidden from the user) which rule IDs apply to this turn, then write the reply. Explicitly selecting rules makes it more likely to apply them. If your Flash model has a thinking budget, this is a natural use for it.

## 3. Decoding and sampling

- **Best-of-N with a verifier.** Generate 3 replies in parallel, score each with your rule checks, and send the best one. On a cheap model this often costs less than a second sequential repair call, and it adds no latency.
- **Constrained decoding.** For format rules (JSON, fixed fields, allowed labels), use schema-constrained output so violations are impossible.
- **Logit bias for banned words.** If certain words or phrases must never appear, block them at the token level when the API supports it, instead of asking in the prompt.

## 4. Architecture

- **Separate content from style.** One call decides what to say (facts, policy, next action). A second call rewrites it in your voice. Style rules only exist in the second prompt, so they no longer compete with policy rules.
- **Move fixed text into code.** Disclaimers, greetings, sign-offs, and legal lines should be added by code, not requested in the prompt. Every rule you hard-code is one fewer the model has to remember.
- **Model cascade.** Detect hard or high-risk turns (complaints, refunds, legal topics, low verifier score) and send only those to a larger model. Most turns stay on Flash.
- **Templates for frequent intents.** For your top 10 intents, have the model fill slots in a template instead of writing freely. Less freedom means fewer ways to break rules.

## 5. Training (if you can use open models)

- **Preference tuning from your own bot.** Best-of-N already gives you pairs: replies that passed your checks versus replies that failed. Use those for DPO. The model learns your rules from its own mistakes, and you don't need to label anything by hand.
- **RL with verifiable rewards.** Your rule checks are the reward function. Tülu 3 used this approach for constraint following. It's more work than DPO but more targeted.
- **Attention steering.** With open weights, methods like PASTA ("Tell Your Model Where to Attend," ICLR 2024) increase the model's attention to chosen spans, such as your rule section, at inference time without retraining.

## 6. Process and operations

- **CI for prompts.** Treat the prompt like code: version control, and every change runs the eval set and the conflict check before merging. Block a change if any instruction drops by more than a set threshold.
- **Production feedback loop.** Sample live conversations daily, run the judges, and feed failures into the eval set and the rulebook or GEPA loop. Your eval set then reflects real usage over time instead of only the cases you thought of.
- **Re-test on model updates.** Providers update Flash-class models silently or frequently. Keep a fixed regression suite and re-run it whenever the model version changes, because prompts tuned for one version can break on the next.

## Highest return for the effort

If I had to pick five to do first:

1. MUST/SHOULD split, with MUSTs in code or the verifier
2. Per-turn rule reminder
3. Best-of-N with your existing checks
4. Content/style separation
5. Prompt CI with the eval set

These are cheap, model-agnostic, and each addresses a different failure mode. Training-based fixes become worthwhile once you have production logs to learn from.

Which part of the bot fails most right now: format, policy, tone, or multi-turn? That would narrow down which of these matters most for you.

---

## User

1. alright so the system prompt also chooses between three personas (E,M,R). 

so is there a better way through which we can programatically decide which persona to give in the specific message context, this would reduce the size of the prompt and reduce the instruction bloat, if not programatically what other methods are there. cite articles or papers wherever necessary. 


2. Right now the bot gives the whole conversation to a human agent and that is decided on the basis of number of turns, how can we make this better from a simple turn based system. Maybe an ML model of some sorts ? or some text based DL model ? what other techniques are there. 



Keep in mind that we are serving a large amount of customers and cost is of atmost priority

---

## Claude

> **Web search:** predicting human handoff customer service chatbot escalation model paper

> - [Time to Transfer: Predicting and Evaluating Machine-Human Chatting Handoff](https://arxiv.org/pdf/2012.07610)
> - [Causal Inference for Chatting Handoff](https://arxiv.org/pdf/2210.02862)
> - [ojs.aaai.org](https://ojs.aaai.org/index.php/AAAI/article/view/16731/16538)
> - [Time to Transfer: Predicting and Evaluating Machine-Human Chatting Handoff](https://ar5iv.arxiv.org/html/2012.07610)
> - [Measuring chatbot quality of service to predict human-machine hand-over using a character deep learning model](https://opus.lib.uts.edu.au/handle/10453/168298)
> - [2022.emnlp main.213](https://aclweb.org/anthology/2022.emnlp-main.213.pdf)
> - [customer support chatbot to human handoff timing](https://www.cognizant.com/ca/en/insights/insights-blog/customer-support-chatbot-to-human-handoff-timing)
> - [A Role-Selected Sharing Network for Joint Machine-Human Chatting Handoff and Service Satisfaction Analysis](https://preview.aclanthology.org/author-url/2021.emnlp-main.767/)
> - [A Role-Selected Sharing Network for Joint Machine-Human Chatting Handoff and Service Satisfaction Analysis](https://preview.aclanthology.org/setup/2021.emnlp-main.767)

> **Web search:** SetFit efficient few-shot learning sentence transformers

> - [Efficient few-shot learning with Sentence Transformers](https://pypi.org/project/setfit/0.4.1)
> - [Efficient Few-Shot Learning Without Prompts](https://deepai.org/publication/efficient-few-shot-learning-without-prompts)
> - [SetFit: Efficient Few-Shot Learning Without Prompts](https://huggingface.co/blog/setfit)
> - [Efficient Few-Shot Learning Without Prompts](https://neurips.cc/virtual/2022/59465)
> - [Efficient Few-Shot Learning Without Prompts](https://nips.cc/virtual/2022/59465)
> - [efficient few shot learning without prompts](https://www.catalyzex.com/paper/efficient-few-shot-learning-without-prompts)
> - [Efficient Few-Shot Learning Without Prompts](https://neurips.cc/virtual/2022/59466)
> - [Efficient Few-Shot Learning Without Prompts](https://nips.cc/virtual/2022/59466)
> - [Efficient Few-Shot Learning Without Prompts](https://api.deepai.org/publication/efficient-few-shot-learning-without-prompts)
> - [Efficient few-shot learning with Sentence Transformers](https://pypi.org/project/setfit-dont-use-deprecated-dataset-filter/)

> **Web search:** Gemini API implicit context caching common prefix discount

> - [Gemini 2.5 Models now support implicit caching](https://developers.googleblog.com/gemini-2-5-models-now-support-implicit-caching/)
> - [Gemini 2.5 Models now support implicit caching](https://developers.googleblog.com/zh-hans/gemini-2-5-models-now-support-implicit-caching)
> - [Gemini 2.5 Models now support implicit caching](https://developers.googleblog.com/en/gemini-2-5-models-now-support-implicit-caching/)
> - [Gemini 2.5 Models now support implicit caching](https://developers.googleblog.com/pt-br/gemini-2-5-models-now-support-implicit-caching)
> - [Gemini 2.5 Models now support implicit caching](https://developers.googleblog.com/es/gemini-2-5-models-now-support-implicit-caching/)
> - [Simon Willison’s Weblog](https://feeds.simonwillison.net/tags/prompt-caching/)
> - [Simon Willison’s Weblog](https://simonwillison.net/tags/prompt-caching/)

The two problems have the same answer: move decisions out of the LLM and into cheap, specialized components, and keep the LLM for writing replies.

# 1. Choosing the persona outside the prompt

Right now every message carries all three persona definitions plus the logic for picking one. That's bloat, and it also asks the model to make a decision it isn't reliably good at. Pick the persona outside the LLM and inject only the chosen persona's block.

The right method depends on what drives the choice, so check this first:
- **Known customer facts** (segment, product, language, channel, tier): use rules. They're free and exact.
- **What the customer is saying** (topic, emotion, urgency): use a classifier.
- **Both**: use a classifier that takes customer facts as extra features.

## Options, from cheapest up

**a) Rules on metadata.** If persona choice mostly follows customer fields, a lookup table solves it at zero cost. Check your logs: if the current bot's persona choice correlates strongly with any field, start there.

**b) Small text classifier.** Embed the last 1 to 3 user messages and train a logistic regression or small classifier head on top. It runs on CPU in milliseconds. If you have few labeled examples, use SetFit. It fine-tunes a sentence transformer on a small number of labeled text pairs with contrastive learning, then trains a classification head on the resulting embeddings, with no prompts needed and orders of magnitude fewer parameters and less runtime than LLM-based approaches. It also handles multilingual text by swapping in a multilingual sentence-transformer model, which matters if your customers mix Hindi and English.

**c) Cascade.** Use the classifier when it's confident (for example, probability above 0.8). Only in uncertain cases, make a short Flash call containing just the three persona descriptions and the recent messages. If 85 to 90% of turns are decided by the classifier, the LLM fallback costs very little.

**d) Let the main bot choose for the next turn.** Add a `next_persona` field to the bot's structured output. There's no extra call, but there's a one-turn lag. This is useful as a feature for (b), or as a fallback if you don't want to train anything yet.

## Getting labels without manual work

Your bot already picks a persona on every turn. Log those choices and train the classifier to reproduce them (this is distillation). Then have a strong model review a few hundred cases to correct the wrong ones. You get a fast classifier at least as good as the current LLM choice, and better wherever the corrections helped.

## Keep the persona stable

Choose the persona at the start of the conversation and switch only on a strong signal, for example the classifier preferring another persona with high confidence for two turns in a row. That prevents the bot from changing voice mid-conversation, and you can run the classifier less often.

## Later: choose by outcome, not by fit

Ultimately you want the persona that leads to the best result, not the one that "matches" best. Once you log outcomes (resolved, CSAT, escalated), treat persona choice as a contextual bandit: context in, persona out, and reward from the outcome. Bandit methods like LinUCB or Thompson sampling are simple to implement, and they learn things like "persona M resolves billing complaints faster than R," which no labeling scheme would capture.

## Order the prompt for caching

Put the shared core instructions first, then the persona block, then the conversation. Google's guidance for implicit caching is to keep the beginning of the request the same and put content that changes per request at the end. When Gemini 2.5 launched implicit caching, matching prefixes got a 75% token discount. Check the current rate for your model. With three personas, you effectively have three cached prefixes, all of which stay warm at your traffic volume. At large scale, this alone can cut input cost substantially.

# 2. Better handoff than a turn count

A turn limit fails in both directions. It escalates long conversations that were going fine, and it misses a customer who is furious at turn 2. Research calls this problem Machine-Human Chatting Handoff (MHCH): continuously monitoring the conversation, predicting chatbot failures such as algorithm errors or negative user emotions, and transferring to a human agent. Timing matters: a good handoff model should detect dissatisfaction as early as possible, because a delayed handoff can lead to impatience and abandonment.

## A layered system, cheapest layer first

**Layer 1: Hard triggers (rules, near-zero cost).** Escalate immediately on any of these:
- The customer explicitly asks for a human.
- Legal threats, fraud or security issues, or payment failures.
- The same intent repeated 2 or 3 times.
- Tool or API calls failing twice.
- The bot repeating itself.

These catch the obvious cases, and every decision is easy to explain.

**Layer 2: Feature-based model (LightGBM or XGBoost).** Compute cheap signals each turn:

| Signal | How to compute it cheaply |
|---|---|
| User not being understood | Embedding similarity between consecutive user messages (high similarity means they're rephrasing) |
| Frustration trend | Sentiment score per turn and its slope, all-caps text, repeated punctuation, shorter messages |
| Bot struggling | Count of apologies or hedges in bot replies, verifier failures, "I'm not sure" responses |
| Difficulty | Intent category (some intents rarely get resolved by the bot) |
| Context | Turn number (as one feature among many, not the rule), customer tier, current agent queue length |

Gradient-boosted trees run in microseconds, need modest amounts of data, and show which features drive decisions, which helps when you're explaining the system to stakeholders.

**Layer 3: Text encoder over the conversation.** Fine-tune a small encoder (DistilBERT- or ModernBERT-size, or SetFit) on the last k turns to predict whether this conversation needs a human. Feed its probability into the Layer 2 model as a feature, so you don't maintain two separate decision systems. Joint training also helps: RSSN (EMNLP 2021) combines satisfaction estimation and handoff prediction in a single multi-task model, using local user satisfaction to connect the two.

**Free signal from the bot itself:** add `needs_human: true/false` and a short reason to the main LLM's structured output. It costs nothing extra. Use it as a feature, not as the final decision.

## Decide by cost, not a fixed threshold

Escalate when the expected cost of continuing with the bot exceeds the cost of an agent:

```
P(bot fails) × cost of failure (churn, repeat contact, bad CSAT)  >  cost of agent time
```

The CEM paper (EMNLP 2022) argues that ignoring this matters: existing handoff models ignore causal variables like user state and labor cost, which leads to biased predictions and higher costs. Their fix trains an auxiliary cost simulator with counterfactual learning so the model becomes cost-aware. A simple practical version: make the threshold depend on agent queue length. Escalate more readily when agents are free and be stricter when they're overloaded.

## Labels: the trap to avoid

Don't train on "was this handed off?" Your current handoffs come from the turn rule, so the model would just learn the turn rule again. Use outcome labels instead:
- **Positive:** the customer asked for a human, abandoned mid-conversation, gave negative CSAT, contacted support again within 48 hours, or an agent resolved something the bot couldn't.
- **Negative:** resolved by the bot with no repeat contact.

There's also a selection-bias issue. Your current policy cuts off every conversation at N turns, so you have no data on what would have happened if the bot continued. To fix this, let a small random slice of traffic (1 to 2%) continue past the limit when there are no frustration signals. That gives you unbiased data, and it's cheap.

## Reduce agent cost after handoff too

- **Send a summary, not the transcript.** One cheap LLM call produces the issue, what was already tried, and the customer's emotional state. Agents resolve faster, and agent time is your largest per-conversation cost.
- **Offer, don't force.** For borderline cases, ask "Want me to connect you to an agent?" Many customers decline, which saves agent time without making them feel ignored.

## How to measure

- **Offline:** precision and recall of handoff predictions, plus how many turns earlier than the current rule you catch failing conversations.
- **Online (A/B test):** containment rate, CSAT, agent minutes per conversation, and repeat-contact rate.

The industry framing agrees: escalation thresholds should be retrained and recalibrated continuously by analyzing outcomes after handoff.

# Recommended setup for your scale

| Component | Start with | Upgrade to |
|---|---|---|
| Persona | Metadata rules + distilled SetFit classifier, kept stable per conversation | Contextual bandit on outcomes |
| Handoff | Hard triggers + LightGBM on cheap features + LLM's `needs_human` flag | Add an encoder probability and a cost-aware threshold based on queue length |
| Prompt | Shared core → persona block → conversation (cache-friendly) | Per-intent instruction modules on the same pattern |

None of this adds an LLM call on the common path. Everything new runs on CPU or rides along in the existing call, which matters at your volume.

What are E, M, and R in practice: different tones, different expertise levels, or different customer segments? That determines whether rules alone are enough or you need the classifier.

---

## User

for handoff what is a better method, feature based ml models, text encoders over conversations or an ensemble of these

---

## Claude

**Short answer: an ensemble, built in stages, with the gradient-boosted tree model as the final decision-maker and the text encoder feeding into it.** Each model type sees signals the other misses, so combining them usually beats either one alone. But start with the tree model, and add the encoder only if it gives a measurable improvement on your data.

## What each one sees

| | Feature model (LightGBM / XGBoost) | Text encoder over the conversation |
|---|---|---|
| **Strong at** | Operational signals: tool failures, repeated intents, turn count, customer tier, queue load, timing between messages | Language nuance: implied frustration ("this is my third time contacting you"), sarcasm, polite but annoyed phrasing, confusion |
| **Blind to** | Meaning that isn't captured by a hand-designed feature | Anything that isn't in the text (API errors, customer history, agent availability) |
| **Data needed** | Hundreds to a few thousand labeled conversations | Thousands or more for fine-tuning (less with SetFit) |
| **Inference cost** | Microseconds | Milliseconds on CPU for a small model, per turn |
| **Explainability** | High (feature importance, SHAP values) | Low |
| **Calibration** | Easy to get reliable probabilities | Needs post-hoc calibration |

Calibration matters here because the cost-based threshold from earlier (escalate when P(failure) × cost of failure > agent cost) only works if the probabilities are accurate.

In production customer support, many of the strongest handoff signals aren't in the text at all: a failed refund API call, a customer who contacted support yesterday, a queue that's empty right now. The academic MHCH models are mostly text-only because their datasets lack those signals. Your system has them, which is why the tree model should be the core.

## The ensemble design: stacking

Don't average the two models' outputs. Use the encoder's probability as one input feature to the tree model:

```
features per turn ──────────────┐
                                ├──► LightGBM ──► P(needs human) ──► cost-based threshold
encoder(last k turns) ──► p_enc ┘
```

This lets the tree learn when to trust the encoder. For example, it might rely on the encoder for complaint intents but ignore it when a tool failure already explains the problem.

One rule is essential: **train the encoder's predictions out-of-fold.** If you train the encoder on the same conversations you then use to train the tree, the encoder's probability will look unrealistically accurate, and the tree will over-trust it. Use k-fold cross-fitting so each encoder prediction comes from a model that never saw that conversation.

## A cheaper middle option

Before fine-tuning anything, use **frozen sentence embeddings to build features** for the tree:
- Similarity between consecutive user messages (rephrasing means the customer isn't being understood)
- Similarity of the current message to a small set of example frustrated messages
- Sentiment score from an off-the-shelf model, plus its trend over turns

This captures much of what a fine-tuned encoder would provide at a fraction of the effort, and the features stay interpretable. If your customers write in Hinglish or other code-mixed text, use a multilingual embedding model for this.

## Saving compute at scale: cascade

You don't need to run the encoder on every turn. Run the tree model on cheap features first. Only if its probability falls in an uncertain middle range (say 0.3 to 0.7), run the encoder and re-score. Most turns are clearly fine or clearly failing, so the encoder might run on only 10 to 20% of turns.

## How to decide with your own data

Build all three variants and compare them on the same held-out set:

1. Tree model with operational features only
2. Tree model plus frozen-embedding features
3. Tree model plus fine-tuned encoder probability (stacked)

Evaluate them correctly:
- **Split by time and by customer**, not randomly. Train on older months and test on the most recent. Random splits leak information about the same customer or the same week into the test set and make results look better than they are.
- **Predict per turn using only information up to that turn.** Never use features from later in the conversation.
- **Metrics:** PR-AUC (handoffs are a minority class, so plain accuracy is misleading); recall at a fixed handoff rate matching your agent capacity (e.g., "if we can escalate 8% of conversations, how many true failures do we catch?"); how many turns earlier than the current rule you catch failures; and calibration.

Then decide on cost: keep the encoder only if the gain from variant 2 to variant 3 is worth the extra inference and maintenance. In many production systems, variant 2 captures most of the benefit and is the right stopping point.

---

## User

what does calibration mean and explain post hoc calibration

---

## Claude

## What calibration means

A model is **calibrated** if its probabilities match how often things actually happen.

If your handoff model says "70% chance this conversation needs a human" for 1,000 conversations, then about 700 of them should actually need a human. If only 400 do, the model is **overconfident**. If 900 do, it's **underconfident**.

Calibration is separate from ranking. A model can be excellent at ordering conversations from "fine" to "failing" (high AUC) and still produce the wrong numbers. Example:

| Model says | Actual failure rate | |
|---|---|---|
| 0.9 | 0.55 | ranked correctly, number too high |
| 0.6 | 0.30 | ranked correctly, number too high |
| 0.2 | 0.05 | ranked correctly, number too high |

The ranking is perfect but the numbers are inflated.

## Why it matters for your handoff system

If you use a fixed threshold tuned on data (e.g., "escalate the top 8%"), you only need correct ranking, and calibration doesn't matter much.

But the cost-based rule from earlier uses the probability directly:

```
escalate if P(failure) × cost of failure > cost of agent time
```

If P is inflated, you escalate too often and spend money on agents unnecessarily. If P is too low, you miss customers who are about to churn. The decision is only as good as the number.

Calibration also matters when combining models (stacking). The tree model takes the encoder's probability as a feature, and a miscalibrated input is harder for it to use well.

## Why models become miscalibrated

- **Neural networks** (your text encoder) tend to be overconfident. Guo et al. ("On Calibration of Modern Neural Networks," ICML 2017) showed that modern deep networks are much more overconfident than older, smaller ones.
- **Class imbalance fixes.** If you downsample negatives or use class weights because handoffs are rare, the model sees an artificially high positive rate during training and its probabilities shift upward. This is the most common cause in practice, and it applies to your tree model too.
- **Drift.** The model was calibrated on last quarter's traffic, but customer behavior, products, or the bot itself have changed since.

## How to measure it

- **Reliability diagram:** group predictions into bins (0 to 0.1, 0.1 to 0.2, and so on), and plot average predicted probability against actual outcome rate in each bin. A calibrated model's points fall on the diagonal. Points below the diagonal mean overconfidence.
- **Expected Calibration Error (ECE):** the average gap between predicted and actual rates across bins, weighted by how many predictions fall in each. Lower is better.
- **Brier score:** mean squared error between predicted probability and the 0/1 outcome. It combines calibration and discrimination into one number.

## Post-hoc calibration

"Post-hoc" means **after training**. You don't retrain the model. You train a small second function that maps the model's raw scores to corrected probabilities. It keeps the ranking (mostly) and fixes the numbers.

The key rule: **fit the calibrator on held-out data the model never trained on.** On training data, the model looks better than it really is, so the calibrator learns the wrong correction.

There are three main methods.

**1. Platt scaling.** Fit a logistic regression on the model's score: corrected = sigmoid(a × score + b). It has only two parameters, so it works with little data (a few hundred examples). It assumes the miscalibration has a simple S-curve shape, which is often roughly true.

**2. Isotonic regression.** Fit a step function that can take any shape, with one constraint: it can only go up (higher raw score always means higher or equal corrected probability). It's more flexible than Platt but needs more data (a few thousand examples) or it overfits and produces jagged steps.

**3. Temperature scaling.** For neural networks: divide the logits by a single learned number T before the softmax. T > 1 softens overconfident predictions. Since it's a single parameter, it can't overfit, and it never changes the ranking. It's the standard choice for your encoder.

**Which to use:**

| Situation | Method |
|---|---|
| Text encoder | Temperature scaling |
| Tree model, small calibration set | Platt scaling |
| Tree model, a few thousand+ held-out examples | Isotonic regression |
| You downsampled negatives | Apply the known prior correction, or simply fit Platt/isotonic on held-out data with the real class balance |

## In practice

```python
from sklearn.calibration import CalibratedClassifierCV, calibration_curve

# cv=5 fits the calibrator on held-out folds, avoiding the leakage problem
calibrated = CalibratedClassifierCV(lgbm_model, method="isotonic", cv=5)
calibrated.fit(X_train, y_train)

probs = calibrated.predict_proba(X_test)[:, 1]
actual_rate, predicted_rate = calibration_curve(y_test, probs, n_bins=10)
# plot predicted_rate vs actual_rate: should lie on the diagonal
```

For your pipeline, calibrate the encoder with temperature scaling before stacking it into the tree model, then calibrate the tree model's final output, since that's the number the cost rule uses. Recheck calibration monthly on recent traffic, because drift breaks calibration well before it noticeably hurts ranking.

---

## User

so regardless you are saying that feature based ml models is better right.

---

## Claude

Not quite. My claim is narrower than "feature-based models are better."

**What I'm saying:** for your setup, the feature-based model is the better *starting point* and the better *final decision layer*. That's because you have operational signals (tool failures, repeat contacts, queue load, customer tier) that a text model can't see, and because tree models are cheap, need less data, are easy to calibrate, and are easy to explain.

**What I'm not saying:** that they predict handoffs better in general. The text encoder can win when:
- **Most of the signal is in the language.** If your conversations rarely involve tool calls or account context, and failures show up mainly as subtle frustration or confusion, the encoder will capture things hand-built features miss.
- **You have lots of labeled data.** With tens of thousands of labeled conversations, a fine-tuned encoder often learns patterns you'd never think to build as features.
- **Your operational data is weak or messy.** Missing or unreliable logs remove the tree model's main advantage.

**What usually works best** is the combination: the encoder's probability fed into the tree model. Each sees what the other misses.

So the recommendation is about order and structure, not a winner:
1. Build the tree model first. It's fast to ship and gives you a baseline.
2. Add frozen-embedding features. This is cheap and often gets most of the text signal.
3. Add the fine-tuned encoder, stacked into the tree model.
4. Keep whichever version wins on your held-out data by enough to justify its cost.

Your data decides the answer. If the encoder alone beats the tree model on your evaluation, use that.

---

## User

well calibration would be needed in a thrshold based thing then why dont we use labels for target variable over here

---

## Claude

Good question. The answer has two parts: we *do* train on labels, but the model should still output a probability rather than a hard yes/no.

## Training already uses labels

The target variable is the 0/1 label (1 = this conversation needed a human). That doesn't change. The question is what the model outputs at prediction time.

Every classifier, including LightGBM and the encoder, internally produces a score or probability. When you ask for a hard label (`predict()` instead of `predict_proba()`), it just applies a threshold to that score, usually 0.5. So "predicting the label directly" still involves a threshold; you've only hidden it and fixed it at a default.

## Why a hard label is a bad output here

**1. The default 0.5 cutoff is almost always wrong for rare events.** If 5% of conversations need a human, the model will rarely output a probability above 0.5, so it predicts "no handoff" nearly every time. That looks great on accuracy and catches almost no real failures.

**2. You lose the ability to adjust.** With a probability, you can change the decision without retraining:
- Agents are idle: escalate at P > 0.3
- Agents are overloaded: escalate only at P > 0.7
- High-value customer: lower the cutoff

With a hard label, every one of these changes requires retraining.

**3. You lose ranking.** If agents can take 500 handoffs an hour, you want the 500 most likely failures. Hard labels give you an unordered set of "yes" predictions with no way to prioritize.

**4. Stacking needs scores.** The encoder's output feeds into the tree model. A probability like 0.82 carries far more information than a bare "1."

## When you can skip calibration

You're right that calibration isn't always necessary. **If you pick the threshold empirically and keep it fixed, ranking is all you need:**

1. Get probabilities on a held-out validation set.
2. Try many cutoffs (0.1, 0.15, 0.2, …) and compute the actual cost at each, using real outcomes: agent cost for escalations, failure cost for missed cases.
3. Choose the cutoff with the lowest total cost.

That works even with miscalibrated scores, because you're only using the order of the scores, not their exact values.

**You need calibration when the threshold is computed from changing inputs**, as in the cost formula:

```
escalate if P × cost of failure > cost of agent time
```

Here P is used as an actual probability, and the threshold moves with queue load or customer value. You can't tune one fixed cutoff for every situation in advance, so P has to mean what it says.

## Another option: put costs into training

You can also include costs during training through class weights or sample weights (e.g., missing a failing high-value customer counts 10× more). The model then learns the trade-off directly. The downside is that whenever costs change, you have to retrain. For that reason, it's usually more practical to keep the model as a probability estimator and apply costs at decision time.

## Summary

| Approach | Needs calibration? | Flexible at runtime? |
|---|---|---|
| Hard label (default 0.5) | No | No, and usually a bad cutoff |
| Fixed threshold tuned on validation data | No | No |
| Cost formula with dynamic inputs | **Yes** | **Yes** |
| Costs as training weights | No | No (retrain to change) |

A practical path: start with a fixed threshold tuned on validation data, which needs no calibration. Add calibration once you want the threshold to adapt to queue load or customer value.

---

## User

how do we curate data for this though. Some ideas that I can give are: 

1. All the features of the feature based ML model are derived by sending the conversation logs through the LLM. Remove the bot's replies in the conversation and tell the LLM that these are the user conversations and through these curate a data that tells if human agent accesss needs to be given or not. 
2. Different types of llms (multiple llms) are used and according to the features, logs and stuff find out if agent access or not. Repeat this process and find the value of target variable through voting. 


These are some ideas, maybe refine them and give better ones.

---

## Claude

Your ideas have the right instinct: use LLMs to label at scale, and combine several of them to reduce errors. But each has a flaw worth fixing first.

## Problems with the two ideas

**Idea 1: removing bot replies and having the LLM judge from user messages**

- **Removing bot replies removes the main signal.** Most handoffs are needed because the bot failed: wrong answers, loops, misunderstanding, or being unable to perform an action. You can't see any of that without the bot's side. "I already told you that" only makes sense next to what the bot said. Keep both sides.
- **The LLM's opinion isn't the truth.** An LLM judging "should this go to a human?" gives you its interpretation, not what actually happened to the customer. Your model's ceiling becomes the LLM's judgment, including its biases.
- **Hindsight bias.** If the LLM reads the whole conversation, it knows how it ended. Your production model only sees the conversation up to the current turn, so labels must reflect what was knowable at each turn.
- **LLM-derived features don't work in production.** If training features come from an LLM, then in production you'd need an LLM call per turn to compute them, which defeats the purpose of a cheap model. Using an LLM for labels offline is fine. Features must be computable cheaply at inference time.

**Idea 2: voting across multiple LLMs**

- **Voting only helps if the voters make different mistakes.** LLMs are trained on similar data and share many of the same biases, so they often agree on the same wrong answer. Majority voting reduces random noise but not shared bias.
- **Equal votes ignore accuracy.** If one model is right 90% of the time and another 65%, giving them equal weight wastes the better one.
- **It costs several times more** than a single good judge, for limited gain.

## Better approach: several label sources, combined carefully

### Step 0: Define what "needs a human" means

Before labeling anything, write a definition with reason categories:

| Category | Example |
|---|---|
| **Capability gap** | Needs an action the bot can't perform (refund exception, account change) |
| **Bot failure** | Misunderstanding, looping, wrong information |
| **Customer preference** | Explicitly asks for a human |
| **Risk** | Legal threats, fraud, safety, a vulnerable customer |

Labeling the reason as well as yes/no makes labels more consistent and gives you more useful training data.

Also define the label **per turn**: at which turn should the handoff have happened? Turns before that point are labeled 0, turns at or after it 1. That matches what the production model predicts.

### Source 1: Outcome labels from your logs (most important)

These come from what actually happened, so they need no LLM and are available for every conversation:
- The customer explicitly asked for a human
- The customer abandoned mid-conversation
- The customer contacted support again within 48 hours about the same issue
- Low CSAT score
- After handoff, **what the agent had to do.** Agent dispositions, notes, and actions are very valuable here. If the agent performed an account action or a policy exception, the handoff was needed. If the agent just repeated an FAQ answer, the bot could have handled it.

Each signal is noisy on its own, but they reflect real outcomes rather than opinions.

### Source 2: A small human-labeled gold set

Have experienced agents label 300 to 1,000 conversations using the definition from Step 0, with two people labeling each conversation. Measure how often they agree (Cohen's kappa). If two agents only agree 70% of the time, no model will reach 95%, and the definition needs work.

This gold set is not for training. It's for **measuring how accurate every other label source is.**

### Source 3: An LLM judge, done properly

This is the refined version of your first idea:
- Give it the **full conversation including bot replies, but only up to turn t.** Ask: "Given only this, should we hand off now?" Run it at several cut points per conversation, or ask it to identify the earliest turn where handoff became necessary.
- Give it the written rubric from Step 0, and ask for structured output: `{handoff: yes/no, turn, reason_category, confidence}`.
- **Measure it against the gold set.** If its agreement with humans is low, improve the rubric and prompt. You could even run GEPA on the judge prompt, using the gold set as the metric.
- Run it through the batch API, which is typically much cheaper than real-time calls.
- Remove personal information (names, phone numbers, account details) before sending logs to any external model.

### Combine the sources with weak supervision

This is the refined version of your second idea. Instead of LLMs voting equally, treat **every source** as a noisy labeler: the outcome signals, a few rules (e.g., "customer typed 'agent'"), and one or two LLM judges. Then use a **label model** that learns how accurate each source is from their agreements and disagreements, and weights them accordingly. Snorkel (Ratner et al., 2017) is the standard framework for this. The underlying idea goes back to Dawid and Skene (1979), who estimated annotator accuracy without knowing the true answers.

Benefits over plain voting:
- Sources are weighted by estimated accuracy
- Outcome signals and LLM judgments both contribute
- The output is a probability per example, which you can use as a soft training target or to filter out low-confidence examples

### Use disagreement to direct human effort

When sources strongly disagree (the LLM says handoff, outcome signals say resolved), send those cases to human reviewers. That's where human labels improve the dataset most (active learning). Over time, the gold set grows exactly where your labels are weakest.

## Handling the selection bias

Your current turn limit means the bot never continues past N turns, so you have no data on whether it could have succeeded. Two fixes:
- **Agent transcripts after handoff:** if the agent resolved it in one simple message, the handoff probably wasn't needed.
- **A small exploration slice:** let 1 to 2% of conversations continue past the limit when there are no frustration signals, and record outcomes.

## Pipeline summary

```
logs ─► redact PII
     ├─► outcome signals (abandonment, repeat contact, CSAT, agent actions) ─┐
     ├─► rules (explicit human request, legal keywords, tool failures) ─────┤
     └─► LLM judge (prefix up to turn t, rubric, batch API) ────────────────┤
                                                                            ▼
                                            label model (Snorkel-style weighting)
                                                                            │
                         gold set (human, double-labeled) ──► validates everything
                                                                            │
                         high-disagreement cases ──► human review ──► grows gold set
                                                                            ▼
                                       per-turn labels ──► train LightGBM / encoder
```

Features stay cheap and computed in code or with small models; LLMs are used only offline for labeling.

## Where to start

1. Write the definition and reason categories.
2. Pull outcome signals from logs. You may already have enough for a first model.
3. Have agents label around 300 conversations as the gold set.
4. Add one LLM judge and check it against the gold set.
5. Combine the sources with a label model once you have three or more.

Do you have access to agent-side data after handoff (notes, disposition codes, actions taken)? That's the most valuable label source, and it determines how much you need to rely on LLM judges.

---

## User

for idea 2 would choosing models of different famillies be good. ?

---

## Claude

> **Web search:** Replacing Judges with Juries panel of LLM evaluators diverse model families

> - [Replacing Judges with Juries: Evaluating LLM Generations with a Panel of Diverse Models](https://arxiv.org/pdf/2404.18796)
> - [Replacing Judges with Juries:](https://arxiv.org/html/2404.18796v2)
> - [Replacing Judges with Juries: Evaluating LLM Generations with a Panel of Diverse Models](https://alphaxiv.org/abs/2404.18796)
> - [alphaxiv.org](https://alphaxiv.org/overview/2404.18796v2)
> - [Apr 29, 2024](https://cohere.com/research/papers/replacing-judges-with-juries-evaluating-llm-generations-with-a-panel-of-diverse-models-2024-04-29)
> - [arxiv.org](https://arxiv.org/pdf/2404.18796v1)
> - [arxiv.org](https://arxiv.org/abs/2404.18796v2)
> - [@naomi white](https://www.alphaxiv.org/@naomi-white)
> - [DEV Community](https://dev.to/aimodels-fyi/replacing-judges-with-juries-evaluating-llm-generations-with-a-panel-of-diverse-models-mpa)
> - [Replacing Judges with Juries Evaluating LLM Generations with a Panel of Diverse Models 174d3cfe027d802b92e8de4da2ab8570](https://nova-quicksand-5ae.notion.site/Replacing-Judges-with-Juries-Evaluating-LLM-Generations-with-a-Panel-of-Diverse-Models-174d3cfe027d802b92e8de4da2ab8570)

> **Web search:** Correlated errors in large language models agree on wrong answers same provider

> - [When LLMs Agree, Are They Right? Auditing Self-Consistency and Cross-Model Agreement as Confidence Signals](https://arxiv.org/pdf/2607.08065)
> - [Correlated Errors in Large Language Models](https://arxiv.org/html/2506.07962v1)
> - [icml.cc](https://icml.cc/virtual/2025/poster/44225)
> - [Literature Review Correlated Errors in Large Language Models](https://www.themoonlight.io/review/correlated-errors-in-large-language-models)
> - [Correlated Errors in Large Language Models](https://slideslive.com/39041839/correlated-errors-in-large-language-models?locale=cs)
> - [Correlated Errors in Large Language Models](https://slideslive.com/39041839/correlated-errors-in-large-language-models?locale=de)
> - [Correlated Errors in Large Language Models](https://slideslive.com/39041839)
> - [AI DevelopmentFramework13 min readPublished August 2, 2026](https://www.digitalapplied.com/blog/cross-model-review-consensus-verification-2026)
> - [skip to main content](https://par.nsf.gov/biblio/10616986)

Yes, it helps, but less than you might expect. Different families reduce shared errors somewhat; they don't remove them.

## The evidence

**In favor:** Cohere's "Replacing Judges with Juries" (2024) found that a panel of several smaller models outperformed a single large judge, showed less intra-model bias because the models came from different families, and cost over seven times less. Their panel used three models from three different families (Command R, Haiku, and GPT-3.5) and had the highest Cohen's kappa agreement with human judgments.

**The caveat:** "Correlated Errors in Large Language Models" (ICML 2025) studied over 350 models. It found that models from the same provider, with the same base architecture, or of similar size have more correlated errors, which supports picking across families. But it also found that larger and more accurate models have highly correlated errors even across different architectures and providers. On one benchmark, when two models were both wrong, they picked the same wrong answer about 60% of the time, compared with one in three by chance. Their conclusion: independent components are not enough to get independent outputs.

So: different families are better than the same family, but don't treat their votes as independent.

## One specific reason it matters for you

Your bot runs on Gemini. If your judges are mostly Gemini models, they may be more lenient toward the bot's own replies. A review of the correlated-errors paper notes that LLM-as-judge inflation is especially strong for models from the same provider or architecture as the judge, reflecting a kind of self-preference. Since your labels judge whether *the bot* failed, include at least one or two non-Gemini judges.

## Getting more diversity than model family alone

Diversity in what each judge looks at matters as much as which model it is.

**1. Give judges different perspectives.** Use different questions instead of asking every model the same one:
- Customer judge: "Is this customer frustrated or getting worse?"
- Bot-failure judge: "Did the bot misunderstand, loop, or give wrong information?"
- Capability judge: "Does this request need an action the bot can't take?"

Each judge makes different kinds of mistakes, and the answers map directly onto your reason categories.

**2. Include non-LLM sources.** Outcome signals (abandonment, repeat contact, agent actions) are the most independent "votes" you have, since they don't come from any language model. That's why they belong in the label model alongside the LLM judges.

**3. Measure diversity instead of assuming it.** On your gold set, check how often each pair of judges is wrong on the same examples. Keep judges whose errors overlap least, even if one is individually a bit weaker. A weaker judge with independent errors adds more than a strong judge that copies another's mistakes.

## How to combine them

- **Don't use plain majority voting.** Weight judges by accuracy, using the label model (Snorkel or Dawid-Skene style) or weights estimated from the gold set.
- **Treat unanimous agreement carefully.** When all judges agree but outcome signals disagree, that's a likely shared error. Send those cases to human review.
- **Use smaller, cheaper models from each family.** Following the PoLL result, three small models from different families can beat one large model at a fraction of the cost.

## A practical setup

| Source | Purpose |
|---|---|
| Small model, family A (non-Gemini) | Bot-failure judge |
| Small model, family B (non-Gemini) | Customer-state judge |
| Gemini Flash | Capability judge (rubric-based, less exposed to self-preference) |
| Outcome signals | Independent ground truth |
| Rules | Clear-cut cases (explicit human request, legal keywords) |
| **Label model** | Weights all of the above, validated on the gold set |

Short answer: yes, choose different families, but get diversity mainly from different perspectives and non-LLM signals, and verify it on the gold set.

---

## User

but if we keep both sides then the model will be trained on data of which the outcome is known no ? how do we solve that ?

---

## Claude

Good instinct to check, but including the bot's replies isn't the leak. The leak comes from **future information**, not from the bot's side.

## Inputs vs. labels

Supervised learning always trains on examples where the outcome is known. That's how the model learns. The rule is narrower than "don't let outcomes into the data":

- **The label can come from the future.** "This conversation ended in abandonment" is fine as a target.
- **The inputs can only contain what was available at prediction time.**

At turn t in production, the bot's replies up to turn t have already been sent, so the model can legitimately see them. Using them in training matches what the model will see in production.

```
Turn:     1      2      3      4      5      6 (handoff)    7 (agent)
        [user  bot   user  bot   user  bot] │ ✗ future     ✗ future
        └──── input for predicting at turn 3 ┘
Label for turn 3: did this conversation need a human by this point? (may use future outcomes)
```

## Where leakage actually comes from

**1. Turns after t.** The training example for turn t must be cut off at turn t. If the full conversation is in the input, the model sees the ending and learns nothing useful. Build one training row per turn, each using only the prefix up to that turn.

**2. Text that encodes the handoff itself.** Remove anything that only exists because a handoff happened or was about to happen:
- Bot messages like "I'm connecting you to an agent" or "Would you like to speak to someone?"
- System messages ("transferred to queue"), agent turns, end-of-chat markers

If these stay in, the model learns "the word 'agent' in a bot reply means handoff," which is trivially true and useless.

**3. Features computed over the whole conversation.** Total conversation length, final sentiment, total number of apologies, or whether a CSAT survey was shown all summarize the full conversation. Compute every feature as a running value up to turn t.

**4. The turn-limit artifact.** Your current rule escalates at turn N, so "turn count = N" predicts handoff perfectly in historical data. This is why labels should be based on outcomes, not on whether a handoff happened. If you keep turn count as a feature, also check the model isn't simply relearning the old rule (look at its feature importance).

## A subtler issue: labels that are too far ahead

Even with correct prefixes, consider a conversation that was fine for 4 turns and then went badly. If you label every turn as "needs a human," turn 1 gets labeled positive even though nothing was wrong yet. The model then learns to escalate conversations that look completely normal.

The fix is the per-turn labeling from before: identify the **earliest turn where handoff became necessary**. Label turns before it 0 and turns at or after it 1. The LLM judge does this by reading prefixes and marking the first turn where handoff was warranted, or by examining the full conversation and naming that turn explicitly.

## Quick leakage check

Train the model, then look at the top features (SHAP values or feature importance) and a sample of its most confident predictions. If its best signal is something you couldn't have known at that turn, such as a handoff phrase, an agent message, or the exact turn limit, you have a leak. Real signals look like rephrasing, sentiment trends, and tool failures.

---

## User

explain the ideas of data curation for this

---

## Claude

Here's the full data curation process for the handoff model, end to end, with the reason behind each step.

## The goal

You want a table where **each row is one turn of one conversation**, containing:
- **Features:** everything knowable at that turn
- **Label:** whether a human was needed by that point
- **Weight or confidence:** how much to trust that label

Every step below exists to make the features honest (no future information) and the labels accurate (close to the truth).

## Step 1: Define the target

Decide what "needs a human" means before touching data, or every labeling source will interpret it differently.

- **Reason categories:** capability gap, bot failure, customer preference, risk
- **Timing:** the label is about the *earliest turn* where handoff became necessary, not just whether the conversation should have been handed off at some point

Write this as a one-page rubric. Human labelers and LLM judges both use it.

## Step 2: Collect and clean raw logs

- **Gather conversations** with timestamps, all bot and user messages, tool/API call results, customer metadata, and what happened afterward (handoff, agent actions, CSAT, repeat contacts).
- **Redact personal information** (names, phone numbers, account IDs) before any external model sees the data.
- **Tag the bot version** for each conversation. When you change the prompt or model, bot behavior changes and old data partly reflects a different bot.
- **Remove junk:** test conversations, spam, sessions that broke from technical errors, and duplicates.

## Step 3: Build per-turn rows without leakage

Each conversation of length n becomes up to n rows. For the row at turn t:
- **Input:** messages from turn 1 to t only
- **Remove handoff artifacts:** bot messages offering a transfer, system transfer notices, agent turns
- **Compute features as running values:** sentiment trend so far, rephrase count so far, tool failures so far, never totals over the whole conversation

This is what prevents the model from learning from information it won't have in production.

## Step 4: Label from several sources

Each source has different strengths and errors.

**a) Outcome signals (most important).** These record what actually happened:

| Signal | Suggests |
|---|---|
| Customer explicitly asked for a human | Positive |
| Abandoned mid-conversation | Positive (weak) |
| Repeat contact within 48h on the same issue | Positive |
| Low CSAT | Positive (weak) |
| Agent performed an action the bot can't do | Positive |
| Agent resolved with a simple FAQ answer | Negative (handoff wasn't needed) |
| Resolved by the bot, no repeat contact | Negative |

**b) Rules.** Clear-cut cases: legal threats, fraud keywords, repeated identical tool failures.

**c) LLM judges.** Multiple judges with different perspectives (bot failure, customer state, capability), drawn from different model families and including non-Gemini models. Each reads the rubric and marks the earliest turn where handoff was warranted, plus a reason.

**d) Human gold set.** 300 to 1,000 conversations labeled by experienced agents, two per conversation, with agreement measured. Used to **validate** the other sources, not as the main training data.

## Step 5: Combine into one label

Use a label model (Snorkel or Dawid-Skene style) that learns how reliable each source is from patterns of agreement and disagreement, then produces a probability per row. Check its accuracy against the gold set.

You then have three choices:
- Use the probability directly as a **soft label**
- Convert it to 0/1, and **drop rows with uncertain labels** (e.g., between 0.4 and 0.6)
- Use it as a **sample weight**, so confident labels count more

## Step 6: Route disagreements to humans

When sources strongly disagree, especially when LLM judges agree with each other but outcome signals say the opposite, send those conversations to human reviewers. Add them to the gold set. Human effort goes where labels are weakest (active learning), and these are often the most informative training examples.

## Step 7: Fix selection bias

Historical data reflects your current turn-limit policy, so you never observe whether the bot could have succeeded past turn N.
- **Agent transcripts after handoff** reveal whether the handoff was needed.
- **A small exploration slice** (1 to 2% of conversations without frustration signals continue past the limit) generates data your current policy never produces.

## Step 8: Balance and sample

Handoffs are rare, so:
- **Stratify by intent** so rare-but-important intents (billing disputes, account security) aren't drowned out by common simple ones.
- **Include hard negatives:** long or difficult conversations the bot still resolved. These teach the model that "long" doesn't mean "failing."
- If you downsample negatives for training speed, **calibrate afterward** (as discussed earlier), since downsampling shifts probabilities.

## Step 9: Split correctly

- **By time:** train on older data, validate and test on the most recent weeks. This simulates production.
- **By customer:** the same customer shouldn't appear in both train and test.
- **Never split rows of the same conversation** across train and test. Neighboring turns are nearly identical.

## Step 10: Run quality checks before training

- Label rate per intent and per week: sudden jumps usually mean a pipeline bug or a bot change.
- Agreement of each source with the gold set: drop or down-weight unreliable sources.
- Leakage check: train a quick model and inspect top features. A handoff phrase or the exact turn limit at the top means leakage.
- Read 50 random rows yourself. This catches problems no metric shows.

## Step 11: Keep it updated

- Version every dataset with the rubric version, the label sources used, and the bot version.
- Re-label new traffic regularly (weekly or monthly).
- Retrain when the bot changes significantly, because handoff patterns change with it.

## The whole pipeline

```
raw logs ─► clean + redact PII + tag bot version
        ─► per-turn rows (prefix only, artifacts removed, running features)
        ─► label sources: outcomes │ rules │ LLM judges │ human gold set
        ─► label model (weights sources, validated on gold set)
        ─► disagreements ─► human review ─► gold set grows
        ─► exploration data + agent transcripts (fix selection bias)
        ─► stratify, add hard negatives
        ─► time + customer split
        ─► quality checks ─► train ─► calibrate
        ─► version, monitor, refresh
```

## Where to start

If you're building this now: Steps 1, 2, 3, and 4a (outcome labels) are enough for a first model. Add the gold set next, so you can measure label quality. Add LLM judges and the label model once you can see where outcome labels are weakest.

---

## User

its the swiggy chatbot so give me answer in contexst to that.

---

## Claude

Here's the data curation plan adapted to Swiggy. The structure is the same as before; what changes is the intents, the signals, the outcome labels, and some risks specific to food delivery.

## What's different about Swiggy

- **Live orders are urgent.** A customer whose biryani is 40 minutes late needs a different handoff threshold than someone asking about yesterday's refund. Every row should record whether the order is still in progress.
- **Every contact is tied to an order ID.** That makes outcome labels much easier, because you can connect repeat contacts, refunds, and agent actions to the same order.
- **Money is involved in most conversations.** Refunds, compensation, and coupons mean some customers push hard specifically to reach a human who might give more. Your labels must not reward that (more on this below).
- **Several business lines.** Food delivery, Instamart, and Dineout have different issues and policies, so stratify and possibly model them separately.
- **Language.** Expect Hinglish and regional languages. Your judges, embeddings, and classifiers need to handle code-mixed text.

## Step 1: Define "needs a human" for Swiggy

Your support SOPs already contain most of this. Use them as the rubric:

| Category | Swiggy examples | Handling |
|---|---|---|
| **Safety / risk** | Foreign object in food, food poisoning, allergic reaction, delivery partner misconduct or harassment, accident | Hard rule: escalate immediately, no model needed |
| **Capability gap** | Compensation above the bot's limit, payment deducted but order failed, account blocked, multi-order or complex disputes | Escalate when detected |
| **Bot failure** | Looping on "where is my order," referencing the wrong order, wrong refund information | Model should detect |
| **Customer preference** | "Mujhe agent se baat karni hai," "connect me to a human" | Rule + model |
| **Doesn't need a human** | Status checks, refunds within the bot's authority, coupon questions, cancellation within policy | Negative |

Separate "the customer wanted a human" from "the case needed a human." A customer demanding more compensation than policy allows may want an agent, but if the agent will just repeat the bot's decision, the handoff only adds agent cost.

## Step 2: Swiggy-specific features (per turn, running values)

**Order context** (from your systems, not the chat):
- Order status: placed, preparing, picked up, delivered, cancelled
- Minutes past the promised ETA, and whether the delay is still growing
- Order value and number of items
- Business line: Food / Instamart / Dineout
- Payment method: prepaid vs COD, and payment gateway status
- Whether the delivery partner is reachable

**Customer context:**
- Order frequency and tenure (a loyal weekly customer is worth more to retain)
- Swiggy One membership
- Prior contacts about this same order
- Past complaint and refund rate (abuse risk, see below)

**Conversation signals** (same as before, adapted):
- The customer rephrasing the same issue ("order kahan hai" → "still not here" → "where is my food")
- Whether the bot already offered a refund or coupon that the customer rejected
- Whether the customer uploaded a photo (for missing, wrong, or damaged items)
- Tool failures, such as refund API errors or order lookup failures
- Sentiment trend, including Hinglish frustration markers

**Environment:**
- City, time of day (dinner peak), weather such as rain (delays spike), festival or event days

## Step 3: Outcome labels in Swiggy terms

| Signal | Label meaning |
|---|---|
| Repeat contact about the **same order ID** within 24 to 48h | Strong positive: the first contact didn't resolve it |
| Agent issued compensation **above the bot's limit** | Positive (capability gap) |
| Agent did investigation or account work (payment reconciliation, unblocking) | Positive |
| Agent **upheld the bot's decision** with no new action | Handoff likely unnecessary (negative or weak) |
| Customer explicitly requested a human | Positive (preference) |
| Customer abandoned during a live delayed order | Positive (weak) |
| Low CSAT after the chat | Positive (weak) |
| Chargeback or bank dispute raised later | Strong positive |
| Customer **stopped ordering** in the following weeks | Positive (weak, delayed; useful for retention-weighted costs) |
| Resolved by the bot, no repeat contact, customer reordered | Negative |

Agent disposition codes and actions are your best label source. Ask whoever owns the agent tooling for access early.

## The biggest Swiggy-specific risk: refund abuse

If you label "agent gave extra compensation" as positive without care, the model learns that **customers who complain aggressively should go to a human**, and those are often the customers abusing refunds. You'd be building a system that routes abusers to the people most likely to pay them.

Mitigations:
- **Label by policy correctness, not customer pressure.** The question is "did this case legitimately need something the bot couldn't do?", not "did escalating get the customer more money?"
- **Exclude or flip labels for conversations later flagged as fraud or abuse** by your trust and safety systems.
- **Include an abuse-risk score as a feature,** so the model can learn that high-risk accounts with a "missing item" complaint don't need escalation the same way a first-time complainer does.
- **Audit the model by abuse-risk segment** before launch: check that escalation rates aren't highest among the riskiest accounts.

## LLM judges, adapted

- Give judges **order context alongside the chat**: order timeline, ETA breach, refunds already issued, the bot's compensation limits. Without these, a judge can't tell whether the bot failed or was correctly following policy.
- Include your SOP summary in the rubric.
- Check judge accuracy on Hinglish conversations separately on the gold set. Some models are noticeably weaker on code-mixed text.
- Use at least one non-Gemini judge, since the bot runs on Gemini.

## Gold set

- Labelers: experienced support agents or team leads who know the SOPs.
- Stratify the 500 to 1,000 conversations across food / Instamart / Dineout, live vs post-delivery, major cities, languages, and top intents. Oversample safety and payment cases even though they're rare.
- Measure agreement per intent. Low agreement on, say, "spilled food" means the SOP is ambiguous there, and the rubric needs clarifying.

## Sampling, splits, and scale

- **You don't need to LLM-label everything.** At Swiggy's volume, outcome labels can cover every conversation for free. Use LLM judges on a stratified sample (tens of thousands of conversations) through the batch API.
- **Stratify by** business line, intent, live vs post-delivery, city tier, and language.
- **Hard negatives:** long conversations about delayed live orders that the bot resolved (e.g., by giving accurate ETA updates and the customer stayed). These teach the model that "delayed order + long chat" doesn't automatically mean escalate.
- **Split by time, and watch for seasonality.** Monsoon delays, festival peaks, and big cricket match nights change support patterns. Make sure test data covers at least one unusual period, or the model will fail on the first rainy Friday.
- **Split by customer,** so heavy users don't appear in both train and test.

## Selection bias, carefully

The exploration slice (letting some conversations continue past the turn limit) should **exclude live orders with large ETA breaches and anything touching safety or payment failures.** Only explore on low-risk cases such as post-delivery refund queries without frustration signals. Agent transcripts after handoff remain the safest source for learning which handoffs were unnecessary.

## Where to start

1. Turn the support SOPs into the rubric (Step 1), and implement safety categories as hard rules immediately. That's a quick win regardless of the model.
2. Join chat logs with order data and agent dispositions by order ID to build outcome labels.
3. Build the gold set with agents, stratified as above.
4. Train the first LightGBM on order context + conversation features + outcome labels.
5. Check escalation rates by abuse-risk segment before going live.

Do you have access to agent dispositions and the trust and safety abuse flags? Those two data sources decide how clean your labels can be.

---

## User

alright then lets go to the model part. What were u suggesting in feature based ML models and text encoders. what was the ensemble method and what was purely ml based method

---

## Claude

There were four variants, ranging from purely feature-based to fully combined. Here they are side by side, in Swiggy terms.

## Option 1: Purely feature-based ML (the baseline)

**What it is:** a gradient-boosted tree model (LightGBM or XGBoost) trained on structured numbers and categories computed for each turn. No model reads the raw text directly.

**Inputs, one row per turn:**

| Type | Examples |
|---|---|
| Order context | Order status, minutes past ETA, order value, Food / Instamart / Dineout, prepaid vs COD, delivery partner reachable |
| Customer context | Order frequency, Swiggy One, prior contacts on this order, abuse-risk score |
| Conversation signals (computed by code) | Turn number, number of times the customer rephrased, bot apologies so far, refund offered and rejected, tool/API failures, photo uploaded |
| Simple text signals | Keywords ("agent," "human," "refund nahi chahiye"), message length trend, all caps, repeated "?" or "!" |
| Environment | City, hour of day, rain, festival day |
| Free LLM signal | The main bot's own `needs_human` flag from its structured output |

**Output:** P(this conversation needs a human now), calibrated, then passed to the threshold or cost rule.

**Strengths:** microseconds per prediction, works with modest data, easy to explain ("escalated because ETA breach is 35 minutes and the customer rephrased 3 times"), easy to calibrate.
**Weakness:** misses meaning that no feature captures, like polite-but-furious messages or "this is the third time this month."

```
order + customer + conversation features ──► LightGBM ──► P(handoff)
```

## Option 2: Feature-based ML + frozen embeddings (the cheap middle option)

**What it is:** still only the tree model, but some features come from a **pre-trained sentence embedding model used as-is, with no fine-tuning** (a multilingual one, for Hinglish). The embeddings produce a few numeric features:
- Similarity between consecutive customer messages (high means the customer is repeating themselves and the bot isn't understanding)
- Similarity to a small set of example frustrated messages
- Sentiment score per turn and its trend

These go into LightGBM as additional columns.

**Why:** it captures much of the text signal at very low cost, and the features remain explainable. Often this option gets most of the benefit of a fine-tuned encoder.

```
features + embedding-derived features ──► LightGBM ──► P(handoff)
```

## Option 3: Text encoder alone

**What it is:** a small transformer (DistilBERT- or ModernBERT-size, a multilingual model, or SetFit) **fine-tuned** to read the last few turns of the conversation (customer and bot, with speaker tags) and output P(needs human).

**Strengths:** understands language nuance and code-mixed text without anyone designing features for it.
**Weaknesses:** can't see order data (ETA breach, refund already issued, abuse risk) unless you insert it into the text; needs more labeled data; harder to explain; needs calibration (temperature scaling).

For Swiggy this alone is weak, because much of the handoff signal lives in order and customer data, not the chat text.

```
last k turns (text) ──► fine-tuned encoder ──► P(handoff)
```

## Option 4: The ensemble (stacking)

**What it is:** the encoder's output becomes **one more feature** for the tree model. The tree makes the final decision using everything.

```
last k turns ──► fine-tuned encoder ──► p_encoder ──┐
                                                    ├──► LightGBM ──► P(handoff) ──► calibrate ──► decision
order + customer + conversation features ───────────┘
```

**Why stacking instead of averaging:** the tree learns *when* to trust the encoder. For example, it can rely on the encoder for food-quality complaints where tone matters, and mostly ignore it when there's already a 45-minute ETA breach with a failed refund API call that explains the situation.

**The rule that makes it work:** generate the encoder's predictions **out-of-fold.** Split training data into k folds, train the encoder on k minus 1 folds, and predict on the remaining fold. Repeat for every fold. Otherwise the encoder's probabilities on its own training data look far too accurate, and the tree over-trusts them.

**Optional cost saving (cascade):** run LightGBM on cheap features first. Run the encoder only when the tree is uncertain (say P between 0.3 and 0.7), then re-score. Most Swiggy chats ("where is my order" with an on-time ETA) are clearly fine, so the encoder runs on a small fraction of turns.

## Summary

| | Reads raw text? | Uses order/customer data? | Cost | Explainable? |
|---|---|---|---|---|
| 1. Pure feature-based | No | Yes | Lowest | High |
| 2. + frozen embeddings | Indirectly | Yes | Very low | High |
| 3. Encoder alone | Yes | Only if inserted into the text | Medium | Low |
| 4. Stacked ensemble | Yes | Yes | Low to medium (lower with cascade) | Medium |

## Suggested order

Build 1 → add 2 → try 4. Compare all three on the same time-based test split using PR-AUC, recall at your agent-capacity budget, and how many turns earlier than the current rule they catch failures. Keep the simplest version whose results are close to the best. Option 3 alone mainly serves as a comparison point for whether text carries signal the features miss.

---

## User

explain option 4

---

## Claude

## The idea

You have two models that see different things:

- **The text encoder** reads the conversation and picks up language: frustration, confusion, sarcasm, Hinglish phrasing like "kitni baar bolun" (how many times do I have to say it).
- **LightGBM** reads structured data: ETA breach, order value, refund already given, abuse-risk score, tool failures.

Stacking means **the encoder's output becomes one input column for LightGBM.** LightGBM makes the final decision, weighing the encoder's view of the text against everything else it knows.

An analogy: the encoder is a colleague who read the chat and says "this customer sounds 80% likely to need a human." LightGBM is the manager who also has the order dashboard. It knows how reliable that colleague usually is, in which situations, and decides.

## The pieces

**1. The text encoder**
- A small multilingual transformer (e.g., a multilingual MiniLM, MuRIL, or IndicBERT-size model), fine-tuned for binary classification.
- Input: the last k turns up to the current turn, with speaker tags, truncated to around 256 to 512 tokens:
  ```
  [USER] order kab aayega, 40 min ho gaye
  [BOT] Your order is on the way and will arrive in 10 minutes.
  [USER] yahi 20 min pehle bhi bola tha
  ```
- Output: `p_encoder`, the probability that a human is needed, based only on the text.

**2. LightGBM**
- Inputs: all the structured features (order, customer, conversation, environment) **plus `p_encoder` as one extra column.**
- Output: the final P(handoff).

**3. Calibration** on the final output, so the probability can be used in the cost rule.

## Training, step by step

### Step 1: Prepare the data

Use the per-turn rows from data curation: each row has the text prefix up to turn t, the structured features up to turn t, and the label.

Hold out the most recent weeks as the **test set** and don't touch it until the end.

### Step 2: Generate encoder predictions out-of-fold

This is the critical step.

**The problem:** if you train the encoder on all training data and then predict on that same data, it will be very confident and mostly correct, because it has seen those examples. LightGBM then learns "p_encoder is almost always right, trust it heavily." In production, on new conversations, the encoder is much less accurate, and LightGBM's trust is misplaced.

**The fix: k-fold out-of-fold prediction.**

```
Training data split into 5 folds: [F1][F2][F3][F4][F5]

Round 1: train encoder on F2–F5 → predict on F1
Round 2: train encoder on F1,F3–F5 → predict on F2
Round 3: train encoder on F1,F2,F4,F5 → predict on F3
Round 4: train encoder on F1–F3,F5 → predict on F4
Round 5: train encoder on F1–F4 → predict on F5
```

Now every training row has a `p_encoder` produced by a model that **never saw that row**, so it's as reliable as the encoder will be in production. LightGBM learns realistic trust.

**How to split the folds:**
- **Group by conversation:** all turns from one conversation go in the same fold. Neighboring turns are nearly identical, so splitting them would leak.
- **Preferably group by customer too,** so a heavy user's style doesn't leak across folds.

### Step 3: Train LightGBM

Train LightGBM on the structured features plus the out-of-fold `p_encoder` column. Use a time-based validation split for tuning and early stopping.

### Step 4: Train the final encoder

Train one more encoder on **all** training data. This is the version you deploy. Its predictions are what LightGBM will see in production, and since it trained on more data, it's slightly better than the fold models, which is fine.

### Step 5: Calibrate

Calibrate LightGBM's output on held-out data (isotonic regression if you have thousands of examples, Platt scaling otherwise).

### Step 6: Evaluate on the test set

Compare against Option 1 (LightGBM without `p_encoder`) on the same test set. If the stacked version doesn't improve PR-AUC or recall at your agent-capacity budget by a meaningful margin, the encoder isn't worth running.

## What LightGBM learns from this

Because trees split on combinations of features, LightGBM can learn patterns like:

- *ETA breach > 30 min and refund API failed:* escalate, mostly regardless of `p_encoder`, since the situation already explains the problem.
- *Order delivered on time, food-quality complaint:* rely heavily on `p_encoder`, since tone is what separates "slightly cold" from "this made my kid sick."
- *High abuse-risk score:* discount a high `p_encoder`, since aggressive language from this group often isn't a real handoff need.
- *Hinglish-heavy chats:* the tree can learn whether the encoder is more or less reliable on them, if you include a language feature.

A simple average of the two models can't do any of this.

## In production

```
new customer message
   │
   ├─► compute structured features (order API, customer data, chat stats)
   │
   ├─► LightGBM on features alone → is it clearly fine or clearly failing?
   │        │
   │        ├─ clear (P < 0.3 or > 0.7) → use this, skip the encoder   [cascade]
   │        │
   │        └─ uncertain → run encoder on last k turns → p_encoder
   │                       → LightGBM with p_encoder → final P
   │
   └─► calibrated P → threshold or cost rule → escalate or continue
```

The cascade is optional. If you use it, you need two LightGBM models: one without `p_encoder` for the first pass, and the stacked one for uncertain cases. Most Swiggy chats ("where is my order" with an on-time ETA) end at the first step, so the encoder runs on a small share of turns. On CPU, a small encoder takes milliseconds per prediction.

## Alternative: embedding vector instead of probability

Instead of the encoder's probability, you could feed its embedding vector (or a compressed version, e.g., 16 to 32 dimensions after PCA) into LightGBM. That gives the tree more information, but trees aren't great with dense embedding features, it overfits more easily, and it's harder to explain. Start with the single probability column; try embeddings only if you have lots of data and the probability version plateaus.

## Maintenance

- **Retrain both together.** If you retrain only the encoder, its output distribution shifts, and LightGBM's learned trust no longer fits. When retraining, redo the out-of-fold step and retrain LightGBM.
- **Retrain when the bot changes significantly.** New prompts or a new model change what bot replies look like, which changes what the encoder sees.
- **Monitor `p_encoder` drift** in production. If its average shifts noticeably (e.g., during a festival or after a new feature launch), the encoder may need fresh data.

## Pseudocode

```python
from sklearn.model_selection import GroupKFold
import lightgbm as lgb
import numpy as np

oof_p = np.zeros(len(train))
gkf = GroupKFold(n_splits=5)

# Step 2: out-of-fold encoder predictions
for fit_idx, pred_idx in gkf.split(train, groups=train["conversation_id"]):
    enc = fine_tune_encoder(train.iloc[fit_idx]["text_prefix"],
                            train.iloc[fit_idx]["label"])
    oof_p[pred_idx] = enc.predict_proba(train.iloc[pred_idx]["text_prefix"])

train["p_encoder"] = oof_p

# Step 3: stacked LightGBM
feature_cols = structured_cols + ["p_encoder"]
stacked = lgb.LGBMClassifier(n_estimators=1000, learning_rate=0.03)
stacked.fit(train[feature_cols], train["label"],
            eval_set=[(val[feature_cols], val["label"])],
            callbacks=[lgb.early_stopping(50)])

# Step 4: final encoder on all training data (deployed)
final_enc = fine_tune_encoder(train["text_prefix"], train["label"])

# Step 5: calibrate stacked output on held-out data, then evaluate on test
```

For validation and test rows, compute `p_encoder` with the final encoder (`final_enc`), since that's what production will use.

---

## User

How is it different from fine tuned encoder as a feature in classical ML

---

## Claude

They're the same thing. "Stacking" is the name for using one model's prediction as an input feature to another model. Option 4 is exactly "fine-tuned encoder output as a feature in LightGBM."

What can differ is how you do it, and those differences matter.

## 1. How the feature is generated (the most important difference)

| Approach | How `p_encoder` is produced for training rows | Result |
|---|---|---|
| **Naive** | Train the encoder on all training data, then predict on that same data | The feature looks far more accurate than it really is, LightGBM over-trusts it, and performance drops in production |
| **Proper stacking** | Out-of-fold: each row's prediction comes from an encoder that never saw that row | The feature is as reliable in training as it will be in production |

Many people who "use an encoder as a feature" do the naive version without realizing it. The out-of-fold step is what makes it correct stacking.

## 2. What you pass from the encoder

| Option | Feature added to LightGBM | Trade-off |
|---|---|---|
| **Probability** (what I suggested) | 1 column: `p_encoder` | Simple, stable, explainable |
| **Embedding vector** | 16 to 768 columns from the encoder's hidden layer | More information, but overfits more easily, trees handle dense vectors poorly, harder to explain |
| **Multiple heads** | A few probabilities: frustration, bot failure, explicit request, capability gap | More specific signals that match your reason categories, still interpretable |

The multiple-heads version is worth considering for Swiggy: one encoder fine-tuned with several outputs gives LightGBM separate "customer is angry" and "bot misunderstood" signals instead of one combined score.

## 3. Fine-tuned vs. frozen encoder

This is the actual difference between Option 2 and Option 4:

- **Option 2 (frozen):** a pre-trained embedding model used as-is. You compute generic features from it (message similarity, sentiment). No training on your labels, so no leakage risk and no out-of-fold step needed.
- **Option 4 (fine-tuned):** the encoder is trained on your handoff labels, so its output is specific to your task. More powerful, but it needs labels, compute, and the out-of-fold procedure.

## 4. The real alternative: training both together

The approach that's genuinely different from stacking is a **single neural network trained end to end**: the encoder reads the text, the structured features (ETA breach, order value, abuse risk) are fed into the same network, and one loss trains everything together.

| | Stacking (Option 4) | End-to-end neural model |
|---|---|---|
| Training | Two stages: encoder, then tree | One stage, one model |
| Structured features handled by | Trees (strong on tabular data) | Neural network (usually weaker on tabular data) |
| Text and structured features interact | Only through one probability | Throughout the network |
| Data needed | Moderate | More |
| Debugging and explaining | Easier: you can inspect each part | Harder |
| Retraining | Must redo both stages together | Single retrain |

For Swiggy, where much of the signal is in tabular order and customer data, stacking is usually the better choice: trees are hard to beat on tabular features, and the two-stage setup is easier to debug and explain to ops teams. End-to-end makes more sense when text dominates and you have a very large labeled dataset.

## Summary

- Option 4 = fine-tuned encoder output used as a feature in LightGBM. Same idea, two names.
- The detail that matters most is generating that feature **out-of-fold**.
- The design choices are probability vs. embedding vs. multiple heads, and frozen vs. fine-tuned.
- The genuinely different approach is end-to-end joint training, which is less suited to Swiggy's tabular-heavy signals.

---

## User

give more ideas, cite papers wherever necessary

---

## Claude

> **Web search:** learning to defer to an expert consistent estimators Mozannar Sontag

> - [Consistent Estimators for Learning to Defer to an Expert](https://alphaxiv.org/abs/2006.01862)
> - [Consistent Estimators for Learning to Defer to an Expert](https://libmast.utm.my/Record/mit-1721.1%2F151827/Description)
> - [Consistent Estimators for Learning to Defer to an Expert](https://proceedings.mlr.press/v119/mozannar20b.html)
> - [Consistent Estimators for Learning to Defer to an Expert](https://icml.cc/virtual/2020/poster/53615)
> - [arxiv.org](https://arxiv.org/pdf/2006.01862)
> - [icml.cc](https://icml.cc/virtual/2020/poster/6448)
> - [Consistent Estimators for Learning to Defer to an Expert](https://clinicalml.org/publication/mozannar-2020-consistent/)
> - [Consistent Estimators for Learning to Defer to an Expert](https://liner.com/review/consistent-estimators-for-learning-to-defer-to-expert)
> - [Consistent Estimators for Learning to Defer to an Expert](https://mlanthology.org/icml/2020/mozannar2020icml-consistent)
> - [Consistent Estimators for Learning to Defer to an Expert](https://www.wizwand.com/paper/68fa692c1e209131cea2089c)

> **Web search:** conformal risk control Angelopoulos false negative rate guarantee

> - [Conformal Risk Control](https://arxiv.org/pdf/2208.02814)
> - [Conformal Risk Control](https://proceedings.iclr.cc/paper_files/paper/2024/hash/f3549ef9b5ff520a7e41ff3cc306ab2b-Abstract-Conference.html)
> - [arxiv.org](https://arxiv.org/abs/2208.02814)
> - [Conformal Risk Control](https://research.google/pubs/conformal-risk-control/)
> - [arxiv.org](https://arxiv.org/abs/2208.02814v4)
> - [Current browse context:](https://export.arxiv.org/abs/2208.02814)
> - [iclr.cc](https://iclr.cc/virtual/2024/poster/19529)
> - [Conformal Risk Control](https://sotaverified.org/papers/conformal-risk-control)
> - [Conformal Risk Control](https://mlanthology.org/iclr/2024/angelopoulos2024iclr-conformal)
> - [Conformal Risk Control](https://www.wizwand.com/paper/68fa5da41e209131ce9dbd4c)

> **Web search:** user satisfaction estimation task-oriented dialogue turn level Sun 2021 simulating user satisfaction

> - [arxiv.org](https://arxiv.org/abs/2105.03748v1)
> - [Simulating User Satisfaction for the Evaluation of Task-oriented Dialogue Systems](https://api.deepai.org/publication/simulating-user-satisfaction-for-the-evaluation-of-task-oriented-dialogue-systems)
> - [core.ac.uk](https://core.ac.uk/download/519721716.pdf)
> - [www.arxiv.org](https://www.arxiv.org/pdf/2105.03748)
> - [www.emergentmind.com](https://www.emergentmind.com/papers/2105.03748)
> - [Simulating User Satisfaction for the Evaluation of Task-oriented Dialogue Systems](https://www.dare.uva.nl/id/b41a5f11-6137-4ab1-bebd-436be4f301ce?page=2732)
> - [Simulating User Satisfaction for the Evaluation of Task-oriented Dialogue Systems](https://dare.uva.nl/id/b41a5f11-6137-4ab1-bebd-436be4f301ce)
> - [Quick review](https://liner.com/review/simulating-user-satisfaction-for-evaluation-taskoriented-dialogue-systems)
> - [api.emergentmind.com](https://api.emergentmind.com/papers/2105.03748)
> - [Simulating User Satisfaction For The Evaluation Of Task-oriented Dialogue Systems | Awesome LLM Papers](https://awesomepapers.io/large-language-models/publications/sun2021simulating)

These go beyond the stacked LightGBM + encoder setup. They're grouped by what they change: how the problem is framed, the model, the decision rule, or how you learn from deployment.

# A. Reframe the problem

## 1. Learning to defer: escalate where the human adds value

Your current framing asks "will the bot fail?" A better question is "**will a human do meaningfully better than the bot here, given the cost?**" Those aren't the same. Some conversations fail no matter who handles them (a customer furious about a cancelled order the restaurant can't remake), and escalating them just spends agent time.

This is the learning-to-defer setting. Mozannar and Sontag (ICML 2020) learn models that either make the decision themselves or pass it to a downstream expert, training a classifier and a rejector from samples of the expert's decisions, using a reduction to cost-sensitive learning with a consistent surrogate loss that generalizes cross-entropy. A related point from that line of work is that deciding when to defer is harder when the expert has side information the model lacks, which is exactly your case: Swiggy agents can see dashboards and take actions the bot can't.

**For Swiggy:** a human adds a lot for payment reconciliation, account blocks, and compensation above limits, and little for "where is my order" with an accurate ETA. Train with agent outcomes as the expert's performance, so the model learns where agents actually change outcomes.

## 2. Uplift modeling: rank by improvement, not risk

Closely related: estimate, for each conversation,

```
uplift = P(bad outcome | stays with bot) − P(bad outcome | handed to human)
```

and escalate the conversations with the highest uplift, not the highest risk. Standard approaches are meta-learners like the T-learner and X-learner (Künzel et al., PNAS 2019). The CEM paper discussed earlier also takes a causal view of handoff and labor cost.

**Requirement:** you need cases where similar conversations got different treatment, ideally randomized. The 1 to 2% exploration slice from earlier provides this. Without it, uplift estimates are unreliable because handoff decisions so far were made by the turn rule.

## 3. Survival framing: risk per turn, with censoring handled properly

Treat each conversation as "time until failure" and predict the **hazard**: the probability that the conversation fails at this turn, given that it hasn't yet.

Why it fits:
- **Censoring is built in.** Conversations cut off by your turn limit are "censored" (you never saw what would have happened), and survival models handle that correctly instead of mislabeling them.
- **It works with LightGBM.** Discrete-time survival is a per-turn binary classification over turns where the conversation was still "at risk," so your existing per-turn rows already fit.
- **You get useful outputs**, such as "probability of failure within the next 2 turns," which supports the earliest-useful-escalation goal.

# B. Model changes

## 4. A streaming sequence model over turn features

Instead of recomputing everything each turn, run a small GRU or temporal convolution over **per-turn feature vectors** (turn features plus a frozen embedding of each message). It carries state forward, so each new turn costs one small update.

Evidence for hierarchical models on dialogue: on the USS user-satisfaction dataset, a hierarchical GRU model performed best for in-domain satisfaction prediction, while a BERT-based model generalized better across domains. The MHCH handoff model DAMI is also hierarchical. Use the GRU output as another stacked feature into LightGBM, or as an alternative to the fine-tuned encoder.

**For Swiggy:** this captures trajectories, such as sentiment declining over three turns while the ETA keeps slipping, which single-turn features represent only roughly.

## 5. Auxiliary tasks on the encoder

Train the encoder with extra outputs alongside the handoff label:
- **Turn-level satisfaction:** the RSSN paper discussed earlier does this jointly with handoff prediction. The USS dataset includes 6,800 dialogues from several domains, including real e-commerce conversations, with every user utterance and each full dialogue labeled on a 5-point satisfaction scale, which could serve for pre-training or as a schema for your own labels, though it's not Hinglish or food delivery.
- **Reason category:** capability gap, bot failure, preference, risk
- **Dialogue breakdown:** "the bot's last reply didn't make sense here"

Auxiliary tasks give the encoder more training signal from the same data, and each head can be a separate feature for LightGBM.

## 6. Bot uncertainty features

The bot often signals its own trouble before the customer complains:
- **Token log-probabilities** of the bot's replies, if your API exposes them. Low confidence often precedes failure.
- **Policy or retrieval misses:** the bot looked up a policy and found nothing relevant.
- **Repeated or near-identical bot replies** (high similarity between consecutive bot messages means it's looping)
- **Tool-call patterns:** order lookup returned an unexpected status, refund API returned an error.

These are cheap, available in real time, and often predict failure earlier than customer sentiment.

# C. The decision layer

## 7. Conformal risk control for safety categories

For food safety, allergic reactions, and delivery partner misconduct, you want a guarantee, not just a good average. Conformal risk control (Angelopoulos et al., ICLR 2024) extends conformal prediction to control the expected value of any monotone loss, and the authors demonstrate using it to bound the false negative rate.

**In practice:** on a calibration set of safety-related conversations, the procedure picks a threshold such that, for example, no more than 2% of true safety cases are missed, with a statistical guarantee under the usual assumption that future data resembles the calibration data. Combine it with hard rules: rules catch explicit keywords, and conformal thresholds catch subtler cases.

## 8. A three-way decision instead of bot vs. human

Add a middle option: **agent-assist.** The bot drafts the resolution ("refund ₹180 for missing item, offer ₹50 coupon"), and an agent approves or edits it in a few seconds without taking over the chat.

| Decision | When | Agent cost |
|---|---|---|
| Bot handles | Low risk, within bot authority | None |
| **Agent approves bot's action** | Medium risk, or slightly above bot's limit | Seconds |
| Full handoff | Safety, complex disputes, high uplift | Minutes |

Learning to defer extends naturally to multiple "experts" with different costs. For Swiggy, many compensation cases could move from full handoff to approval, which could reduce agent minutes substantially.

# D. Learning from deployment

## 9. Off-policy evaluation before A/B tests

Before testing a new handoff policy live, estimate how it would have performed using logged data, with inverse propensity scoring or doubly robust estimators (Dudík et al., ICML 2011). This requires logging the **probability** with which each decision was made, which the randomized exploration slice provides. It lets you compare many candidate thresholds or models offline and send only the best ones to A/B tests, which matters at Swiggy's scale where a bad live policy affects many customers quickly.

## 10. Continuous label refresh from agent feedback

Add one button to the agent interface: "Was this handoff necessary? Yes / No / Should have come earlier." It costs agents a second per case and gives you a steady stream of high-quality labels on exactly the decisions the model made, including the timing.

# Suggested priority for Swiggy

| Priority | Idea | Why |
|---|---|---|
| 1 | Bot uncertainty features (6) | Cheap, real-time, early signal |
| 2 | Agent feedback button (10) | Best ongoing label source, very low cost |
| 3 | Three-way decision with agent-assist (8) | Likely the biggest direct reduction in agent cost |
| 4 | Conformal thresholds for safety (7) | Guarantees where mistakes are most costly |
| 5 | Survival framing (3) | Handles turn-limit censoring correctly, fits LightGBM |
| 6 | Learning to defer / uplift (1, 2) | Best long-term framing; needs exploration data first |
| 7 | Sequence model, auxiliary tasks (4, 5) | Incremental gains once the basics work |
| 8 | Off-policy evaluation (9) | Once you're iterating on policies frequently |

Ideas 1 and 2 are also good research directions: cost-aware learning to defer, with agents as experts who have side information, studied in a real high-volume support setting, is still underexplored.

---

## User

is there any latest research done on this which might help us get a new way/method of doing this ?

---

## Claude

> **Web search:** LLM customer service agent when to escalate to human 2026 paper

> - [(PDF) Beyond Customer Success Automation: Designing and Evaluating a Human-in-the-Loop AI Agent for Proactive SaaS Retention](https://www.researchgate.net/publication/415549432_Beyond_Customer_Success_Automation_Designing_and_Evaluating_a_Human-in-the-Loop_AI_Agent_for_Proactive_SaaS_Retention)
> - [Recognition Without Mitigation: Ethical Frameworks in Autonomous Offensive-LLM Agent Research](https://arxiv.org/pdf/2506.08693)
> - [Act or Escalate? Evaluating Escalation Behavior in Automation with Language Models](https://arxiv.org/pdf/2604.08588)
> - [AI Customer Care Human Escalation Triggers When to Hand Off - Petronella Cybersecurity News](https://petronellatech.com/blog/ai-customer-care-human-escalation-triggers-when-to-hand-off/)
> - [When Should Service Agents Reconsider? Difficulty-Routed Control in Customer-Service Operations](https://arxiv.org/pdf/2607.01426)
> - [Customer Service AI Agent Statistics 2026: 120+ Data](https://www.digitalapplied.com/blog/customer-service-ai-agent-statistics-2026-data)
> - [5 Best LLMs for Customer Support, Based on Our Own Research - Omnichannel Conversational Platform](https://www.qiscus.com/en/blog/best-llm-for-customer-support/)
> - [AI Agent for Customer Service: 2026 Guide - Allainews](https://allainews.net/ai-agent-for-customer-service/)
> - [Customer Service Escalation Process: AI Handoff Guide](https://www.ever-help.com/blog/customer-service-escalation-process)

> **Web search:** Agentic AI and human-in-the-loop interventions field experimental evidence Alibaba customer service

> - [Agentic AI and Human-in-the-Loop Interventions: Field Experimental Evidence from Alibaba's Customer Service Operations](https://arxiv.org/abs/2605.14830)
> - [Even With Humans in the Loop, Agentic AI Systems Struggle](https://tuck.dartmouth.edu/news/articles/even-with-humans-in-the-loop-agentic-ai-systems-struggle)
> - [calendar.hkust.edu.hk](https://calendar.hkust.edu.hk/node/48224)
> - [www.emergentmind.com](https://www.emergentmind.com/papers/2605.14830)
> - [department industrial engineering decision analytics joint iedaisom seminar gen ai assistant](https://calendar.hkust.edu.hk/zh-hant/events/department-industrial-engineering-decision-analytics-joint-iedaisom-seminar-gen-ai-assistant)
> - [sites.google.com](https://sites.google.com/view/yiweiwang/)
> - [Agentic AI and Human-in-the-Loop Interventions: Field Experimental Evidence from Alibaba's Customer Service Operations](https://feedbagel.com/post/agentic-ai-and-human-in-the-loop-interventions-field-experimental-evidence-from-)
> - [Agentic AI and Human-in-the-Loop Interventions: Field Experimental Evidence from Alibaba's Customer Service Operations](https://arxiv.deeppaper.ai/papers/2605.14830v2)
> - [Agentic AI and Human-in-the-Loop Interventions: Field Experimental Evidence from Alibaba's Customer Service Operations](https://arxiv.deeppaper.ai/papers/2605.14830v1)

> **Web search:** "When Should Service Agents Reconsider" difficulty-routed control customer-service

> - [When Should Service Agents Reconsider? Difficulty-Routed Control in Customer-Service Operations](https://arxiv.org/pdf/2607.01426)
> - [arxiv.org](https://arxiv.org/abs/2607.01426)
> - [論文評述 When Should Service Agents Reconsider? Difficulty-Routed Control in Customer-Service Operations](https://www.themoonlight.io/tw/review/when-should-service-agents-reconsider-difficulty-routed-control-in-customer-service-operations)
> - [Revisión de artículo When Should Service Agents Reconsider? Difficulty-Routed Control in Customer-Service Operations](https://www.themoonlight.io/es/review/when-should-service-agents-reconsider-difficulty-routed-control-in-customer-service-operations)
> - [papers.cool](https://papers.cool/arxiv/2607.01426)
> - [when should service agents reconsider](https://www.catalyzex.com/paper/when-should-service-agents-reconsider)
> - [When Should Service Agents Reconsider? Difficulty-Routed Control in Customer-Service Operations](https://chatpaper.com/pt/chatpaper/paper/306576)
> - [When Should Service Agents Reconsider? Difficulty-Routed Control in Customer-Service Operations](https://chatpaper.com/de/paper/306576)
> - [When Should Service Agents Reconsider? Difficulty-Routed Control in Customer-Service Operations](https://chatpaper.com/es/paper/306576)
> - [cs.CLcs.AI03 Jul 2026](https://chatpaper.com/paper/306576)

> **Fetched:** None

Yes. Several 2026 papers are directly relevant, and together they point toward a different design than "predict handoff yes/no." Here are the most useful ones, followed by what they suggest for Swiggy.

## 1. Alibaba field experiment: the type of failure decides whether handoff helps

This is the closest real-world evidence to your situation. Researchers ran a randomized field experiment on Alibaba's Taobao platform, where treated workers supervised an agentic AI that resolved AI-eligible chats, while control workers handled all chats without AI. The scale is similar to yours: Taobao's service operation includes 38,000 gig workers serving 380 million daily active users, and the study covered 680,676 chats over 17 days.

The key finding: human intervention preserved service quality in technical escalations (issues beyond the AI's capability), but was less effective in emotional escalations, where customers expressed frustration or dissatisfaction. Also, how well intervention worked depended on the type of AI failure, how much effort agents put in after escalation, and when the intervention happened. One summary describes the takeaway as early human intervention improving recovery.

**What this means for you:** "needs a human" is not one category.
- **Technical failures** (refund above limit, payment mismatch, account issue): handoff works, and timing is less critical.
- **Emotional failures** (customer frustrated): by the time frustration is visible, a handoff often comes too late. These need **earlier** action, or a different response than a plain transfer.

So the model should predict *which kind* of failure is developing, not just whether one is.

## 2. Difficulty-routed control: escalate control before acting, not just to humans

A July 2026 paper from Penn State looks at agents that take real actions. It notes that agents now retrieve records, apply policies, and execute backend writes like refunds, cancellations, and order changes, creating a problem of keeping routine service fast while preventing errors where customer instructions, policies, records, and backend writes interact.

Their design: a lightweight router keeps routine sessions on a low-cost path and sends operationally complex sessions to an escalated workflow, which applies extra deliberation and safeguards before consequential backend writes, instead of applying extra control to every session. In tests, this improved reliability on retail requests involving operational conflict, with stronger control going to conflicted requests rather than routine ones. A review summarizes the core idea as routing based on how operationally entangled a request is, rather than how complex its language is.

**What this means for you:** there's a useful tier between "Flash handles it" and "send to a human." When a refund or cancellation is about to be issued and the situation is complicated (order status doesn't match the complaint, multiple items, partial delivery), route that step through a verification pass or a stronger model before the write happens. Many cases that currently need a human because the bot might make a costly mistake could be handled safely this way.

## 3. "Act or Escalate?": LLMs are poor judges of their own escalation

A Harvard and Johns Hopkins paper tested how LLMs decide when to escalate. They found that the implicit thresholds models use to trade off error cost against escalation cost vary widely, aren't predicted by architecture or scale, and models' self-estimates are miscalibrated in model-specific ways. In numbers: across 304 model and condition pairs, 201 (66%) were overconfident.

On fixes: cost framing in the prompt alone had no effect, but combined with extended thinking it helped reasoning models. Fine-tuning on chain-of-thought targets worked best, producing near-optimal escalation decisions that generalized to domains never seen in training. But the fine-tuned model depended on an external accuracy signal: without the signal, accuracy dropped from 100% to about 84%, because the model invented optimistic accuracy estimates.

**What this means for you:**
- Don't trust the bot's own `needs_human` flag at face value. Flash likely has its own unknown escalation tendency. Measure it on your gold set before using it, and keep it as one feature among many.
- The paper's best setup is essentially what we designed: a **calibrated external probability** combined with an explicit cost rule. Keep the decision in code, using LightGBM's calibrated probability, rather than asking the LLM to decide.

## 4. LLM handover detection on real support dialogues

Qiscus published work at ICADEIS 2026 (IEEE) comparing GPT-4.1 and Gemini 2.5 Flash on deciding when a bot should hand a conversation to a human, using a dataset of 100 real customer service dialogues containing 4,265 utterances. The details I could access come from the company's blog rather than the paper itself, but it supports the point that LLM choice measurably affects handover accuracy. That's another reason to test your judges and the bot's flag on your own data.

# A new design these papers suggest

Combining the findings: **a multi-action, failure-type-aware escalation policy.** Instead of a single "hand off?" probability, predict what kind of trouble is developing and choose the cheapest action that fixes it.

**Predictions per turn:**
- P(technical failure): the bot can't do what's needed
- P(emotional failure): frustration is building
- Operational conflict score: the next action (refund, cancellation) involves mismatched records or several items

**Possible actions:**

| Action | Triggered by | Cost |
|---|---|---|
| Continue with Flash | All risks low | Lowest |
| **Reconsider before acting:** verification pass or stronger model before the refund or cancellation write | High operational conflict | Low |
| **Early emotional recovery:** acknowledge directly, offer goodwill within the bot's limits, or bring in a human early | Rising P(emotional) while still moderate | Low to medium |
| **Agent approves bot's proposed action** | Technical issue slightly beyond bot authority | Seconds of agent time |
| Full handoff with summary | High P(technical), safety, or emotional failure past recovery | Highest |

**Decision rule:** choose the action with the lowest expected cost, using calibrated probabilities. That's the cost formula from earlier, extended from two options to five.

**Why this is better than binary handoff:**
- It acts on emotional failures **earlier**, which the Alibaba results suggest is when intervention still works.
- It handles many "risky refund" cases with automated safeguards instead of agents, following the Penn State results.
- It keeps the escalation decision out of the LLM's hands, following the "Act or Escalate?" results.

## Getting there in steps

1. **Add a reason label** (technical vs. emotional) to your data curation. This is a small change, and it lets you check whether the Alibaba finding holds for Swiggy: compare outcomes of past handoffs by type.
2. **Train separate technical and emotional heads** in LightGBM, or one model with two outputs.
3. **Add the "reconsider before write" step** for refunds and cancellations with operational conflict. This is independent of the handoff model and probably the fastest reliability gain.
4. **Measure Flash's escalation tendency** on your gold set before using its `needs_human` flag.
5. **Use the exploration slice** to test early emotional intervention vs. late handoff. This is the experiment that tells you whether timing matters as much for Swiggy as it did for Taobao.

## As a research direction

This also fits well with your research work. Learning to defer has mostly been studied with one model, one expert, and a single defer/act choice. A **multi-action deferral policy** that distinguishes technical from emotional failures, accounts for intervention timing, and is evaluated in a real high-volume support setting combines the Alibaba, Penn State, and HBS findings in a way none of them does alone.

---

## User

what is "flash" you are talking about. Also, tell about how can these ideas be implemented in our case and how can we apply these ideas

---

## Claude

## What "Flash" means

"Flash" was my shorthand for **the LLM your chatbot currently runs on**. In your first message you said the bot uses cheap, small models like Gemini Flash. Google's cheaper, faster Gemini models are called "Flash," so I used that name for "your main bot model." Wherever I wrote "Flash," read it as "your production chatbot LLM," whichever one that is.

# Implementing this for Swiggy

## The target architecture, per customer message

```
customer message
   │
   ▼
[1] Hard rules ──── safety / explicit "agent" request / fraud ──► immediate handoff
   │
   ▼
[2] Feature service: order data + customer data + chat stats (running values)
   │
   ▼
[3] Risk models (LightGBM, calibrated)
       → P(technical failure)
       → P(emotional failure)
       → operational conflict score
   │
   ▼
[4] Decision layer: pick the cheapest action by expected cost
   │
   ├─► Continue with bot
   ├─► Reconsider before refund/cancel write
   ├─► Emotional recovery mode
   ├─► Agent approves bot's proposed action
   └─► Full handoff + summary
```

Only the bot's reply generation uses an LLM on the normal path. Everything else is rules, cached data lookups, and small models on CPU.

## [1] Hard rules

Implement first. No ML is needed, and it immediately makes the system safer.

| Trigger | Detection | Action |
|---|---|---|
| Food safety (foreign object, illness, allergic reaction) | Keyword lists in English, Hindi, Hinglish + an intent label from the bot | Immediate handoff, priority queue |
| Delivery partner misconduct or harassment | Same | Immediate handoff, trust and safety queue |
| Explicit request ("agent se baat karao") | Keyword list + bot intent | Handoff, or offer if low-risk (configurable) |
| Payment deducted, order failed | Payment gateway status from your systems | Handoff to the payments queue |
| Refund API failing repeatedly | Tool-call logs | Handoff |

Keep these rules in config, not code, so ops teams can update keywords without a deploy. Log every rule hit, so you can measure precision later.

## [2] Feature service

A small service that returns a feature vector for (conversation ID, turn number) in a few milliseconds.

**Sources:**
- **Order service:** status, ETA, minutes past ETA, order value, items, business line (Food / Instamart / Dineout), payment method, delivery partner reachability
- **Customer profile:** order frequency, Swiggy One, prior contacts on this order, abuse-risk score from trust and safety
- **Chat state** (computed incrementally each turn): turn count, rephrase count (embedding similarity between consecutive customer messages), bot apology count, refund offered and rejected, tool failures, photo uploaded, sentiment per turn and its trend
- **Bot output fields** (see below)

**Implementation notes:**
- Fetch order and customer data once at conversation start and cache them; refresh order status only if the order is live.
- Compute chat features incrementally: update running counters per turn instead of reprocessing the whole conversation.
- **Use exactly the same feature code in training and production.** If training features are computed differently from production features, the model degrades silently.

**Add structured fields to the bot's output.** This costs no extra LLM call:

```json
{
  "reply": "...",
  "intent": "missing_item",
  "needs_human": false,
  "reason": null,
  "proposed_action": {"type": "refund", "amount": 180, "items": ["Paneer Tikka"]}
}
```

Use `needs_human` as a feature only, after measuring on your gold set how often the bot's flag is right. The "Act or Escalate?" paper found escalation tendencies vary unpredictably across models.

## [3] Risk models

**Labels:** from the data curation plan, with the reason category split:
- **Technical:** capability gap, payment or account issue, compensation beyond the bot's limit, agent performed an action the bot can't do
- **Emotional:** frustration or dissatisfaction is the main issue (rising negativity, "worst service," threats to uninstall), whether or not there's also a technical issue

**Models:** two LightGBM classifiers (or one multi-output setup) on the same features:
- `P_technical` (the bot can't resolve this)
- `P_emotional` (the customer experience is breaking down)

**Operational conflict score:** this can start as rules. It's high when:
- The proposed refund involves items that don't match the order record
- The order status contradicts the complaint (e.g., "not delivered" when status says delivered, with proof)
- Multiple orders or partial refunds are already on record
- The refund amount is near or above the bot's limit
- The customer has a high abuse-risk score

Later, you can train a model for it using cases where agents corrected or reversed bot refunds.

**Calibration:** isotonic or Platt scaling on held-out data, since the decision layer uses these probabilities directly.

**Start simple:** the first version can be the feature-only LightGBM (Option 1 from before). Add the stacked encoder later only if evaluation shows it helps.

## [4] Decision layer

A small function in code, with costs defined in config that ops and finance teams can adjust:

```python
COSTS = {
    "agent_minute": 12,          # ₹ per agent minute (fill in real value)
    "full_handoff_minutes": 6,
    "approval_minutes": 0.5,
    "reconsider_call": 0.3,      # stronger-model call cost in ₹
    "technical_miss": 150,       # expected cost of an unresolved technical issue
    "emotional_miss": 250,       # churn risk, repeat contact, bad rating
}

def choose_action(p_tech, p_emo, conflict, has_pending_write, queue_load):
    agent_cost = COSTS["agent_minute"] * queue_multiplier(queue_load)
    options = {
        "continue":  p_tech * COSTS["technical_miss"] + p_emo * COSTS["emotional_miss"],
        "emotional_recovery": p_tech * COSTS["technical_miss"]
                              + p_emo * RECOVERY_RESIDUAL * COSTS["emotional_miss"],
        "approval":  COSTS["approval_minutes"] * agent_cost
                     + p_emo * COSTS["emotional_miss"] * APPROVAL_RESIDUAL,
        "handoff":   COSTS["full_handoff_minutes"] * agent_cost
                     + p_emo * COSTS["emotional_miss"] * HANDOFF_RESIDUAL_EMO,
    }
    if has_pending_write and conflict > CONFLICT_THRESHOLD:
        return "reconsider"      # runs before any action is executed
    return min(options, key=options.get)
```

The `RESIDUAL` values capture how much each action actually reduces each risk. Start with estimates from ops experience, then learn them from data. In particular, the Alibaba study suggests handoff reduces emotional risk less than technical risk, so `HANDOFF_RESIDUAL_EMO` should not be near zero. The timing experiment below measures this for Swiggy.

`queue_multiplier` makes agent time effectively more expensive when agents are overloaded, so the system automatically escalates less during the dinner peak and more when queues are short.

## [5] The actions

### Reconsider before write

A guard step that runs **before** any refund, cancellation, or order change is executed:

1. **Deterministic checks (always, almost free):** amount ≤ order value; items exist in the order; no duplicate refund; policy limits respected
2. **If the conflict score is high:** send the conversation, order record, and proposed action to a stronger model with one question: "Is this action correct and consistent with the records and policy? If not, what's wrong?"
3. **Outcomes:** approve → execute; correct → bot revises; uncertain → route to agent approval

Since this only runs on high-conflict writes, the stronger model is called on a small share of conversations. This is the Penn State paper's main idea applied to Swiggy refunds.

### Emotional recovery mode

When `P_emotional` is rising but still moderate, before the customer is furious:
- **Switch to an empathetic persona.** If one of your E, M, R personas is the empathetic one, the persona router from earlier can be driven by this signal.
- **Inject a specific instruction module:** acknowledge the problem directly, give one concrete next step, avoid repeating earlier messages, don't apologize generically again.
- **Offer goodwill within the bot's authority**, such as a coupon, when policy allows and abuse risk is low.
- **Check after one turn:** if `P_emotional` doesn't drop, escalate to a human then. Don't keep the customer in recovery mode for several turns, since the Alibaba results suggest late intervention works poorly.

### Agent approval

For technical cases slightly beyond the bot's authority:
- The bot tells the customer "Let me get this confirmed, one moment."
- The agent sees a compact card: issue summary, proposed action, order record, and **Approve / Edit / Take over** buttons.
- The agent spends seconds instead of minutes. If no agent responds within the SLA (e.g., 60 seconds), fall back to full handoff.

This needs a change in the agent tool, so involve the agent tooling team early.

### Full handoff with summary

One LLM call generates a structured summary for the agent:

```
Issue: Missing item (Paneer Tikka, ₹180), order #123, delivered 35 min late
Tried: Bot offered ₹50 coupon, customer rejected
Customer state: Frustrated, 2nd contact on this order
Suggested next step: Refund item + goodwill per SOP
```

Agents start working immediately instead of reading the whole conversation.

# Rollout plan

**Phase 1: Foundations (weeks 1 to 4)**
- Hard rules live in production
- Feature service built; features logged for every turn
- Bot outputs structured fields (`intent`, `needs_human`, `proposed_action`)
- Deterministic pre-write checks live
- Data curation started: outcome labels, reason categories, gold set with agents

**Phase 2: Models in shadow mode (weeks 5 to 8)**
- Train `P_technical` and `P_emotional`, calibrate
- Run the decision layer in **shadow mode**: it computes decisions but doesn't act, while the turn rule stays in control
- Compare: which conversations would the new system have escalated, and when? How did those conversations actually end?

**Phase 3: Limited live test (weeks 9 to 12)**
- A/B test on a small share of traffic (e.g., 5%), starting with one city or business line
- Arm A: current turn rule. Arm B: new decision layer with continue / reconsider / handoff
- Add emotional recovery and agent approval once the basic version is stable

**Phase 4: Expand and learn (ongoing)**
- Roll out gradually while metrics hold
- Agent feedback button ("Was this handoff necessary? Earlier?")
- Exploration slice for unbiased data
- Retrain monthly, and whenever the bot changes significantly

# Metrics

| Metric | What it tells you |
|---|---|
| Containment rate | Share of conversations resolved without an agent |
| Agent minutes per 1,000 conversations | Direct cost |
| Repeat contact within 48h on the same order | Whether issues were really resolved |
| CSAT, split by technical vs. emotional cases | Whether recovery mode helps |
| Refund reversal or error rate | Whether reconsider-before-write works |
| Time from first frustration signal to intervention | Whether you act earlier |
| Escalation rate by abuse-risk segment | Whether the system is being gamed |

# One experiment to run early

**The timing test.** Within the exploration slice, for conversations where `P_emotional` crosses a moderate level, randomly assign one of:
- (a) Immediate human handoff
- (b) Emotional recovery mode, then human only if it doesn't help
- (c) Current behavior (turn rule)

Compare CSAT, repeat contact, and agent minutes. This tells you whether the Alibaba finding (emotional cases need early intervention, and handoff alone helps less) holds for Swiggy, and it gives you real values for the `RESIDUAL` parameters in the decision layer instead of estimates.

---

## User

removing the hard rules, if the current pipeline is fine tuned encoder+ ml model, how can we improve the current

---

## Claude

Here's how to improve a pipeline that's already a fine-tuned encoder stacked into a tree model. The order matters: **diagnose first**, because the best improvement depends on where the current model actually fails.

## Step 0: Diagnose before changing anything

**1. Ablation: where does the signal come from?**
Evaluate three versions on the same recent test set:
- Tree model without the encoder feature
- Encoder alone
- The current stacked pipeline

| Result | Meaning | Focus on |
|---|---|---|
| Stacked ≈ tree alone | Encoder adds little | Improving the encoder (or dropping it to save cost) |
| Stacked ≈ encoder alone | Structured features add little | Feature engineering, order context |
| Stacked clearly better than both | Both contribute | Labels, timing, decision layer |

**2. Slice the errors.** Break down false negatives (missed failures) and false positives (unnecessary handoffs) by:
- Intent (missing item, delay, refund, payment, quality)
- Business line (Food / Instamart / Dineout)
- Language (English / Hindi / Hinglish / regional)
- Turn number (failing early in conversations vs. late)
- Live vs. delivered order

Usually a few slices account for most errors. Those slices tell you what to fix.

**3. Check timing, not just correctness.** For conversations that truly needed a human, how many turns after the right moment did the model flag them? A model can have good AUC and still flag failures two turns too late.

**4. Check the setup for silent problems:**
- Are the encoder's training-set predictions generated out-of-fold, grouped by conversation (and ideally by customer)?
- Is the final output calibrated? Plot the reliability diagram on recent data.
- Do any top features leak future information (handoff phrases, exact turn limit)?

## A. Improving the encoder

**1. Continue pre-training on Swiggy chats.** Before fine-tuning, continue the encoder's masked-language-model pre-training on a large set of unlabeled Swiggy conversations. Gururangan et al. ("Don't Stop Pretraining," ACL 2020) showed that this domain-adaptive pre-training consistently improves downstream classification. It's especially helpful for Hinglish, Swiggy-specific vocabulary ("Instamart," "Swiggy One," "DE," restaurant names), and code-mixed text that general models handle poorly. You have millions of unlabeled conversations, so this mostly costs compute.

**2. Try a stronger base model.** If you're on a generic English model, compare multilingual or Indic models (MuRIL, IndicBERT, multilingual MiniLM or XLM-R variants) on your gold set, with special attention to the Hinglish slice.

**3. Improve the input format.**
- Include both customer and bot turns with speaker tags.
- **Truncate from the start**, not the end, so the most recent turns are always kept.
- Add a short structured header, so the encoder can read order context in the same text:
  ```
  [LIVE] [ETA_BREACH=35] [REFUND_OFFERED] [2ND_CONTACT]
  [USER] order kahan hai ...
  [BOT] ...
  ```
  This lets the encoder learn interactions between text and context ("angry tone + 35 minutes late" vs. "angry tone + on time").

**4. Multi-task heads.** Fine-tune with several outputs instead of one:
- Technical failure
- Emotional failure
- Turn-level satisfaction (RSSN, discussed earlier, trains satisfaction jointly with handoff)
- Intent

Pass all of these to the tree model as separate features. The tree can then weigh "customer is angry" differently from "bot can't do this," which also prepares you for the multi-action decision layer.

**5. Use soft labels.** If labels come from a label model or several judges, train on their probabilities (e.g., 0.7) rather than forced 0/1 labels. Uncertain examples then contribute less, which reduces the effect of label noise.

**6. Hard example mining.** Retrain with extra weight on cases the current model gets wrong, especially long delayed-order conversations the bot resolved (these teach "long ≠ failing") and polite-but-furious messages.

## B. Improving the tree model

**1. Use the encoder's history, not just its current value.** This is probably the single biggest quick win. If the tree currently sees only `p_encoder` for this turn, add:
- `p_encoder` at turns t-1 and t-2
- The maximum so far in this conversation
- The change since the previous turn (slope)

Trajectory matters more than level: a customer going from 0.2 → 0.5 → 0.7 is very different from one sitting steady at 0.5.

**2. Trajectory features for everything else.** The same idea for sentiment, rephrase count, and ETA breach: values at previous turns, deltas, and maximums so far.

**3. Entity-level prior rates.** Features describing the restaurant, delivery partner, and area, computed from historical data (using only data from before the conversation):
- The restaurant's recent missing-item or quality-complaint rate
- The delivery area's recent delay rate
- The customer's past rate of conversations needing a human

If a restaurant has a high missing-item rate, a missing-item complaint from it is more likely genuine and more likely to need resolution.

**4. Monotonic constraints.** LightGBM supports forcing a feature's effect to only increase (or decrease) risk. Set constraints where the direction is clear: more minutes past ETA, more rephrases, more tool failures should never *lower* risk. This prevents odd learned patterns, makes the model more robust when data shifts (e.g., festivals, rain), and makes it easier to explain to ops.

**5. Weight samples by label confidence.** Use the label model's confidence as sample weight, so uncertain labels have less influence.

**6. Consider separate models per business line.** Instamart and Dineout issues differ from food delivery. Either train separate models or verify through slice metrics that one model serves all three well.

## C. Improving the stacking setup

**1. Pass more than one encoder number.** Along with the probability(s), include an uncertainty measure, such as prediction entropy or variance across several dropout passes. The tree can learn "when the encoder is unsure, rely on order context."

**2. Calibrate the encoder before stacking.** Apply temperature scaling to the encoder's outputs first. A more stable input makes it easier for the tree to use.

**3. Time-aware folds.** For the out-of-fold step, group by conversation and customer, and if possible keep folds roughly separated in time. Otherwise the encoder features can look more reliable in training than they will be on future traffic.

## D. Making the encoder cheaper and more temporal

**Encode each turn once and cache it.** Currently, each new turn likely re-encodes the last k turns. Instead:
1. Encode each message once when it arrives, and store its embedding.
2. Run a small GRU over the stored turn embeddings to produce the conversation-level output.

The USS benchmark found a hierarchical GRU model performed best for in-domain satisfaction prediction, while a BERT-based model generalized better across domains, so this is a reasonable option to test against your current encoder. Each new turn costs one short encoding plus a tiny GRU step, which is much cheaper at Swiggy's volume.

**Other speed improvements:**
- Export the encoder to ONNX and quantize to int8. This typically speeds up CPU inference several times with little accuracy loss.
- Cascade: run the tree on cheap features first, and call the encoder only for uncertain cases.

## E. Improving the target and decision

**1. Split into technical vs. emotional outputs.** Based on the Alibaba field experiment, where human intervention preserved quality for technical escalations but helped less for emotional ones, separate outputs let you act differently on each: early recovery for emotional, handoff or approval for technical.

**2. Predict "failure within the next 1 to 2 turns."** A short-horizon target (survival-style) pushes the model to flag problems earlier instead of confirming them once they're obvious.

**3. Segment thresholds and queue-aware costs.** Use different thresholds for live vs. delivered orders, and adjust by agent queue load. These are config changes in the decision layer, not model changes.

## F. Keeping it improving

- **Use disagreement for active learning.** Conversations where the encoder and the tree-without-encoder strongly disagree are the most informative ones to send for human labeling.
- **Agent feedback button** ("Was this handoff necessary? Should it have come earlier?"), which gives you labels on exactly the model's decisions, including timing.
- **Drift monitoring:** track the distribution of `p_encoder` and the final probability weekly, and the calibration curve monthly. Festivals, monsoon, and product launches shift behavior.
- **Retrain both stages together** whenever the bot's prompt or model changes significantly, since bot replies are encoder inputs.

## Suggested priority

| Priority | Change | Effort | Expected impact |
|---|---|---|---|
| 1 | Diagnosis: ablation, error slices, timing, leakage and calibration check | Low | Tells you where to focus |
| 2 | Encoder history features in the tree (lags, max, slope) | Low | Often large |
| 3 | Structured header in encoder input + recent-turn truncation | Low | Medium |
| 4 | Domain-adaptive pre-training on Swiggy chats | Medium | Large, especially for Hinglish |
| 5 | Multi-task encoder (technical / emotional / satisfaction) | Medium | Medium to large, enables better decisions |
| 6 | Entity prior rates + monotonic constraints | Low to medium | Medium, better robustness |
| 7 | Short-horizon target for earlier detection | Medium | Better timing |
| 8 | Turn-level caching + GRU, ONNX int8 | Medium | Large cost savings |
| 9 | Active learning + agent feedback loop | Medium | Steady gains over time |

Start with 1 and 2. If the diagnosis shows the encoder adds little, prioritize 3 to 5. If it shows the encoder dominates and structured features add little, prioritize 6 and the order-context features.

---

## User

I was thinking of what other strategies might be possible for this. Other techniques we can nuse, cite latest paers and articles if needed

---

## Claude

> **Web search:** forecasting user dissatisfaction before it happens conversational agents LLM 2025 2026 paper

> - [Interpretable User Satisfaction Estimation for Conversational Systems with Large Language Models](https://www.researchgate.net/publication/384214975_Interpretable_User_Satisfaction_Estimation_for_Conversational_Systems_with_Large_Language_Models)
> - [User Frustration Detection in Task-Oriented Dialog Systems](https://aclanthology.org/2025.coling-industry.23.pdf)
> - [DCEA: A dynamic cognition-emotion aggregation model for interpretable satisfaction prediction with AI conversational services - ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0306457326003407)
> - [Can LLMs Be Efficient Predictors of Conversational ...](https://aclanthology.org/2025.findings-emnlp.816.pdf)
> - [Expectation Alignment of Language Models for Real-World User Expectations](https://arxiv.org/pdf/2607.20485)
> - [Feedback by Design: Understanding and Overcoming User Feedback Barriers in Conversational Agents](https://arxiv.org/pdf/2602.01405)
> - [Using LLMs to Investigate Correlations of Conversational Follow-up Queries with User Satisfaction](https://arxiv.org/pdf/2407.13166)
> - [Clarify User Expertise: Towards Proactive Conversational Agents Tailoring Responses to User Proficiency](https://arxiv.org/pdf/2608.22266)
> - [Evaluating User Experience in Conversational Recommender Systems: A Systematic Review Across Classical and LLM-Powered Approaches](https://arxiv.org/pdf/2508.02096)
> - [PrefIx: Understand and Adapt to User Preference in Human-Agent Interaction](https://arxiv.org/pdf/2602.06714)

> **Web search:** LLM user simulator customer service agent evaluation realistic simulated users 2026

> - [Literature Review Mind the Sim2Real Gap in User Simulation for Agentic Tasks](https://www.themoonlight.io/review/mind-the-sim2real-gap-in-user-simulation-for-agentic-tasks)
> - [2026.acl long.2192](https://aclanthology.org/2026.acl-long.2192.pdf)
> - [License: CC BY 4.0](https://arxiv.org/html/2603.11245v1)
> - [Michał K. Szczerbak](https://aclanthology.org/people/michal-k-szczerbak/)
> - [Ewa Komkowska](https://aclanthology.org/people/ewa-komkowska/unverified/)
> - [arxiv.org](https://arxiv.org/pdf/2606.11079)
> - [Lukasz Krajewski](https://aclanthology.org/people/lukasz-krajewski/unverified/)
> - [← Back to Paper List](https://papers.lunadong.com/paper/9258)
> - [www.arxiv.org](https://www.arxiv.org/pdf/2601.17087)
> - [arxiv.org](https://arxiv.org/pdf/2601.17087v2.pdf)

> **Web search:** offline reinforcement learning from logged customer service conversations escalation policy

> - [End-to-End Offline Goal-Oriented Dialog Policy Learning via Policy Gradient](https://arxiv.org/pdf/1712.02838)
> - [Offline Reinforcement Learning: Tutorial, Review, and Perspectives on Open Problems](https://arxiv.org/pdf/2005.01643)
> - [ojs.aaai.org](https://ojs.aaai.org/index.php/AIES/article/download/36657/38795/40732)
> - [End-to-End Offline Goal-Oriented Dialog Policy Learning via Policy Gradient](https://astro.paperswithcode.com/paper/end-to-end-offline-goal-oriented-dialog)
> - [arxiv.org](https://arxiv.org/pdf/1702.03334.pdf)
> - [arXiv is now an independent nonprofit! Learn more](https://arxiv.org/html/1702.03334)
> - [Scalable and Safe Remediation of Defective Actions](https://ar5iv.labs.arxiv.org/html/2305.10528)
> - [← all papers · overview](https://awesomepapers.io/ai-agents/papers/1712.02838)
> - [end to end offline goal oriented dialog](https://sotaverified.org/papers/end-to-end-offline-goal-oriented-dialog)

Here are strategies that go beyond everything discussed so far. Some come from recent papers; others are Swiggy-specific ideas that follow from the same principles.

# 1. Forecast failure instead of detecting it

Most handoff models, including yours, detect failure once signs are visible. A different framing is **forecasting**: predicting that a conversation is about to go wrong before the customer shows frustration.

This has been studied as conversational derailment forecasting. An EMNLP 2025 Findings paper notes that recent work has shifted from detecting problems after the fact to predicting them before they occur, enabling earlier intervention, but that forecasting is hard because problems emerge in context-dependent ways and alerts must be timely. It tested prompted LLMs on this task, asking whether they can predict derailment as early as existing models, and how they compare on performance and cost.

**For Swiggy:** change the target from "needs a human now" to "will need a human within the next 2 turns," and evaluate on how many turns of warning the model gives. This works especially well for emotional failures, where the Alibaba study found late intervention helps little. Early signals often come from the order side (the ETA updates keep slipping, the delivery partner is unreachable) before the customer gets angry.

# 2. Model cognition and emotion as separate pathways

A 2026 paper in Information Processing & Management proposes DCEA, which builds a dynamic picture of user experience from both cognitive and emotional dimensions during interactions with AI, motivated by the observation that existing satisfaction estimation methods mostly rely on a single dimension of user experience, which limits prediction quality. It also adds an auxiliary task predicting the reasons for dissatisfaction, improving both interpretability and robustness.

**For Swiggy:** this supports the technical vs. emotional split from independent evidence. Concretely, track two running states per conversation:
- **Cognitive:** is the issue getting closer to resolution? (correct order identified, cause understood, a valid action available)
- **Emotional:** is the customer's mood improving or worsening?

A conversation where the issue is nearly resolved but the customer is angry needs a different response than one where the customer is calm but the bot is going in circles.

# 3. Treat handoff as a sequential decision (offline RL)

Your current model answers "how likely is failure now?" But the real decision is **"is it better to act now or wait one more turn?"** A conversation at 60% risk that usually recovers by itself should be handled differently from one at 60% that only gets worse.

That's a reinforcement learning problem: at each turn, choose an action (continue, recovery mode, agent approval, handoff), and receive a reward at the end (resolution, CSAT, repeat contact, minus agent cost). The standard reference, Levine et al.'s offline RL tutorial, notes that offline RL lets you combine optimal decision making with large datasets of logged conversations, and that it has been applied to datasets of logged agent-customer transcripts.

**For Swiggy:**
- **State:** your existing per-turn features
- **Actions:** the action options from the multi-action design
- **Reward:** resolution outcome minus agent cost
- **Method:** start with fitted Q-iteration using LightGBM as the value function. It's much simpler than deep RL and works on tabular features.

**Main risk:** offline RL is unreliable for actions that rarely appear in your logs. A paper on legal conversational agents notes that offline training suffers from distribution shift between the learned policy and the behavior policy in the data. Your logs mostly show "continue until the turn limit, then hand off," so the model will have little information about other actions until the exploration slice collects some. Treat this as a medium-term project.

# 4. Simulate customers to test policies, carefully

LLM-simulated customers could let you test "what if the bot had continued?" without risking real customers, which addresses the selection bias from your turn limit.

**But recent work urges caution.** A 2026 study replaced simulated users with 451 real human participants across 165 tasks on τ-bench (a customer service benchmark), and compared them with 31 LLM simulators. It found that LLM simulators are excessively cooperative, stylistically uniform, and lack realistic frustration or ambiguity, creating an "easy mode" that inflates agent success rates above the human baseline: up to 77.8% success compared with 63.6% for humans. A separate ACL 2026 paper reached a similar conclusion, titled "Lost in Simulation: LLM-Simulated Users are Unreliable Proxies for Human Users in Agentic Evaluations."

**For Swiggy:** simulators are especially bad at exactly what you care about, which is frustration. So:
- Don't use simulated conversations as labels or as a measure of real success rates.
- **Do** use them for stress testing: build customer personas from real Swiggy logs (impatient live-order customer, repeat refund requester, confused first-time user, Hinglish speaker) and check that your handoff policy behaves sensibly across them.
- Validate the simulator by comparing simulated conversations with real ones for the same scenario before trusting any results.

# 5. Distill an LLM teacher into your encoder

You can get LLM-level understanding at encoder-level cost:

1. Run a strong LLM judge (ideally with a forecasting prompt) over **millions of unlabeled Swiggy conversations** using the batch API.
2. Use its probabilities as soft labels to train your encoder.
3. Fine-tune further on your gold set and outcome labels.

The encoder learns patterns from far more examples than you could ever label by hand. An industry paper on frustration detection at COLING 2025 found that LLM-based in-context learning outperformed sentiment and rule-based methods for detecting user frustration, but also observed poor LLM performance in short conversations. So check the teacher's accuracy on short chats specifically, and weight its labels lower there.

# 6. Incident-aware escalation

This is a Swiggy-specific strategy. Individual conversations aren't independent: when a restaurant's kitchen is overwhelmed, a delivery area floods, or a payment gateway goes down, dozens of customers contact support about the same root cause within minutes.

**Implementation:**
- Track complaint rates in real time per restaurant, delivery zone, and payment method, using sliding windows (e.g., last 15 minutes).
- When a spike is detected, mark it as an **active incident**.
- Feed incident status into the handoff model as a feature.

**What changes during an incident:**
- The bot can give an honest explanation ("There's heavy rain in your area and many orders are delayed") instead of generic apologies, which reduces frustration.
- Compensation can follow an incident policy instead of case-by-case agent decisions.
- Agents aren't flooded with identical cases. One incident decision applies to many conversations.

# 7. Act before the customer contacts support

The cheapest handoff is the conversation that never happens. Train a model on order data to predict which **live orders** will generate a support contact (ETA slipping repeatedly, partner stalled, restaurant delayed in preparing). For high-risk orders, send a proactive update or apply compensation automatically before the customer opens chat.

This uses the same feature service and order data you already built for the handoff model. It reduces inbound volume, and customers who receive a proactive update arrive (if they do contact support) less frustrated.

# 8. Route to the right agent, not just to an agent

Handoff quality also depends on **who** receives the conversation. Use the predicted reason (payment, food safety, refund dispute, delivery partner issue) and language to route to the right agent skill group: payments specialists, trust and safety, a Hindi or regional-language agent. A well-matched agent resolves faster, which reduces the agent cost in your decision formula and improves outcomes for the cases you do escalate.

# 9. Per-customer escalation preferences

Customers differ. Some always want a human; others prefer to self-serve and get annoyed by being transferred. From each customer's history (past contacts, whether they asked for an agent, CSAT after bot vs. human resolution), compute a "prefers human" score and use it as a feature. A customer who always asks for an agent at turn 1 shouldn't be kept in the bot for four turns first.

# Summary and priority

| Strategy | Effort | Impact | When |
|---|---|---|---|
| 7. Proactive outreach before contact | Medium | High (reduces volume) | Soon: reuses order features |
| 6. Incident-aware escalation | Low to medium | High during peaks and rain | Soon |
| 1. Forecasting target (next 1 to 2 turns) | Low | Earlier intervention | Soon: label change only |
| 2. Cognitive + emotional states | Medium | Better action choice | With the multi-action design |
| 8. Skill-based agent routing | Low to medium | Faster resolution after handoff | Soon |
| 9. Per-customer preference feature | Low | Fewer annoyed customers | Soon |
| 5. LLM teacher distillation | Medium | Better encoder, same inference cost | Next quarter |
| 4. Simulation for stress testing | Medium | Safer policy changes | Before major rollouts |
| 3. Offline RL policy | High | Optimal timing | After exploration data exists |

Strategies 6 and 7 work at the system level rather than inside the handoff model, and for Swiggy they may reduce agent load more than any model improvement. Strategy 3 is the most ambitious, and the most interesting as research, but it depends on exploration data you don't have yet.

