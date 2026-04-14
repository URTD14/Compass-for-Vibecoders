# Pre-mortem Workflow

## What this is
A pre-mortem imagines the feature already failed — 6 months from now, it flopped. You work backwards to find out why, then mitigate the risks before you build. Best run after writing a PRD, before starting engineering.

## Input
Feature name and what it's supposed to do. If `docs/prd-*.md` exists, read it first (max 80 lines).

## Process
1. Assume it's 6 months post-launch and the feature failed badly
2. Brainstorm 8–12 plausible reasons it could have failed
3. Categorize each: Product / Technical / Market / Execution / User behavior
4. Score each: Likelihood (H/M/L) × Impact (H/M/L)
5. Define mitigations for the top 5 risks

## Output

Save to `docs/premortem-[feature-kebab-case].md`:

---
# Pre-mortem: [Feature Name]
**Date:** [today's date]
**Hypothesis being tested:** [What you're betting on]

## Failure scenario
It's [6 months from today's date]. The feature launched but failed. Usage is near zero / the metric didn't move / churn spiked. What went wrong?

## Risk map

| Risk | Category | Likelihood | Impact | Priority |
|---|---|---|---|---|
| [e.g. Users don't understand the referral mechanic] | Product | H | H | P1 |
| [e.g. Referral links break on mobile] | Technical | M | H | P2 |
| [e.g. Competitor ships equivalent feature first] | Market | L | M | P3 |
| [Continue for all risks — aim for 8–12] | | | | |

*Categories: Product / Technical / Market / Execution / User behavior*

## Mitigations for top 5 risks

### Risk 1: [Name]
**Mitigation:** [Specific action to reduce likelihood or impact]
**Owner:** [Who is responsible]
**By when:** [Date or milestone]

### Risk 2: [Name]
[same format]

### Risk 3: [Name]
[same format]

### Risk 4: [Name]
[same format]

### Risk 5: [Name]
[same format]

## Launch tripwires
If any of these happen, stop and reassess:
- [ ] [Leading failure signal to watch in first 48h — e.g. "< 5% of signups use referral link"]
- [ ] [Metric that signals early failure]
- [ ] [Rollback trigger — e.g. "Error rate > 2% → revert"]
---

After saving, reply: "Pre-mortem saved to `docs/premortem-[name].md`"
