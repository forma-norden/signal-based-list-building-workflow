# Test: signal-tech-stack-qualification

Load skill: `.claude/skills/signal-tech-stack-qualification.md`

## Prompt

```text
Read .claude/skills/signal-tech-stack-qualification.md

Inputs:
- target technologies: HubSpot, Salesforce, Segment
- disqualifying technologies: legacy on-prem CRM only
- ICP: B2B SaaS, 50-500 employees
- output policy: include route and message_angle

Return qualification workflow and scoring logic.
```

## Must Pass Checklist

- [ ] Defines stack states: fit, gap, conflict, unknown
- [ ] Includes normalization before scoring
- [ ] Includes ICP blend with stack signal
- [ ] Includes route and message angle output
- [ ] Includes disqualification logic

## Failure Indicators

- No disqualifying logic
- Treats unknown stack as fit
- No structured output fields

