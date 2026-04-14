# Discovery & Research Synthesis Workflow

## Input
Raw research — interview notes, transcripts, survey responses, or support tickets. User pastes directly or gives a file path. If a file path, read it (max 200 lines).

## Synthesis process
1. Read all input
2. Identify 3–5 recurring themes
3. For each theme: JTBD statement + 2 quotes + opportunity score
4. Surface key assumptions the data supports or breaks

## Opportunity Scoring (Ulwick formula)
For each theme, score 1–5:
- **Frequency:** How often does this situation occur?
- **Importance:** How much does it matter to the user?
- **Satisfaction gap:** How badly does the current solution fall short?
- **Score** = Importance + (Importance − Satisfaction gap) — higher = bigger opportunity

## Output

Save to `docs/discovery-[topic-kebab-case].md`:

---
# Discovery: [Topic]
**Date:** [today's date]
**Sources:** [What was analyzed — e.g. "8 user interviews, 45 survey responses"]

## Summary
[2–3 sentences. The single most important insight. What changes because of this?]

## Theme 1: [Name]
**JTBD:** When [situation], users want to [motivation], so they can [outcome].

**Opportunity score:** [X/10]
Frequency [X/5] · Importance [X/5] · Satisfaction gap [X/5]

**Evidence:**
> "[Quote]" — [source type]
> "[Quote]" — [source type]

**Assumption surfaced:** [What we now believe to be true — or false]

## Theme 2: [Name]
[same format as Theme 1]

## Theme 3: [Name]
[same format as Theme 1]

## Assumptions to validate next
| Assumption | Confidence | Cheapest way to test |
|---|---|---|
| [What we're assuming] | H/M/L | [e.g. "5 more interviews" or "A/B test copy"] |

## Recommended next steps
- [ ] [Specific action with owner — e.g. "Add Theme 1 to active PRD"]
- [ ] [Specific action]
---

After saving, reply: "Discovery saved to `docs/discovery-[topic].md`"
