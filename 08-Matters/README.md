---
created: '2026-04-08'
last_reviewed: '2026-04-08'
type: system
---

# Matters — Conventions and Protocol

## Purpose
This folder contains one sub-folder per active criminal matter. Each matter sub-folder is the single source of truth for that case — instructions, hearings, evidence notes, PLAUD transcripts, and strategy.

## How matters enter the vault

### From the Libertas Diary (primary route)
The Google Calendar MCP reads Libertas Diary events. When a hearing is detected that does not have an existing matter sub-folder, the calendar agent:
1. Creates a new sub-folder at `/08-Matters/[Defendant-Surname]-[Offence-Slug]/`
2. Copies the Matter Template into it
3. Pre-populates frontmatter from the diary event (date, court, hearing type)
4. Adds the hearing to `Hearings.md`
5. Generates a pre-hearing brief 30 minutes before the listing

### Manual creation
Use the template at `/Templates/Matter.md`. Copy the Matter-Template sub-folder structure. Name the folder `[Defendant-Surname]-[Offence-Slug]`.

## Folder structure per matter
```
/08-Matters/
  [Defendant-Surname]-[Offence-Slug]/
    _index.md         ← Matter overview, charges, representation, fee note
    Hearings.md       ← Chronological hearing log
    Evidence.md       ← Evidence issues, admissibility, expert evidence
    Instructions.md   ← Instructions received, advice given
```

## PLAUD integration
- PLAUD device records hearings and conferences
- Transcripts sync via plaud-sync-for-obsidian plugin to `/00-Inbox/`
- Agent links transcript to the correct matter sub-folder based on date and named parties
- Transcript file linked in `Hearings.md` against the relevant hearing entry

## Hearing type taxonomy
| Abbreviation | Full name | Notes |
|-------------|-----------|-------|
| PTPH | Plea and Trial Preparation Hearing | First Crown Court hearing |
| PTH | Preparation for Trial Hearing | Case management |
| PCMH | Pre-Charge Management Hearing | Pre-charge stage |
| Trial | Trial | Main event |
| Sentence | Sentencing hearing | Post-conviction |
| Confiscation | POCA confiscation | Post-conviction financial |
| Appeal | Appeal hearing | CACD or Supreme Court |
| Conference | Solicitor / client conference | Not a court hearing |

## Naming conventions
- Sub-folder: `[Defendant-Surname]-[Short-Offence]` e.g. `Smith-Fraud` or `Jones-EncroChat`
- PLAUD transcripts: `YYYY-MM-DD-[Hearing-Type]-[Matter-Slug].md`
- All dates: ISO format YYYY-MM-DD

## Active matters index
See [[08-Matters/_index]] for the Dataview index of all active matters.
