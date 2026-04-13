---
created: '2026-04-09'
entities:
  - Human8
last_reviewed: '2026-04-12'
people:
  - Gabe
  - Ammar
  - Houda-Aoussar
projects:
  - Human8-BIT
source: whatsapp-enriched
status: active
tags:
  - human8
  - bit
  - business-intelligence
  - conversational-ai
type: project
---

# Human8 — BIT (Business Intelligence Twin)

## Overview
BIT is the conversational AI core of [[01-Projects/Human8-Nodex]]. A digital twin of a venture that builds its profile through dialogue, auto-maps unstructured input to CIRCA pillars, and provides scored assessments with reasoning.

## What BIT Does

- Conversational AI that builds venture profiles through dialogue (not forms)
- Auto-maps unstructured data to CIRCA pillars
- Suggests primary/secondary SDG alignment with explanation
- Scores each RBC pillar with reasoning for each score
- Operates in modes: Default/Mixed, Investor, Operator, Impact
- Updates live venture record from conversation
- Summarises venture to user
- Nudges founders on tasks based on conversational input and programme context

## MVP Status (Nov 2025–present)

Built by [[03-People/Gabe]] using Claude Code (Max plan). Painful build with multiple context crashes, Docker issues. Methodology pivoted to multi-AI: Claude (BAI), ChatGPT (QAI), Gemini (MAI).

**Working features:**
- Input unstructured information → returns structured data
- Live venture record update
- Auto-mapping to CIRCA pillars
- SDG alignment suggestion with explanation
- Per-pillar RBC scoring with reasoning

**Remaining:**
- Make more conversational (BIT asks questions back)
- Better UI mapping
- Cloud hosting for team testing
- RAG incorporation (currently text-based, evolve to document ingestion)
- Voice-first onboarding (Boardy.ai-style) — see notes below

## Voice-First Vision

Oliver proposed Boardy.ai-style voice agent as BIT front end:
- Founders communicate via WhatsApp → AI voice call → BIT profile creation → continued check-ins
- Individual BIT with own unique voice and knowledge
- Language-specific models for Arabic (Middle East), native languages (India)
- "Humanate CoLab — we speak the language of venture"
- Gabe confirmed: "entirely feasible post-MVP"

## Architecture Principles

- "The measurement tool is coupled to the measurement" — more deterministic engineering, less LLM dependency
- Layer 1 stop line: field completeness + pillar coherence roll up only. Do NOT cross-validate across pillars or BIT drifts into Layer 2.
- BIT's catch rate depends on variable LLM domain knowledge — need perimeter definition
- "What if as users speak to BIT, they see the local Nodex network grow?" — visual network expansion as engagement metaphor

## Key People

| Person | Role |
|--------|------|
| [[03-People/Gabe]] | Architect, MVP builder |
| [[03-People/Houda-Aoussar]] | Proposed Layer 1 build contributor |

## Corporate vehicle
- [[02-Entities/Human8]]

## Open items
- [x] Define scope — ✅ completed via WhatsApp integration
- [ ] Voice-first onboarding (Boardy-style) — post-MVP
- [ ] Cloud hosting for collaborative testing
- [ ] RAG document ingestion
- [ ] Multi-language voice models

## Recordings

- [[00-Inbox/PLAUD/plaud-2026-02-05-02-05-meeting-global-economy-hub-rwanda-project-and-advisory-board-collaboration|02-05 Meeting: Global Economy Hub, Rwanda Project, and Advisory Board Collaboration — 2026-02-05]]
- [[00-Inbox/PLAUD/plaud-2026-01-11-01-11-meeting-accelerator-platform-mvp-and-investment-strategy|01-11 Meeting: Accelerator Platform, MVP, and Investment Strategy — 2026-01-11]]
- [[00-Inbox/PLAUD/plaud-2026-01-10-01-10-meeting-digital-incubator-onboarding-and-platform-features|01-10 Meeting: Digital Incubator Onboarding and Platform Features — 2026-01-10]]
- [[00-Inbox/PLAUD/plaud-2026-01-10-01-10-meeting-product-vision-roadmap-and-mvp-prototyping|01-10 Meeting: Product Vision, Roadmap, and MVP Prototyping — 2026-01-10]]
- [[00-Inbox/PLAUD/plaud-2026-01-10-01-10-strategic-definition-and-competitive-analysis-for-a-digital-incubator-platform|01-10 Strategic Definition and Competitive Analysis for a Digital Incubator Platform — 2026-01-10]]
- [[00-Inbox/PLAUD/plaud-2026-01-04-01-04-meeting-unified-healthcare-platform-patient-os-cqc-auditing-ai-and-business-strategy|01-04 Meeting: Unified Healthcare Platform (Patient OS), CQC Auditing AI, and Business Strategy — 2026-01-04]]
- [[00-Inbox/PLAUD/plaud-2025-12-22-12-22-meeting-business-identity-regenerative-business-and-bit-ai-tool-development|12-22 Meeting: Business Identity, Regenerative Business, and 'Bit' AI Tool Development — 2025-12-22]]
