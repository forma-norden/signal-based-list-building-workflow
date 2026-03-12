# Test: signal-visitor-identification

Load skill: `.claude/skills/signal-visitor-identification.md`

## Prompt

```text
Read .claude/skills/signal-visitor-identification.md

Inputs:
- events: repeated pricing visits, return visits, demo page visits
- enrichment stack: Clay + Apollo
- outreach SLA: 24 hours
- target pages: /pricing, /demo, /integrations

Return event scoring and routing workflow.
```

## Must Pass Checklist

- [ ] Distinguishes high-intent from low-intent events
- [ ] Includes confidence bucket logic
- [ ] Includes enrichment plus ICP filtering sequence
- [ ] Includes route output fields
- [ ] Includes safety rule against weak identity assumptions

## Failure Indicators

- Treats all events equally
- Omits confidence logic
- Routes low-confidence rows directly to aggressive outbound

