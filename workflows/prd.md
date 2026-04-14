# PRD Workflow

## Input
Feature or product to write a PRD for. If the name or one-line purpose is missing, ask ONE question: "What does this do in one sentence?"

## Output

Write the PRD below. Save to `docs/prd-[feature-kebab-case].md`.

---
# PRD: [Feature Name]
**Date:** [today's date]
**Status:** Draft

## Hypothesis
We believe that [building this] for [specific user] will [outcome]. We'll know we're right when [metric] changes by [amount] within [timeframe].

## Problem
[2–3 sentences. What user pain does this solve? Why now? Ground it in a real situation — not an abstraction.]

## Users
[Not "users." Be specific: e.g. "Solo founders with < 3 months to launch, no marketing budget"]

## Job to Be Done
When [situation], users want to [motivation], so they can [outcome].

## Goals
- [ ] [Measurable outcome tied to a specific metric]
- [ ] [Measurable outcome]

## Non-goals
- [Specific thing this will NOT do — and why, e.g. "No email sequences — use Loops for that"]

## Requirements

| Requirement | Priority | Risk |
|---|---|---|
| [Specific, unambiguous requirement] | Must | H/M/L |
| [Specific requirement] | Should | H/M/L |
| [Specific requirement] | Could | H/M/L |

## Success Metrics
| Metric | Baseline | Target | Timeframe |
|---|---|---|---|
| [North star metric] | [current or "unknown"] | [target] | [e.g. 30d post-launch] |
| [Secondary metric] | | | |

## Assumption Log
| Assumption | Confidence | How to validate |
|---|---|---|
| [What we're assuming is true] | H/M/L | [Experiment or data source] |

## Decision Log
| Decision | Chosen | Alternatives | Rationale |
|---|---|---|---|
| [e.g. Auth method] | [Email only] | [OAuth, phone] | [Lower friction for MVP] |

## Open Questions
- [ ] [Must resolve before building — who owns answering this?]
---

After saving, reply: "PRD saved to `docs/prd-[name].md`"
