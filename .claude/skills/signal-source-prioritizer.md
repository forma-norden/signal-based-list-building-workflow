# signal-source-prioritizer

## Purpose

Prioritize which signal sources to run first based on expected pipeline yield,
confidence, speed to action, and operating cost.

## Inputs Required

- active signal sources
- ICP definition
- weekly processing capacity
- outreach SLA
- source-level cost profile

## Prioritization Model

Score each source on 0-100:

- ICP relevance: 30
- recency reliability: 20
- conversion proximity: 20
- data quality and coverage: 15
- operational cost efficiency: 15

## Execution Sequence

1. list all active sources
2. score each source with evidence
3. rank by weighted score
4. cap by processing capacity
5. assign cadence and owner per source
6. define spillover queue for lower-ranked sources

## Source Categories

High-proximity sources:

- visitor intent
- hiring intent
- review-site intent

Medium-proximity sources:

- LinkedIn engagement
- tech-stack gap signals

Lower-proximity sources:

- broad competitor audience signals without supporting context

## Output Format

- `source_name`
- `source_score`
- `priority_rank`
- `weekly_row_budget`
- `owner`
- `cadence`
- `route_policy`

## Fail Conditions

Stop and request correction if:

- capacity is unknown
- source scoring lacks evidence
- owner or cadence fields are missing

