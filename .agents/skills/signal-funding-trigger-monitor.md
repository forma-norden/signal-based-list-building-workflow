# signal-funding-trigger-monitor

## Purpose

Monitor and prioritize funding-event signals so teams engage accounts during
early post-funding buying windows.

## Inputs Required

- funding event source
- recency threshold in days
- funding-stage weighting model
- ICP fit constraints

## Signal Logic

Funding signal strength increases when:

- funding event is recent
- stage implies active scaling pressure
- headcount growth or hiring context is present

Funding signal weakens when:

- event is old
- company is outside ICP
- no supporting operational signal exists

## Execution Sequence

1. ingest funding events
2. filter by recency
3. classify by stage and likely pressure type
4. enrich account context
5. combine with ICP and supporting signals
6. output route and urgency

## Urgency Model

- `urgent`: high fit plus recent event plus support signals
- `standard`: high fit with moderate support
- `monitor`: weak support or uncertain fit

## Output Format

- `company_name`
- `company_domain`
- `funding_stage`
- `funding_date`
- `signal_urgency`
- `signal_score`
- `route`
- `owner`
- `first_move`

## Fail Conditions

Stop and request correction if:

- recency threshold is missing
- funding-stage weights are undefined
- route policy by urgency is missing

