# Test: signal-hiring-intent-capture

Load skill: `.claude/skills/signal-hiring-intent-capture.md`

## Prompt

```text
Read .claude/skills/signal-hiring-intent-capture.md

Inputs:
- role keywords: "demand generation manager", "revops manager", "sales operations"
- ICP: B2B SaaS, 50-500 employees, US and UK
- recency window: 7 days
- output schema: company_name, company_domain, trigger_role, signal_score, route, owner, first_move

Return capture workflow and output logic.
```

## Must Pass Checklist

- [ ] Uses role relevance, recency, and ICP fit in scoring
- [ ] Includes disqualification criteria
- [ ] Includes explicit execution sequence
- [ ] Produces routeable output schema
- [ ] Specifies fail conditions

## Failure Indicators

- No scoring model
- No disqualifier logic
- Generic advice without output contract

