# iGen Lessons

Format: `[date] | [what was tested] | [what happened] | [what we learned] | [what changed as a result]`
One entry per lesson. Every lesson must be specific, testable, and immediately usable.

---

## 2026-09-29 | Automated FB publishing loop, 17 cycles, alternating product/positioning copy with rotated formats | 34 posts queued (17 product + 17 positioning), 0 verified unattended publishes on the Page, 0 new revenue; 1 manual verified test publish (exec 97bb702033e44536954651403eedf3b1, SUCCESS, CreatePostWithPhotos) | Content volume without verified distribution is invisible content. The bottleneck is the publish/verify gate (Make API paid-plan + unattended key approval), not copy quality | Every cycle now records a prediction before posting and a verification step after; Make key approval raised as the single unblocking action

## 2026-09-29 | Format rotation (question, story, listicle, analogy, checklist, etc.) across 17 cycles while keeping pillars fixed at product+positioning | 16 distinct format pairs created, but pillar coverage never moved beyond 2 of 5 | Format rotation alone is cosmetic variety. The premium standard requires pillar rotation (pain / proof / teaching / positioning / story) — formats are the surface, pillars are the strategy | FB loop now rotates all 5 pillars; the specific-claim and competitor-swap tests are enforced per pillar

## 2026-09-29 | Outreach: 24+ FB group targets logged, 14 tailored DM drafts staged across cycles 1-17 | Zero DMs sent (no messaging connector in granted set), zero replies, zero measured outcomes | Staged outreach is not outreach. A draft that never sends produces no signal, so the learning loop has nothing to compare | Outreach counts as an action ONLY when sent; messaging channel connection escalated to Commander as a required capability

## 2026-09-29 | Prediction discipline | Cycles 1-17 recorded no predictions before actions — the COMPARE step had nothing to run against | Without a recorded prediction, gap analysis is impossible; the learning loop cannot run on hindsight alone | Every cycle opens with a PREDICT line in its artifact; no action posts without one

## 2026-09-29 | Stripe/Supabase measurement baseline | Stripe: $3.98 lifetime (2 x $1.99, 90-day-content-engine), 0 subscriptions, MRR $0.00; Supabase: 98 products, 1 page_view event (test), 0 feedback, 0 outreach rows | Measurement exists and is cheap (connectors live); the missing piece was recording predictions to compare against, and a send path for outreach | performance.md now tracks these by channel; the Stripe Revenue Capture routine feeds the ledger on every new payment
