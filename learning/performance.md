# iGen Performance

Rolling metrics by channel: Facebook, outreach, Stripe, Supabase. Week-over-week trends. Best/worst content by concrete metric.
All numbers from platform APIs/dashboards, never estimates.

---

## Channel: Facebook (FB publishing loop)

| Period | Posts queued | Posts verified published | Reach | Reactions | Comments | Shares | Clicks |
|---|---|---|---|---|---|---|---|
| Cycles 1-17 (2026-09-27..29) | 34 | 0 (unattended gate) | n/a | n/a | n/a | n/a | n/a |
| Manual test publish (2026-09-29T18:01Z) | - | 1 (exec 97bb7020, SUCCESS, CreatePostWithPhotos) | n/a | n/a | n/a | n/a | n/a |

Trend: publishing architecture verified once manually; unattended verification remains blocked by Make API paid-plan gate. Engagement metrics require FB Graph API access (not granted).

## Channel: Outreach

| Period | Targets logged | DMs staged | DMs sent | Opens | Replies | Demos | Conversions |
|---|---|---|---|---|---|---|---|
| Cycles 1-17 | 24+ FB groups | 14 | 0 | 0 | 0 | 0 | 0 |

Trend: zero send path (no messaging connector). No outcome data until a channel is connected.

## Channel: Stripe

| Period | MRR | Lifetime revenue | Subscribers | One-time sales | Churn | Upgrades |
|---|---|---|---|---|---|---|
| Baseline (2026-07-25/27) | $0.00 | $3.98 | 0 | 2 (x $1.99) | n/a | n/a |
| Cycles 1-17 (2026-09-27..29) | $0.00 | $3.98 | 0 | 0 new | n/a | n/a |

Target: $2,000 MRR = 40 x $49.99/mo Workflow Membership. Subscriptions list verified empty via Stripe API.

## Channel: Supabase

| Metric | Value (verified) |
|---|---|
| products rows | 98 |
| events rows | 1 (test page_view 2026-09-28) |
| feedback rows | 0 |
| outreach rows | 0 |

## Week-over-week (placeholder — populate next week)

(no full prior week logged yet; first comparison after 7 days of running the loop)

## Best / worst content (placeholder — first engagement data)

(no engagement metrics yet; first real comparison after verified publishes have reach data)
