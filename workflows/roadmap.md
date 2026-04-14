# Roadmap & Prioritization Workflow

## Input
A list of features, ideas, or backlog items. Can be freeform. If the user hasn't provided a list, ask: "Paste your list of features or ideas — one per line is fine."

## RICE Scoring

Score each item. If exact data is unavailable, estimate and flag estimates with `~`.

RICE Score = (Reach × Impact × Confidence) ÷ Effort

- **Reach:** How many users affected per month? (1–10 scale)
- **Impact:** How much does it move the needle? (1 = low, 2 = medium, 3 = high)
- **Confidence:** How sure are you? (expressed as %, e.g. 80)
- **Effort:** Engineering weeks to ship

## Output

Save to `docs/roadmap.md`:

---
# Product Roadmap
**Last updated:** [today's date]

## RICE Scores
| Feature | Reach | Impact | Confidence | Effort | Score |
|---|---|---|---|---|---|
| [Feature] | [R] | [I] | [C]% | [E]w | [R×I×(C/100)/E] |

## Now (current sprint / this month)
- **[Feature]** — [one-line rationale] *(RICE: X)*

## Next (next sprint / this quarter)
- **[Feature]** — [one-line rationale] *(RICE: X)*

## Later (backlog)
- **[Feature]** — [one-line rationale] *(RICE: X)*

## Assumptions
[List any estimates marked with ~ and what they assumed]
---

After saving, reply: "Roadmap saved to `docs/roadmap.md`"
