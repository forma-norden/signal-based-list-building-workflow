# signal-visitor-identification

## Purpose

Convert anonymous website activity into identified accounts and contacts with
confidence scoring and route recommendations.

## Inputs Required

- visitor activity source
- target pages and event definitions
- enrichment stack available
- outreach SLA in hours

## Signal Logic

High-intent events include:

- repeated pricing page visits
- return visits within short windows
- high-intent page combinations in one session

Low-intent events include:

- single short-duration visits
- non-commercial page-only traffic

## Execution Sequence

1. ingest raw visitor events
2. map events to account candidates
3. score event intensity and recency
4. enrich account and contact data
5. apply ICP filters
6. route to outbound, ABM assist, or monitor

## Confidence Model

Use confidence buckets:

- `high`: strong event pattern plus ICP fit
- `medium`: partial event pattern with fit
- `low`: weak pattern or missing fit evidence

## Output Format

- `account_domain`
- `account_name`
- `event_pattern`
- `event_recency_hours`
- `confidence_bucket`
- `icp_fit_status`
- `route`
- `owner`
- `first_move`

## Safety Rules

- Do not fabricate person-level identity from weak account-only signals.
- Do not route low-confidence rows directly to aggressive outbound.

## Fail Conditions

Stop and request correction if:

- event definitions are missing
- enrichment coverage is too low for routing
- outreach SLA is undefined

