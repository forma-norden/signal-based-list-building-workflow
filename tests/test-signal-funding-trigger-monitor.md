# Test: signal-funding-trigger-monitor

Load skill: `.claude/skills/signal-funding-trigger-monitor.md`

## Prompt

```text
Read .claude/skills/signal-funding-trigger-monitor.md

Inputs:
- source: Crunchbase export
- recency threshold: 30 days
- stage weights: seed 20, series-a 35, series-b+ 45
- ICP: B2B SaaS, US/UK, 50-1000 employees
- route policy by urgency: urgent outbound now, standard ABM assist, monitor nurture

Return scoring model, urgency logic, and output contract.
```

## Must Pass Checklist

- [ ] Uses recency, stage, and supporting context in prioritization
- [ ] Produces urgency buckets
- [ ] Includes output fields with route and owner
- [ ] Includes fail conditions for missing thresholds or weights
- [ ] Includes execution sequence from ingest to route

## Failure Indicators

- No urgency model
- No stage weighting logic
- No route mapping by urgency

