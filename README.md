# Idea to Solution: Agent Skill for Product Discovery

**Idea to Solution is a portable Agent Skill that applies Product Manager thinking to software idea validation, JTBD analysis, product teardown, solution brainstorming, and GitHub open-source discovery.**

[Chinese (Simplified)](README.zh-CN.md)

It turns a rough software idea into a clearer product direction and reuse plan. The skill applies a **Product Manager’s perspective** to early product thinking: understand the job behind an idea, learn from products that already serve similar needs, decide whether the idea deserves further exploration, and find software that can be reused before implementation.

It is designed for personal software projects. It does not assume a SaaS business, a large market, or a need to build every feature from scratch.

## What it helps you do

- **Frame the user problem.** Clarify who has the problem, when it occurs, what outcome they want, what they do today, and what would count as a useful first result.
- **Break down an idea like a PM.** Separate user needs and outcomes from proposed features. Mark facts, assumptions, and open questions so an early feature list does not become the product definition.
- **Learn from good products.** Examine comparable products through their users’ jobs, time to first value, core usage or completion loop, concrete experience choices, evidence of success, weaknesses, and conditions that may not transfer.
- **Judge whether to explore further.** Return a reasoned view: worth exploring, worth pursuing with a narrower angle, insufficient evidence, or not worth pursuing in its current form. This is a decision about the next exploration step, not a promise of success.
- **Explore distinct solution routes.** Consider an existing product, a lightweight combination, a platform-native feature, or a small custom workflow. Map capabilities to outcomes without assuming one repository per feature.
- **Find reusable GitHub projects.** Search complete products and multi-capability solutions first, then investigate components for meaningful gaps. Compare candidates against the actual job and constraints, verify claims with current sources, and explain what remains to integrate, validate, or build.

## A typical flow

```text
Rough idea
    ↓
User job, context, constraints, and assumptions
    ↓
Relevant product examples and transferable principles
    ↓
Explore / narrow / gather evidence / stop
    ↓
Distinct solution routes and capability coverage
    ↓
Verified GitHub candidates, gaps, and next validation
```

The workflow adapts to the request. It can stop after an idea assessment, analyze an existing product on its own, clarify a JTBD, or start directly from a concrete GitHub search request. When an idea has a clear, promising software direction, it continues into solution exploration and repository research in the same run unless asked to stop earlier.

## What is included

- [`skills/idea-to-solution/SKILL.md`](skills/idea-to-solution/SKILL.md) — the skill entry point and workflow.
- [`skills/idea-to-solution/references/`](skills/idea-to-solution/references/) — focused guides for JTBD, product principles, search, candidate evaluation, and solution synthesis.
- [`skills/idea-to-solution/assets/`](skills/idea-to-solution/assets/) — optional research report and coding handoff templates.

## How search results are presented

The skill organizes findings around **solution routes and user outcomes**, not a forced list of one repository for each feature. A single project may cover several capabilities; several projects may need integration; an official API or simpler workflow may be a better fit than another repository.

For each relevant candidate, the analysis explains what it does, why it fits, what evidence supports the fit, what it does not cover, and what adopting it would still require. It ranks alternatives against hard constraints and evidence before popularity. If no credible candidate is found, it says so and reports the search boundary instead of inventing a recommendation.

When the current environment provides authorized, read-only access to the user’s GitHub Stars, those projects can be checked first. Otherwise, or when they do not cover the job, the search expands to public sources. The skill reports access limits and does not claim exhaustive coverage.

## Structured deliverable

A full idea-to-solution report can include:

1. **Idea and JTBD** — the target user, context, desired progress, constraints, and assumptions.
2. **Product evidence** — comparable products, relevant mechanisms, evidence quality, and what cannot be copied directly.
3. **Assessment** — a clear judgment, confidence, and the facts that could change it.
4. **Solution routes** — meaningfully different ways to deliver the outcome and their trade-offs.
5. **Reuse map** — complete products, multi-capability projects, components, and platform features mapped to outcomes.
6. **Gaps and next step** — what remains unknown, what may need integration or development, and the smallest useful validation.

The report is presented in the conversation by default. Markdown research reports and coding handoffs are created only when requested.

## Install for an Agent

This repository follows the [open Agent Skills format](https://agentskills.io/home). The [`skills` CLI](https://www.skills.sh/docs/cli) can install it for compatible agents and place the complete skill folder, including its references and templates:

```bash
npx skills add JarvixGaby/idea-to-solution-skill --skill idea-to-solution
```

This repository contains one skill. To install it for all supported agents detected by the CLI, use:

```bash
npx skills add JarvixGaby/idea-to-solution-skill --all
```

You can also manually copy `skills/idea-to-solution/` into a skill directory supported by your agent. Directory conventions and support vary by agent; check that agent's documentation.

After installation, ask your agent with a rough idea or a focused request, for example:

> I am considering a lightweight tool for a community sports club to coordinate practice schedules. Is this worth exploring, what product patterns should I learn from, and what could I reuse?

> Analyze why Obsidian works well for personal knowledge management. Focus on the user job, first value, core workflow, and design choices I could apply to a small personal tool.

> Find GitHub libraries that add keyboard shortcuts to a React application. Compare the best fits and show evidence for the key constraints.

## Boundaries

- The skill supports **research and product discovery**. It does not install, clone, run, or modify candidate projects.
- Its conclusions depend on the search and reading tools available in the current agent environment. If live search is unavailable, it marks current repository status as unknown.
- Repository descriptions and documentation are evidence to assess, not proof that the software runs or meets every requirement.
- It is a personal workflow aid, not a substitute for user research or a guarantee that an idea will succeed.

## Frequently asked questions

### What is Idea to Solution?

It is an Agent Skill for product discovery: it breaks down a software idea from the user’s job to possible solution routes, then checks which parts can be reused from existing GitHub projects.

### Which agents can use it?

It follows the open Agent Skills format and can be installed in compatible agents. Available tools, search access, and support for skill resources vary by agent.

### Does it build the product?

No. It produces research, comparisons, and optional coding handoff notes. Implementation happens in a separate, explicitly requested development step.

### Is it just a GitHub repository search tool?

No. It first clarifies the desired user outcome and compares whole products, multi-capability projects, platform features, and simpler workflows. It searches for components when a meaningful gap remains.

### Does it require GitHub authentication?

Public repository research can proceed without access to personal Stars. If authorized read-only Stars access is available, the skill can check those projects first and expand to public search when needed.
