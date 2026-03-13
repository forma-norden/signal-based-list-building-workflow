# signal-multi-source-stacking

Use this skill to combine signals from multiple sources into a compound scoring
framework that drives outreach prioritization.

## Required Inputs

- list of active signal sources with their data fields
- ICP definition for weighting
- outreach capacity (how many contacts can be worked per week)

## Multi-Signal Scoring Framework

### Signal Weight Assignment

| Signal Category | Base Weight | Rationale |
|----------------|-------------|-----------|
| Website visit (identified) | 30 | Highest intent, real-time |
| Content engagement (download/webinar) | 25 | Active interest |
| Job change (champion) | 25 | Relationship + timing |
| Funding event | 20 | Budget availability |
| Hiring signal | 15 | Growth indicator but indirect |
| Tech stack change | 15 | Consideration but not always active |
| LinkedIn engagement | 10 | Interest but low commitment |
| Company event (award, expansion) | 10 | Firmographic, not behavioral |

### Recency Multiplier

| Freshness | Multiplier |
|-----------|-----------|
| Within 24 hours | 2.0x |
| Within 7 days | 1.5x |
| Within 14 days | 1.2x |
| Within 30 days | 1.0x |
| 30-60 days | 0.5x |
| 60+ days | 0.25x |

### ICP Fit Multiplier

| ICP Tier | Multiplier |
|----------|-----------|
| Tier A (perfect fit) | 1.5x |
| Tier B (strong fit) | 1.2x |
| Tier C (acceptable) | 1.0x |
| Tier D (poor fit) | 0.5x |

### Compound Score Formula

```
compound_score = SUM(signal_weight × recency_multiplier) × icp_fit_multiplier
```

### Action Thresholds

| Score Range | Action | SLA |
|-------------|--------|-----|
| 150+ | Immediate manual outreach (AE) | < 1 hour |
| 100-149 | SDR personalized sequence | < 24 hours |
| 50-99 | Automated warm sequence | < 72 hours |
| 20-49 | Marketing nurture | This week |
| 0-19 | Monitor for new signals | Ongoing |

## Deduplication Across Sources

1. Match by email first, then by company domain + title.
2. When the same account appears in multiple sources, keep the highest-scoring signal.
3. Stack signals on the same account (do not deduplicate signals, deduplicate contacts).
4. Track signal source for ROI attribution.

## Execution Sequence

1. List all active signal sources and their output fields.
2. Assign base weights from the table above (adjust for your ICP).
3. Calculate recency multiplier for each signal.
4. Apply ICP fit multiplier to the compound score.
5. Rank contacts by compound score.
6. Apply action thresholds based on outreach capacity.
7. Route to appropriate play (manual AE, SDR sequence, automation).

## Output Contract

Return:

- signal source inventory with weights
- compound score for each contact/account
- prioritized action list with SLA assignments
- routing recommendations by score tier
- weekly capacity plan matching contacts to outreach slots

## Anti-Patterns

- treating all signals as equal weight
- ignoring signal freshness (a 90-day-old website visit is not hot)
- deduplicating signals instead of deduplicating contacts
- no ICP filter on signal feeds (processing irrelevant accounts)
- not tracking source for ROI measurement
