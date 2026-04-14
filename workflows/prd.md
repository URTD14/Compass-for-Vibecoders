# PRD Workflow

## Input
You have a feature or product to write a PRD for. If the name or one-line purpose is missing from the user's message, ask ONE question: "What does this do in one sentence?"

## Output

Write the PRD using the structure below. Save to `docs/prd-[feature-kebab-case].md`.

---
# PRD: [Feature Name]
**Date:** [today's date]
**Status:** Draft

## Problem
[2–3 sentences. What user pain does this solve? Why does it matter now?]

## Users
[Who specifically experiences this? e.g. "Solo founders shipping their first SaaS product"]

## Goals
- [ ] [Measurable outcome — e.g. "Users generate a PRD in under 60 seconds"]
- [ ] [Measurable outcome]

## Non-goals
- [What this will NOT do — be specific, not vague]

## User Stories
1. As a [user], I want [action] so that [outcome]
2. As a [user], I want [action] so that [outcome]
3. As a [user], I want [action] so that [outcome]

## Requirements
**Must have:**
- [Specific, unambiguous requirement]

**Nice to have:**
- [Specific requirement]

## Success Metrics
| Metric | Target |
|---|---|
| [e.g. Time to first PRD] | [e.g. < 60 seconds] |
| [e.g. User completes without help] | [e.g. > 80%] |

## Open Questions
- [ ] [Decision that must be made before building]
---

After saving, reply: "PRD saved to `docs/prd-[name].md`"
