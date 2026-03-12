# Test: signal-source-prioritizer

Load skill: `.claude/skills/signal-source-prioritizer.md`

## Prompt

```text
Read .claude/skills/signal-source-prioritizer.md

Inputs:
- sources: hiring intent, visitor identification, LinkedIn engagement, funding triggers
- ICP: B2B SaaS, 50-500 employees, US and UK
- weekly capacity: 1000 rows
- outreach SLA: 48 hours
- cost profile:
  - hiring intent: medium
  - visitor identification: medium-high
  - linkedin engagement: low-medium
  - funding triggers: low

Return ranked source order, row budget, owner assignment, and cadence.
```

## Must Pass Checklist

- [ ] Uses weighted model with explicit criteria
- [ ] Produces ranked source list with scores
- [ ] Includes weekly row budget allocation
- [ ] Includes owner and cadence fields
- [ ] Includes queue or spillover handling

## Failure Indicators

- No weighted scoring
- No ranking table
- No capacity-aware allocation

