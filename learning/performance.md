# iGen Performance

Rolling metrics by channel: Facebook, outreach, Stripe, Supabase. Week-over-week trends. Best/worst content by concrete metric.
All numbers from platform APIs/dashboards, never estimates.

---

## Channel: Facebook (FB publishing loop)

| Period | Posts queued | Posts verified published | Reach | Reactions | Comments | Shares | Clicks |
|---|---|---|---|---|---|---|---|
| Cycles 1-17 (2026-09-27..29) | 34 | 0 (unattended gate) | n/a | n/a | n/a | n/a | n/a |
| Manual test publish (2026-09-29T18:01Z) | - | 1 (exec 97bb7020, SUCCESS, CreatePostWithPhotos) | n/a | n/a | n/a | n/a | n/a |
| Cycle 18 (2026-09-29T15:38Z, text-only teaching post) | 1 (bridge HTTP 200 "Accepted") | 0 (unattended gate) | n/a | n/a | n/a | n/a | n/a |
| Cycle 19 (2026-09-29, text-only story post, AI Research Assistant Kit) | 1 (bridge HTTP 200 "Accepted") | 0 (unattended gate) | n/a | n/a | n/a | n/a | n/a |
| Cycle 006 watch (2026-09-29T22:2xZ, text-only teaching post P-017) | 1 (P-017 bridged) | PENDING verified post ID | n/a | n/a | n/a | n/a | n/a |

Trend: publishing architecture verified once manually; unattended verification previously blocked by Make API paid-plan gate — this run the Make key is SET in the shell, so the watch path (scenario trigger → execution read → post ID) is being exercised end-to-end. Engagement metrics still require FB Graph API access beyond Make CreatePost (not granted). Copy quality checks stay enforced every cycle; the measurable outcome moves from the bridge to the Page the moment a post ID is captured.

## Channel: Outreach

| Period | Targets logged | DMs staged | DMs sent | Opens | Replies | Demos | Conversions |
|---|---|---|---|---|---|---|---|
| Cycles 1-17 | 24+ FB groups | 14 | 0 | 0 | 0 | 0 | 0 |

Trend: zero send path (no messaging connector). Per Cycle Review 001, outreach staging is PAUSED until a compliant channel exists; cycle time reallocated to content quality + product optimization.

## Channel: Stripe

| Period | MRR | Lifetime revenue | Subscribers | One-time sales | Churn | Upgrades |
|---|---|---|---|---|---|---|
| Baseline (2026-07-25/27) | $0.00 | $3.98 | 0 | 2 (x $1.99) | n/a | n/a |
| Cycles 1-17 (2026-09-27..29) | $0.00 | $3.98 | 0 | 0 new | n/a | n/a |
| Cycle 18/19 (2026-09-29) | $0.00 | $3.98 | 0 | 0 new | n/a | n/a |
| Cycle 006 (2026-09-29T22:01Z) | $0.00 | $3.98 | 0 | 0 new | n/a | n/a |

Target: $2,000 MRR = 40 x $49.99/mo Workflow Membership. Subscriptions list verified empty via Stripe API (status all, has_more=false). PaymentIntents verified live each cycle: 2 succeeded x $1.99, 0 new in cycle 006.

## Channel: Supabase

| Metric | Value (verified) |
|---|---|
| products rows | 98 |
| events rows | 1 (test page_view 2026-09-28) |
| feedback rows | 0 |
| outreach rows | 0 |

(Cycle 006: re-verified 98/1/0/0 via SQL. Product conversion pass performed — 6 products revised with stronger value propositions + CTAs:
ai-content-repurposing-engine, roi-calculator, churnguard-ai, ai-workflow-audit-rebuild-kit, solo-founder-automation-suite, ai-verification-control-kit — read-back verified via SELECT.)

## Week-over-week (placeholder — populate next week)

(no full prior week logged yet; first comparison after 7 days of running the loop)

## Best / worst content (placeholder — first engagement data)

(no engagement metrics yet; first real comparison after verified publishes have reach data)

## Cycle 006 conversion actions (Stripe-side, in this cycle)

- 6 products revised: concrete value proposition + CTA in description, sharper tagline (see Supabase SELECT above). Goal: lift click-through iGen.tech → Stripe checkout.
- Funnel tracking: Facebook → iGen.tech → Stripe checkout remains the mission; events table has 1 test page_view — the product page must emit page_view events per slug so funnel conversion can be measured (next cycle improvement).