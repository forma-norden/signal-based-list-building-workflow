# signal-tech-stack-qualification

## Purpose

Qualify accounts based on technology footprint and stack-gap signals, then
produce routeable records for targeted outbound.

## Inputs Required

- target technologies
- disqualifying technologies
- ICP company constraints
- stack data provider confidence level

## Signal Logic

Signal examples:

- uses adjacent stack but missing required capability
- recently adopted enabling platform relevant to your solution
- has mature CRM but no enrichment or automation layer

Disqualify examples:

- stack conflict with your solution requirement
- non-target architecture patterns

## Execution Sequence

1. ingest stack signals by account domain
2. normalize technology names
3. classify stack state (`fit`, `gap`, `conflict`, `unknown`)
4. blend with ICP fit data
5. generate route and first message angle

## Output Format

- `company_name`
- `company_domain`
- `detected_stack`
- `stack_state`
- `stack_signal_score`
- `icp_fit_status`
- `route`
- `message_angle`

## Quality Rules

- normalize vendor aliases before scoring
- separate direct detections from inferred detections
- do not treat unknown stack as fit

## Fail Conditions

Stop and request correction if:

- target or disqualifying stack list is missing
- provider confidence is unknown
- output route policy is missing

