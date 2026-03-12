# signal-linkedin-engagement-capture

## Purpose

Transform LinkedIn post engagement into an operational list with scores, routes,
and first actions.

## Inputs Required

- source post URLs
- ICP scoring criteria
- enrichment and email-validation path
- route policy by score tier

## Signal Logic

Engagement indicates topical relevance when:

- engagement context matches target problem
- engager role fits ICP persona model
- recency supports timely outreach

## Execution Sequence

1. collect reactors and commenters from selected posts
2. deduplicate person and company entities
3. enrich titles, companies, and contacts
4. validate contactability status
5. score against ICP criteria
6. assign route and produce export-ready output

## Scoring and Routing

Tier model:

- tier 1: immediate outbound or ABM
- tier 2: assisted warm sequence
- tier 3: monitor and nurture

## Output Format

- `first_name`
- `last_name`
- `title`
- `company_name`
- `company_domain`
- `signal_source_post`
- `engagement_type`
- `icp_score`
- `icp_tier`
- `route`
- `first_move`

## Quality Rules

- no routing without score
- no outbound route for invalid contacts
- preserve source-post traceability for every row

## Fail Conditions

Stop and request correction if:

- source posts are missing
- scoring thresholds are undefined
- contact validation status is missing

