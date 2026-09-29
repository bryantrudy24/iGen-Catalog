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
| Cycle 006 watch (2026-09-29T22:2xZ, text-only teaching post P-017) | 1 (P-017 bridged) | 1 — VERIFIED BASELINE (Commander-confirmed visible on Page; exec 4f5833176d374134bef8a4242b3a10e4 SUCCESS) | n/a | n/a | n/a | n/a | n/a |
| Cycle 007 (2026-09-29T22:49Z, text-only positioning post P-018) | 1 (P-018 bridged) | 1 (exec 142c2849aa97462e8c4d0764d058a92e SUCCESS) — DEFECT: no https://igen.tech URL in copy (CTA rule violation shipped) | n/a | n/a | n/a | n/a | n/a |

Trend: publishing loop is now end-to-end verified — the watch procedure produces SUCCESS executions against the Page. First verified baseline (P-017) recorded. Cycle 007 exposed the CTA gate gap: a post without a URL still shipped because enforcement ran at draft time only. The script now has a pre-bridge CTA/URL gate (no https://igen.tech => AI_PENDING, exit 2) so no future post ships without a funnel URL. Engagement metrics still require FB Graph API access beyond Make CreatePost (not granted); reach/reactions/clicks remain n/a until that or Page Insights access exists. Funnel: Facebook → iGen.tech → Stripe checkout is the measured mission.

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
| Cycle 007 (2026-09-29T22:49Z) | $0.00 | $3.98 | 0 | 0 new | n/a | n/a |

Target: $2,000 MRR = 40 x $49.99/mo Workflow Membership. Subscriptions list verified empty via Stripe API (status all, has_more=false). PaymentIntents verified live each cycle: 2 succeeded x $1.99 (90-day-content-engine), 0 new in cycle 007. Checkout surface verified live: 1 active payment link (plink_1UL3gAPHXel7gDrWOOFv3UEh, livemode, submit_type=subscribe, url https://buy.stripe.com/4gM00lgmSa0u0sp440bII00).

## Channel: Supabase

| Metric | Value (verified) |
|---|---|
| products rows | 98 |
| events rows | 1 (test page_view 2026-09-28) |
| feedback rows | 0 |
| outreach rows | 0 |

(Cycle 007: re-verified 98/1/0/0 via SQL. Funnel landing pages verified reachable and CTA-correct:
- https://igen.tech/products/ai-workflow-audit-rebuild-kit — live, Buy Now $49.99, description carries https://igen.tech/ai-workflow-audit-rebuild-kit
- https://igen.tech/products/ai-subscription-audit — live, Buy Now $9.99, claim "Most users cut 1-3 AI subscriptions in the first pass" backs P-020
- Payment link https://buy.stripe.com/4gM00lgmSa0u0sp440bII00 active (livemode).)

## Week-over-week (placeholder — populate next week)

(no full prior week logged yet; first comparison after 7 days of running the loop)

## Best / worst content (placeholder — first engagement data)

(no engagement metrics yet; first real comparison after verified publishes have reach data)

## Cycle 007 conversion actions (funnel-building, in this cycle)

- Baseline publish recorded: P-017 (teaching) is the first verified publish (Commander Page-confirmed + exec SUCCESS).
- Cycle 007 published P-018 (positioning) — recorded as a defect: it shipped without a URL; the concrete outcome is the hardened CTA gate, not the post.
- P-019 repaired with URL; P-020 queued (pain pillar, AI Subscription Audit $9.99, claim matches live product page).
- Funnel verification complete: iGen.tech → product page (Buy Now) → Stripe checkout all reachable from public URLs. Funnel events still limited (1 test page_view); next improvement remains emitting page_view events per product slug so click-through can be measured.