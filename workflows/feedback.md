# User Feedback Synthesis Workflow

## Input
Raw feedback — app store reviews, support tickets, survey responses, NPS comments, or user emails. User either pastes content directly or provides a file path. If a file path is given, read the file (max 200 lines).

## Synthesis process
1. Read all feedback
2. Assess overall sentiment: Positive / Mixed / Negative, with approximate % split
3. Find the top 3 recurring themes — these can be complaints, praise, or requests
4. Pull 2 direct quotes per theme (verbatim if possible)
5. Suggest concrete next actions, separated by effort level

## Output

Save to `docs/feedback-[YYYY-MM-DD].md` (use today's date):

---
# Feedback Analysis — [Date]
**Source:** [e.g. "App Store reviews", "NPS survey", "support tickets"]
**Volume:** [Number of feedback items analyzed]
**Sentiment:** [Positive / Mixed / Negative] (~[X]% positive, ~[Y]% negative)

## Theme 1: [Name]
**Signal strength:** [High / Medium / Low]

**Quotes:**
> "[Direct quote or close paraphrase]"
> "[Direct quote or close paraphrase]"

**Suggested action:** [Specific, actionable — e.g. "Add empty state copy explaining X"]

## Theme 2: [Name]
[same format as Theme 1]

## Theme 3: [Name]
[same format as Theme 1]

## Quick wins (< 1 week to ship)
- [ ] [Specific action]
- [ ] [Specific action]

## Strategic implications
[1–2 sentences on what this feedback reveals about a larger product direction decision]
---

After saving, reply: "Feedback analysis saved to `docs/feedback-[date].md`"
