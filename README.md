# signal-based-list-building-workflow

Signal-driven list-building workflows for B2B SaaS and tech teams that need
higher conversion lead lists before outbound execution. This package focuses on
capture and qualification signals, hiring intent, visitor intent, LinkedIn
engagement, tech stack fit, and funding triggers, then converts them into
routeable prospect lists.

## What's Inside

| File | What it does |
|------|-------------|
| `.claude/skills/signal-hiring-intent-capture.md` | Builds intent capture from hiring events with scoring and qualification filters. |
| `.claude/skills/signal-visitor-identification.md` | Converts anonymous website traffic into enriched, route-ready contacts and accounts. |
| `.claude/skills/signal-linkedin-engagement-capture.md` | Turns LinkedIn post engagement into scored lead lists with operational handoff output. |
| `.claude/skills/signal-tech-stack-qualification.md` | Qualifies accounts from technology footprint and stack-gap indicators. |
| `.claude/skills/signal-funding-trigger-monitor.md` | Detects and prioritizes newly funded accounts using post-funding buying-window logic. |
| `.claude/skills/signal-source-prioritizer.md` | Prioritizes signal sources by ICP fit, recency, confidence, and operational cost. |
| `tests/` | Prompt-based tests and validation checklists for all six skills. |

## Prerequisites

- [ ] Claude Code installed and running
- [ ] CRM access (HubSpot or Salesforce)
- [ ] Enrichment and contact-data access (Clay, Apollo, or equivalent)
- [ ] One or more signal sources (jobs, visitor ID, LinkedIn, funding, technographics)
- [ ] Outbound execution destination defined (sequencer or CRM tasking flow)

## Installation

1. Clone the repo:
   ```bash
   git clone https://github.com/forma-norden/signal-based-list-building-workflow.git
   ```
2. Copy skills into your project:
   ```bash
   cp -r signal-based-list-building-workflow/.claude/skills your-project/.claude/
   ```
3. Load the relevant signal skill in Claude Code before execution.

## Usage

```text
Read .claude/skills/signal-source-prioritizer.md

Inputs:
- target ICP: B2B SaaS, 50-500 employees, US and UK
- active sources: hiring signals, website visitor ID, LinkedIn engagement
- capacity: 500 new rows per week
- outbound SLA: outreach within 48 hours

Return:
1) ranked source order
2) scoring logic
3) execution cadence
4) handoff format
```

Expected output:

- ranked signal-source plan
- explicit scoring and disqualification logic
- operator-ready handoff table

## Who This Is For

GTM engineers, RevOps leads, VP Sales, and founders at B2B SaaS and tech
companies with 50 to 500 employees who are building or consolidating their
outbound infrastructure and want to reduce tool sprawl through
better-engineered GTM systems.

---

## From the Forma Nôrden GTM Library

This is a free resource from the [Forma Nôrden open-source GTM library](https://formanorden.com/open-source).

- [Open-source GTM resources](https://formanorden.com/open-source) — all repos in the library
- [GTM engineering blog](https://formanorden.com/blog) — strategy, systems, and outbound deep-dives
- [All resources](https://formanorden.com/resources) — guides, frameworks, and templates

If this saves you time, star the repo and follow [Forma Nôrden on LinkedIn](https://linkedin.com/company/formanorden).

Built by [Forma Nôrden](https://formanorden.com) — GTM engineering for B2B tech.

