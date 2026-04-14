# User Stories Workflow

## Input
Feature name, description, or PRD reference. If `docs/prd-*.md` exists for this feature, read it first (max 80 lines).

## Story map structure
- **Epic:** The full capability being built
- **Stories:** User-facing, independently shippable slices
- **Not included here:** Tasks (implementation steps — that's for engineers)

## Rules
- Every story must be independently valuable, not just "part of" a larger flow
- Acceptance criteria are binary (pass/fail) — never vague like "works smoothly"
- If a story takes more than one sprint, split it
- Always include at least one edge case AC per story

## Output

Save to `docs/stories-[feature-kebab-case].md`:

---
# Stories: [Feature Name]
**Epic:** [One sentence — what full capability does this deliver?]
**Date:** [today's date]

## Story 1: [Short title]
**JTBD:** When [situation], I want to [action], so I can [outcome].

**Acceptance Criteria:**
- [ ] [Specific, testable — e.g. "User receives confirmation within 60 seconds"]
- [ ] [Specific, testable]
- [ ] [Edge case — e.g. "Duplicate email shows existing position, not an error"]

**Dependencies:** [None / depends on Story X]

## Story 2: [Short title]
**JTBD:** When [situation], I want to [action], so I can [outcome].

**Acceptance Criteria:**
- [ ] [Specific, testable]
- [ ] [Specific, testable]
- [ ] [Edge case]

**Dependencies:** [None / depends on Story X]

[Continue — minimum 3, maximum 8 stories]

## Out of Scope
- [Specifically excluded thing — with reason]

## Definition of Done (Epic)
- [ ] All stories shipped and smoke-tested in production
- [ ] Analytics events firing for [key user action]
- [ ] Error states handled for [specific failure mode]
- [ ] [Any feature-specific done criterion]
---

After saving, reply: "Stories saved to `docs/stories-[name].md`"
