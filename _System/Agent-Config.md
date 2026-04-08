---
created: '2026-04-08'
last_reviewed: '2026-04-08'
type: system
---

# Agent Configuration

## Classification ontology

The classification agent uses these lists to tag incoming captures. Update them as new entities, projects, jurisdictions, and people are added to the vault.

### Projects
- Fuutura-Token
- Fuutura-Exchange
- Qanun-Platform
- Libertas-Practice
- Dubai-Law-Firm
- TradeDar
- Abu-Dhabi-Relocation
- Wife-Health
- Human8
- Human8-Qlarifai
- Human8-CRM
- Human8-Roblodex
- Human8-Nodex

### Entities
- Fuutura Treasury Inc
- Fuutura Technologies Corp
- Human8
- Qlarifai Holding
- Qlarifai Care
- Libertas Chambers
- Dubai Law Firm
- TradeDar
- Oliver Cook KC
- Cook Family

### Jurisdictions
- England and Wales Criminal
- ADGM/FSRA
- DIFC/DFSA
- Dubai Onshore
- El Salvador DASP
- BVI
- Panama
- VARA Dubai
- UK FCA/CQC
- UAE CMA

### People
- Jez Noah Ali
- IK
- Ellis
- Torres Legal
- Dentons
- Ahmed
- David Gevorkian
- Gabe
- Ammar
- Tai
- Hub71
- Fran
- Jack
- Alex
- Libertas Clerks

## Source tags
| Source | Tag | Notes |
|--------|-----|-------|
| WhatsApp | `whatsapp` | Via WasenderAPI MCP |
| Gmail | `gmail` | Via Gmail MCP |
| M365 email | `m365` | Via Microsoft Graph MCP |
| PLAUD device | `plaud` | Via plaud-sync-for-obsidian |
| Google Calendar | `calendar` | Via GCal MCP |
| Instagram | `instagram` | Via forward-to-email habit |
| Voice memo | `voice` | Via Whisper endpoint or direct dictation |
| Manual | `manual` | Direct entry |

## Classification rules

1. Every incoming capture is tagged with `type: inbox` and `status: active` until manually routed.
2. Agent identifies projects, entities, jurisdictions, and people from the ontology above and populates frontmatter arrays.
3. If a capture touches two or more projects, a connection alert is written to `/_System/Connection-Map.md`.
4. Captures containing dates and counterparty names are flagged as potential matter updates for `/08-Matters/`.
5. Captures mentioning Fran, Jack, or Alex are tagged `family: true` and routed to `/09-Family/` context.
6. Voice notes (source: voice or plaud) receive `type: voice-note` and are summarised before filing.

## Voice routing logic

- Duration < 2 minutes: single inbox note
- Duration 2–15 minutes: inbox note with summary + action items extracted
- Duration > 15 minutes (meeting): full transcript + summary + action items + matter/project link if identifiable

## Scheduling

- Morning cron (07:00 UTC): classification agent runs on new inbox items, daily briefing note written to `/06-Weekly/`
- Pre-meeting: triggered 30 minutes before any Google Calendar event, brief written to `/06-Weekly/Briefs/`
- On-demand: triggered by direct Claude session with vault context loaded
