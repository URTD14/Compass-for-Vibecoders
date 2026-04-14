# Strategic Brief Workflow

## What this is
A one-page document that forces clarity on why you're building something and what winning looks like. Use it to align stakeholders, secure resources, or pressure-test an idea before committing a team to it. If you can't fill this out clearly, you're not ready to build.

## Input
Initiative name and what it is. If `docs/prd-*.md` exists, read it first (max 80 lines). If not, ask: "What is this and why are we doing it now?"

## Output

Save to `docs/brief-[initiative-kebab-case].md`:

---
# Strategic Brief: [Initiative Name]
**Date:** [today's date]
**Owner:** [Who is accountable — one name]
**Status:** Draft

## The bet
[1–2 sentences. Frame it as a bet, not a plan. "We believe that X is true, and if we're right, Y happens. If we're wrong, Z is the fallback."]

## Problem
[3–5 sentences max. What is broken, for whom, and how do you know? Cite a real signal — a metric that's wrong, a user quote, a competitor move, a market shift. If you don't have a signal, that's an open question.]

## Proposed solution
[2–3 sentences. What capability are we creating? Not how — what. An engineer should be able to read this and know the scope without being told the implementation.]

## Why us, why now
[2–3 sentences. Why is this team positioned to solve it? What makes this the right moment — competitive window, internal capability, user demand signal?]

## What success looks like
| Metric | Baseline | Target | Timeframe |
|---|---|---|---|
| [Primary metric] | [current] | [target] | [when] |
| [Secondary metric] | [current] | [target] | [when] |

## What failure looks like
[1–2 sentences. How would you know in 90 days this was the wrong bet? What would you see — or not see?]

## Top risks
| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| [Biggest risk] | H/M/L | H/M/L | [How we reduce it] |
| [Second risk] | H/M/L | H/M/L | [How we reduce it] |

## The ask
[What decision or resource is needed from the reader? Be specific — "Approve 6 weeks of eng time", "Greenlight the experiment", "Unblock the API access". One clear ask.]

## What we're not doing
[The closest alternative considered and why it's the wrong bet right now]
---

After saving, reply: "Brief saved to `docs/brief-[name].md`"
