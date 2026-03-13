# Ecosystem: signal-based-list-building-workflow

How this repo connects to the rest of the Forma Norden GTM library.

## Works With

| Repo | Relationship | When to use together |
|------|-------------|---------------------|
| `buying-window-signal-workflow` | Downstream | Signal lists feed into scoring and play routing |
| `clay-claude-code-skill-pack` | Downstream | Signal-qualified leads enter Clay for enrichment |
| `cold-email-copy-playbook` | Downstream | Signal type determines copy angle and template |
| `n8n-gtm-workflow-pack` | Parallel | n8n automates signal capture workflows |
| `linkedin-claude-code-workflow` | Parallel | LinkedIn engagement signals captured here |

## Suggested Skill Chains

1. Full signal pipeline: source-prioritizer > [signal capture skills] > multi-source-stacking > `buying-window-signal-workflow` (score) > `clay-claude-code-skill-pack` (enrich) > `cold-email-copy-playbook` (write)
