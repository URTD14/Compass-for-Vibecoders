# User Stories Workflow

## Input
A feature name, description, or PRD reference. If a `docs/prd-*.md` file exists for this feature, read it first (max 80 lines) for context before generating stories.

## Rules
- Each story must be independently shippable where possible
- Acceptance criteria must be binary (pass/fail) — never vague like "works well"
- If a story is too large for one sprint, split it into two

## Output

Generate 3–8 user stories. Save to `docs/stories-[feature-kebab-case].md`:

---
# User Stories: [Feature Name]
**Date:** [today's date]

## Stories

### Story 1: [Short title]
**As a** [specific user type]
**I want to** [specific action]
**So that** [concrete outcome]

**Acceptance Criteria:**
- [ ] [Specific, testable condition]
- [ ] [Specific, testable condition]
- [ ] [Specific, testable condition]

### Story 2: [Short title]
**As a** [specific user type]
**I want to** [specific action]
**So that** [concrete outcome]

**Acceptance Criteria:**
- [ ] [Specific, testable condition]
- [ ] [Specific, testable condition]

[Continue for all stories — minimum 3, maximum 8]

## Out of Scope
- [Related thing that is explicitly NOT included in these stories]
---

After saving, reply: "Stories saved to `docs/stories-[name].md`"
