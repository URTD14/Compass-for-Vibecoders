# Roadmap & Prioritization Workflow

## Input
A list of features, ideas, or backlog items. Freeform. If missing, ask: "Paste your list — one per line is fine. Also: what's the one metric you're trying to move this quarter?"

## OKR linkage
The north star metric the team is chasing this quarter becomes the scoring lens. Any feature that doesn't connect to it goes to Later automatically — no exceptions.

## RICE Scoring
Score each item. Flag estimates with `~`.

RICE = (Reach × Impact × Confidence) ÷ Effort
- Reach: users/month affected (1–10)
- Impact: 1 low / 2 medium / 3 high
- Confidence: % certainty (e.g. 80)
- Effort: engineering weeks

## Output

Save to `docs/roadmap.md`:

---
# Product Roadmap
**Last updated:** [today's date]
**North star this quarter:** [metric the team is trying to move — e.g. "week-2 retention"]

## Strategic themes
- **[Theme 1]:** [one-line — e.g. "Reduce time-to-value for new signups"]
- **[Theme 2]:** [one-line]

## RICE Scores
| Feature | Theme | Reach | Impact | Conf | Effort | Score |
|---|---|---|---|---|---|---|
| [Feature] | [Theme] | [R] | [I] | [C]% | [E]w | [R×I×(C/100)/E] |

## Now (this sprint / month)
- **[Feature]** — [one-line rationale tied to north star] *(RICE: X)*
  - Opportunity cost: not doing [alternative] this cycle

## Next (next sprint / quarter)
- **[Feature]** — [one-line rationale] *(RICE: X)*

## Later (backlog)
- **[Feature]** — [one-line rationale] *(RICE: X)*

## Dependencies
- [Feature A] must ship before [Feature B] — [reason]

## Assumptions
[Any estimates flagged with ~ and what they assumed]
---

After saving, reply: "Roadmap saved to `docs/roadmap.md`"
