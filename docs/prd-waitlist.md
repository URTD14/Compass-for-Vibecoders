# PRD: Viral Waitlist
**Date:** 2026-04-14
**Status:** Draft

## Problem
When launching a SaaS, founders have no way to build pre-launch demand or create urgency. A flat email capture form gives users no incentive to share, leaving growth entirely to paid channels. Referral-powered waitlists (like the ones that made Robinhood and Superhuman famous) turn every signup into a distribution channel — but they're expensive to build from scratch.

## Users
Solo founders and vibe-coders shipping their first or second SaaS product who want to validate demand and grow an audience before launch, without a marketing budget.

## Goals
- [ ] At least 30% of waitlist signups come from referral links (not direct)
- [ ] Average user shares their referral link at least once within 24h of signing up
- [ ] Waitlist signup to referral share conversion > 25%

## Non-goals
- Will NOT send automated drip email sequences (use an external tool like Loops or Resend for that)
- Will NOT support OAuth / social login for waitlist entry — email only
- Will NOT show a public leaderboard of top referrers
- Will NOT integrate with CRMs at launch

## User Stories
1. As a prospective user, I want to join the waitlist with my email so that I can get early access when the product launches
2. As a waitlist member, I want to see my current position number so that I know where I stand and feel motivated to move up
3. As a waitlist member, I want a unique referral link I can share so that I can move up the list when friends sign up through my link

## Requirements

**Must have:**
- Email capture form with duplicate detection (same email = show existing position, not a new entry)
- Unique referral code generated per signup, embedded in a shareable URL
- Position number displayed immediately after signup (e.g. "You're #247 on the waitlist")
- Position recalculated when a referred user signs up (referrer moves up by 1 per referral)
- Referral link pre-formatted for easy copy (e.g. one-click copy button)
- Admin view: CSV export of all waitlist entries with email, position, referral count, signup date

**Nice to have:**
- "You moved up X spots this week" email notification when position improves
- Shareable card image (og:image) generated per user showing their position
- Waitlist count shown publicly on landing page (social proof)

## Success Metrics
| Metric | Target |
|---|---|
| Referral-driven signups | ≥ 30% of total |
| Share rate (signup → share within 24h) | ≥ 25% |
| Duplicate email submission rate | < 5% (indicates form clarity) |
| Time to join waitlist | < 30 seconds |

## Open Questions
- [ ] Should referral position jumps be capped (e.g. max +50 spots) to prevent gaming?
- [ ] Does position reset if a referred user unsubscribes or bounces?
- [ ] What happens at launch — do we email the top N users first, or all at once?
