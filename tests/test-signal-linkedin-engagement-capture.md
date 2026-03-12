# Test: signal-linkedin-engagement-capture

Load skill: `.claude/skills/signal-linkedin-engagement-capture.md`

## Prompt

```text
Read .claude/skills/signal-linkedin-engagement-capture.md

Inputs:
- source posts: 3 LinkedIn post URLs on outbound automation
- ICP scoring thresholds: tier 1 >= 80, tier 2 >= 60, tier 3 >= 40
- email validation required: true
- route policy: tier 1 outbound now, tier 2 warm sequence, tier 3 monitor

Return end-to-end capture workflow and output schema.
```

## Must Pass Checklist

- [ ] Includes extraction, deduplication, enrichment, validation, scoring, routing
- [ ] Includes no-routing-without-score rule
- [ ] Includes no-outbound-for-invalid-contact rule
- [ ] Preserves source post traceability
- [ ] Outputs structured fields for handoff

## Failure Indicators

- Skips validation or scoring
- Routes all rows the same way
- No source-post traceability in output

