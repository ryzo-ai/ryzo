# Ryzo: open-source skills for B2B go-to-market

Three Claude Code plugins, 39 skills, MIT licensed. They cover outbound, RevOps and paid ads, and they are the same playbooks Ryzo AI Workflows runs for B2B teams, with client detail removed.

```
/plugin marketplace add ryzo-ai/ryzo
/plugin install outbound-os@ryzo       # 9 skills + 2 commands: cold outbound
/plugin install revops-os@ryzo         # 16 skills: RevOps
/plugin install performance-os@ryzo    # 14 skills: paid ads
```

You can install one, two or all three. Each skill is a plain markdown file, so you can also copy them into `~/.claude/skills/` and edit them.

## Who it's for

- Founders and small GTM teams at B2B SaaS companies who want an agent to do the repeatable GTM work. Developer-tool companies are a good fit: their products and buyers are already agent friendly.
- Operators who already use Claude Code and want tested starting points instead of blank prompts.
- Agencies that want to see how a delivery workflow can be written down so an agent can run it.

## What's inside

### outbound-os: from company context to a sent campaign

1. `company-context-builder`: a living file with your product, ICP, lingo and win cases
2. `market-problems-deep-research`: the problems your ICP has, with sources
3. `list-building`: a target list built from a hypothesis, not a database export
4. `data-points-builder`: research per prospect that an email can use
5. `table-enrichment`: fills the gaps in a prospect table
6. `tiering-segmentation`: tiers a list so each tier gets the right level of effort
7. `email-generation`: assembles emails from the datapoints and your rules
8. `copy-feedback`: reads each email the way the prospect would, before you send
9. `run-lemlist`: sets up, launches and monitors campaigns in lemlist

Plus two commands for the infrastructure: `domain-infrastructure-setup` and `domain-warmup-orchestrator`.

### revops-os: a CRM that holds up

- Start here: `revops` routes your question to the right skill
- Lifecycle: `lifecycle-stages`, `lead-scoring`, `lead-routing`, `pipeline-management`
- System: `crm-automation`, `deal-desk`, `data-hygiene`
- Numbers: `revops-dashboards`, `attribution`, `forecasting`
- Delivery workflow: `revops-audit`, `revops-blueprint`, `revops-implement`, `revops-optimize`, `revops-coach`

Works with HubSpot or Attio. Bring your own access.

### performance-os: paid ads on Google, Meta and LinkedIn

- Start here: `paid-ads` routes to the right platform or capability
- Platforms: `google-ads`, `meta-ads`, `linkedin-ads`
- Setup and measurement: `conversion-tracking`, `audience-targeting`, `reporting`
- Running it: `campaign-audit`, `campaign-optimization`, `bidding-strategy`, `budget-pacing`
- Creative and testing: `ad-copywriting`, `creative-strategy`, `ab-testing`

## Where to start

| If you want | Install | First ask |
|---|---|---|
| A list and a first campaign | `outbound-os` | "Build company context for my company" |
| To know what's wrong in your CRM | `revops-os` | "Audit our CRM" |
| To know where your ad budget leaks | `performance-os` | "Audit our ad account" |

## How the skills work

- Each skill reads your own context file and writes its output as a file, so the next skill can use it.
- Review the output before anything goes live. The delivery skills ask for sign-off before they change a CRM, and the outbound flow has you approve emails and preview leads before a campaign starts.
- No keys ship in these repos. Credentials come from your own environment variables or integrations.

## Plugins

| Plugin | Repo |
|---|---|
| outbound-os | [ryzo-ai/outbound-os](https://github.com/ryzo-ai/outbound-os) |
| revops-os | [ryzo-ai/revops-os](https://github.com/ryzo-ai/revops-os) |
| performance-os | [ryzo-ai/performance-os](https://github.com/ryzo-ai/performance-os) |

## More from Ryzo

- The playbooks, step by step, with diagrams: [ryzo.nl/resources/playbooks](https://ryzo.nl/resources/playbooks)
- Issues and pull requests are welcome. Please read the contributing note in each plugin repo first, and never include client names or credentials.

Built by Ryzo AI Workflows. MIT licensed.
