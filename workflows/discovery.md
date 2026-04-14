# Discovery & Research Synthesis Workflow

## Input
Raw research — user interview notes, transcripts, survey responses, or support tickets. The user will either paste content directly or give a file path. If a file path is given, read the file (max 200 lines).

## Synthesis process
1. Read all input
2. Identify 3–5 recurring themes (look for repetition across sources)
3. For each theme, find 2–3 supporting quotes or data points
4. Write one opportunity statement per theme using "How might we..." format

## Output

Save to `docs/discovery-[topic-kebab-case].md`:

---
# Discovery: [Topic]
**Date:** [today's date]
**Sources:** [What was analyzed — e.g. "8 user interviews, 45 survey responses"]

## Summary
[2–3 sentences. What is the single most important insight from all of this?]

## Theme 1: [Name]
**Insight:** [What users consistently think, feel, or do]

**Evidence:**
> "[Quote or paraphrase]" — [source type, e.g. User interview]
> "[Quote or paraphrase]" — [source type]

**Opportunity:** How might we [action] so that [user benefit]?

## Theme 2: [Name]
[same format as Theme 1]

## Theme 3: [Name]
[same format as Theme 1]

## Recommended next steps
- [ ] [Specific action — e.g. "Run 3 more interviews to validate Theme 2"]
- [ ] [Specific action — e.g. "Add Theme 1 insight to the active PRD"]
---

After saving, reply: "Discovery saved to `docs/discovery-[topic].md`"
