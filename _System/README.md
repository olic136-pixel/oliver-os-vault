---
type: system
created: '2026-04-08'
last_reviewed: '2026-04-08'
---

# Oliver OS — Personal Knowledge Vault

## Purpose

This vault is a second brain for Oliver Cook KC. It captures, connects, and surfaces knowledge across all active projects, legal matters, relationships, and personal contexts. It is not a document store — it is a thinking environment.

## Vault structure

| Folder | Purpose |
|--------|---------|
| `/00-Inbox` | Raw capture — agent-populated from WhatsApp, email, PLAUD, voice notes, Instagram |
| `/01-Projects` | One note per active initiative |
| `/02-Entities` | Legal and corporate persons |
| `/03-People` | Key relationships |
| `/04-Jurisdictions` | Regulatory and legal environments |
| `/05-Concepts` | Cross-cutting intellectual assets |
| `/06-Weekly` | Operating rhythm — decisions, actions, open items |
| `/07-Archive` | Closed or parked items |
| `/08-Matters` | Barrister cases — one sub-folder per matter |
| `/09-Family` | Personal and family context |
| `/Templates` | One template per note type |
| `/_System` | Vault config, agent schema, connection map |

## Frontmatter schema

Every note carries this schema regardless of type:

```yaml
type: project | entity | person | jurisdiction | concept | weekly | inbox | matter
status: active | parked | archived
projects: []
entities: []
jurisdictions: []
people: []
tags: []
created: YYYY-MM-DD
last_reviewed: YYYY-MM-DD
source: manual | gmail | m365 | whatsapp | plaud | calendar | instagram | voice
```

## Voice capture pipeline

Three modes for capturing unstructured input:

- **Mode 1 — PLAUD**: Device captures meetings and calls. Transcripts sync to `/00-Inbox/` via the plaud-sync-for-obsidian plugin with `source: plaud`.
- **Mode 2 — Ad-hoc voice**: iPhone voice memo → iOS Shortcut → capture email → M365 agent → Whisper transcription → `/00-Inbox/Voice/`.
- **Mode 3 — Direct dictation**: Speak or paste unstructured notes directly to Claude prefixed with `voice note:`. Claude processes and writes the structured note via MCP.

Mode 3 is available immediately. Mode 1 requires PLAUD plugin install. Mode 2 requires Whisper endpoint setup on Hetzner.

## Agent instructions

The classification agent reads this vault's ontology — entities, jurisdictions, projects, people — and uses it to tag incoming captures with correct frontmatter before writing to `/00-Inbox/`. It never overwrites existing notes. It writes connection alerts to `/_System/Connection-Map.md` when cross-project links are detected.

The intelligence agent runs on demand or on schedule. It reads the full vault and produces:
- Daily briefing note in `/06-Weekly/`
- Pre-meeting briefs triggered by calendar events
- Connection map updates
- Document generation with full vault context loaded

## Separation from Qanun vault

This vault is entirely separate from the Qanun regulatory corpus vault. Cross-references to ADGM/FSRA or DIFC/DFSA provisions link by text citation only — no wikilinks into the Qanun vault. The two vaults are operationally independent.
