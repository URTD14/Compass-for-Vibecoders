# Feature Ideation Workflow

## What this is
Generate, evaluate, and rank feature ideas for a given problem or goal. Run this *before* writing a PRD — when you know the problem but not the best solution. Great PMs never anchor on the first idea.

## Input
The problem to solve, the goal to achieve, or the metric to move. If unclear, ask: "What problem are you trying to solve, or what metric are you trying to move?"

## Read project context first (required)
Before generating any ideas:
1. Read `README.md` (first 50 lines) — understand the product, the user, and what already exists
2. Read `docs/roadmap.md` if it exists — understand what's already planned so you don't suggest it
3. Read any recent `docs/prd-*.md` — understand what's already been specced

Use this context to make every idea specific to this product and this user. Never generate ideas that contradict existing plans or have already been built.

## Process
1. Reframe the input as a "How might we..." statement specific to this product
2. Generate 5–7 genuinely distinct feature ideas grounded in what you know about the product
3. For each: one-line description, effort (S/M/L/XL), impact (H/M/L), and the key assumption it relies on
4. Flag the riskiest assumption for each idea
5. Recommend top 1–2 to develop into PRDs, with clear rationale tied to the product's actual goals

## Output

Save to `docs/ideation-[problem-kebab-case].md`:

---
# Feature Ideation: [Problem / Goal]
**Date:** [today's date]
**How might we...** [reframe the input as an HMW statement]
**Context:** [1–2 sentences on what's driving this — metric, user complaint, competitive pressure]

## Ideas

### Idea 1: [Name]
**What it is:** [One sentence — concrete, not vague]
**Effort:** S / M / L / XL
**Impact:** H / M / L
**Key assumption:** [The one thing that must be true for this to work]
**Riskiest part:** [What could make this fail or underdeliver]

### Idea 2: [Name]
[same format]

### Idea 3: [Name]
[same format]

### Idea 4: [Name]
[same format]

### Idea 5: [Name]
[same format]

[Add up to 2 more if genuinely distinct ideas exist]

## Evaluation

| Idea | Effort | Impact | Assumption risk | Rank |
|---|---|---|---|---|
| [Idea 1] | S/M/L/XL | H/M/L | H/M/L | [1–7] |
| [Idea 2] | | | | |
| [continue] | | | | |

## Recommendation

**Build next:** [Idea name] — [2–3 sentences on why. Connect to the metric/goal, explain why the effort/impact ratio beats alternatives, and what makes the assumption believable.]

**Runner-up:** [Idea name] — [1–2 sentences. Why it's second, and under what conditions it becomes first.]

**Don't build yet:** [1–2 ideas from the list and the specific reason to deprioritize — too risky, too much effort, wrong moment.]

## Next step
To move forward with the top recommendation: invoke the `pm` skill and ask to write a PRD for [idea name].
---

After saving, reply: "Ideation saved to `docs/ideation-[problem].md` — top recommendation: [idea name]."
