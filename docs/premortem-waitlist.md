# Pre-mortem: Viral Waitlist
**Date:** 2026-04-14
**Hypothesis being tested:** A referral-powered waitlist turns signups into distribution — at least 30% of new signups come through referral links, without any paid spend.

## Failure scenario
It's October 2026. The waitlist launched, collected ~200 emails in week one, then flatlined. Referral rate sits at 4%, not 30%. Nobody shared their link. The founder moved on. What went wrong?

## Risk map

| Risk | Category | Likelihood | Impact | Priority |
|---|---|---|---|---|
| Users don't understand what moving up the list actually gets them — no clear launch date or reward | Product | H | H | P1 |
| Referral link is buried after signup — users see their position then leave, never finding the share mechanic | Product | H | H | P2 |
| Position number is too high (e.g. #847) and feels hopeless — users don't bother sharing | User behavior | H | M | P3 |
| Referral link doesn't render correctly on mobile — broken copy, wrong URL, no og:image | Technical | M | H | P4 |
| The product itself has no clear value prop — people won't evangelize something they don't believe in | Market | M | H | P5 |
| A spam wave registers thousands of fake emails, inflating positions and killing trust | Technical | M | M | P6 |
| Founder doesn't follow up — waitlist goes cold, no launch email, people forget they signed up | Execution | H | H | P7 |
| Duplicate emails handled poorly — error message instead of showing existing position, users feel punished for re-engaging | Product | M | M | P8 |
| Competitor (e.g. Waitlist.ly, Beehiiv referrals) already solves this better and for free | Market | L | M | P9 |
| Position recalculation is slow or wrong — referrer doesn't see their rank improve, loses motivation | Technical | L | H | P10 |

*Categories: Product / Technical / Market / Execution / User behavior*

---

## Mitigations for top 5 risks

### Risk 1: No clear reward for moving up
**Why it kills the feature:** If users don't know what #1 on the list gets them, there's no reason to share. "Early access" is not a benefit — "first 50 users get lifetime pricing" is.
**Mitigation:** Before launching the waitlist, define and display the concrete reward for top-N users. Show it on the confirmation page, not buried in a follow-up email. Examples: "Top 100 users get 50% off forever", "First 50 get a 1:1 onboarding call."
**Owner:** Founder / product
**By when:** Before any public traffic hits the waitlist

### Risk 2: Share mechanic is invisible after signup
**Why it kills the feature:** Most referral loops die because the referral link is one more click away from where users land. Attention drops 80% per additional click.
**Mitigation:** The referral link + copy button must be the first thing users see on the confirmation page — above the fold, impossible to miss. No "check your email" — show it immediately. Test on mobile before launch.
**Owner:** Frontend / founder
**By when:** Pre-launch QA

### Risk 3: Position number feels hopeless
**Why it kills the feature:** "You're #847" is demotivating. Users do the math and give up.
**Mitigation:** Frame position as progress, not rank. "You're in the top 12% — refer 3 friends to break the top 5%" is a completely different psychological experience. Alternatively, cap the visible list size early (show position out of 200, not 2000) or use percentile framing instead of raw numbers.
**Owner:** Product / copy
**By when:** Before public launch

### Risk 4: Referral link broken on mobile
**Why it kills the feature:** Most shares happen on mobile. A broken og:image or malformed URL means the share looks like spam — zero clicks.
**Mitigation:** Test the referral link on iOS Safari, Android Chrome, iMessage preview, Twitter card, and WhatsApp before launch. Add og:title and og:description even if og:image is a nice-to-have.
**Owner:** Engineering
**By when:** Pre-launch checklist gate — do not launch without passing this

### Risk 7: Waitlist goes cold — no follow-up
**Why it kills the feature:** A waitlist with no launch email is a graveyard. Users forget they signed up within 2 weeks.
**Mitigation:** Before collecting a single email, write the launch email. Schedule at least 2 check-in emails: one at 2 weeks ("still coming, here's what we're building") and one at launch ("you're in"). Use Loops or Resend — this is explicitly a non-goal to build in-house.
**Owner:** Founder
**By when:** Before launch day

---

## Launch tripwires
If any of these happen in the first 48 hours, stop and reassess before continuing to drive traffic:

- [ ] Referral share rate < 8% (well below the 25% target — indicates the share mechanic isn't visible or the reward isn't compelling)
- [ ] Mobile referral link renders broken on any major platform (iMessage, WhatsApp, Twitter)
- [ ] > 15% of signups are duplicate email submissions (indicates form confusion or a spam wave)
- [ ] Zero position recalculations fire in first 24h despite signups (indicates referral tracking is broken)
- [ ] Error rate on signup endpoint > 1% (revert and fix before driving more traffic)
