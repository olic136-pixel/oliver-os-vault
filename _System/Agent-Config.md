---
created: '2026-04-08'
last_reviewed: '2026-04-09'
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
- Human8-BIT
- Human8-School
- Emerging-Stubs

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
- Blue Ocean Academy

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
- Jezz
- IK
- Ellis
- Torres Legal
- Dentons
- Ahmed
- David Gevorkian
- Gabe
- Ammar
- Tai
- Fran
- Jack
- Alex
- Gary Douglas
- Libertas Clerks
- MB
- Bu Eshaaq Ahmed
- Janyl Alpadis
- Ollie Shewan
- Ismail

## Source tags
| Source | Tag | Notes |
|--------|-----|-------|
| WhatsApp | `whatsapp` | Via WasenderAPI webhook |
| Gmail | `gmail` | Via Gmail MCP |
| M365 email | `m365` | Via Microsoft Graph MCP |
| PLAUD device | `plaud` | Via plaud-sync-for-obsidian |
| Google Calendar | `calendar` | Via GCal MCP |
| Instagram | `instagram` | Via forward-to-email habit |
| Voice memo | `voice` | Via Whisper endpoint or direct dictation |
| Manual | `manual` | Direct entry |

## Project keyword mappings (for webhook classifier)
| Project | Keywords |
|---------|---------|
| Fuutura-Token | ftra, whitepaper, tokenomics, tppa |
| Fuutura-Exchange | dasp, el salvador, operating partner, fuutura exchange, fuutura ops |
| Qanun-Platform | qanun, malis, lexis, compliance studio |
| Libertas-Practice | libertas, chambers, brief, hearing, trial, pcmh, ptph, palmer |
| Dubai-Law-Firm | dubai law, difc law, law firm, brigadeer |
| TradeDar | tradedar |
| Abu-Dhabi-Relocation | abu dhabi, yas island, al raha, relocation |
| Wife-Health | healthcare ecosystem (Fran context) |
| Human8 | human8, humanate |
| Human8-Qlarifai | qlarifai, qlarif, cqc, care home, sop |
| Human8-BIT | bit, business intelligence twin |
| Human8-School | blue ocean, school project, freehold, liverpool school |
| Human8-Roblodex | roblodex |
| Human8-Nodex | nodex |
| Human8-CRM | patient management |
| CoLab-App | colab |
| China-Gas-Deal | china, gas deal |

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
