# signal-hiring-intent-capture

## Purpose

Capture and qualify buying signals from job-posting activity, then output a
list that can be routed into outbound and ABM workflows.

## Inputs Required

- target roles and role keywords
- ICP company constraints
- signal recency window in days
- destination output schema

## Signal Logic

Treat hiring as intent when:

1. role maps to an operational pain your solution solves
2. role posted recently
3. company fits ICP baseline

Disqualify when:

- role is unrelated to target problem
- role is stale outside recency window
- company fails hard ICP filters

## Execution Sequence

1. ingest job-post records
2. normalize role titles and seniority
3. apply ICP hard filters
4. score signal strength
5. enrich account and contact layer
6. output route and first action

## Scoring Model

Use a 0-100 score:

- role relevance: 40
- recency: 25
- ICP fit: 25
- supporting context: 10

## Output Format

- `company_name`
- `company_domain`
- `trigger_role`
- `signal_date`
- `signal_score`
- `icp_fit_status`
- `route`
- `owner`
- `first_move`

## Fail Conditions

Stop and request correction if:

- role mapping dictionary is missing
- recency window is not defined
- destination schema is missing required routing fields

