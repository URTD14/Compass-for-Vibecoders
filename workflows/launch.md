# Launch Workflow

## Input
Feature or product name and what it does. If unclear, ask: "What does it do and who is it for?"

Default audience: indie hackers / solo founders / vibe-coders. If the user specifies a different audience, adjust copy tone accordingly.

## Output

Save to `docs/launch-[feature-kebab-case].md`:

---
# Launch Plan: [Feature / Product Name]
**Launch date:** [from user, or "TBD"]

## One-liner
[Single sentence — user benefit first, not feature name first]

## Pre-launch checklist
- [ ] Feature works end-to-end on production
- [ ] Error states handled (empty state, failure, loading)
- [ ] Docs / onboarding updated if applicable
- [ ] Analytics events firing correctly
- [ ] Rollback plan: [describe rollback method, e.g. "feature flag off"]
- [ ] [Any feature-specific item based on what the user described]

## Day-of checklist
- [ ] Deploy to production
- [ ] Smoke test the critical path as a real user
- [ ] Publish announcement (copy below)
- [ ] Monitor error rates for 30 minutes post-deploy

## Post-launch checklist
- [ ] Check analytics after 24 hours
- [ ] Respond to first wave of user feedback
- [ ] Document what to improve next time

## Announcement copy

**Short (tweet / product update / changelog):**
[1–2 sentences. Lead with what the user can now do, not what you built.]

**Long (blog post intro / detailed changelog):**
[3–5 sentences. Problem you saw → what you built → how to get started → invitation to try it.]
---

After saving, reply: "Launch plan saved to `docs/launch-[name].md`"
