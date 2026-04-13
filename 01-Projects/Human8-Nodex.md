---
created: '2026-04-08'
entities:
  - Human8
jurisdictions: []
last_reviewed: '2026-04-12'
people:
  - Gabe
  - Ammar
  - Houda-Aoussar
projects:
  - Human8-Nodex
source: whatsapp-enriched
status: active
tags:
  - human8
  - nodex
  - circa
  - venture-architecture
  - bit
type: project
---

# Human8 — Nodex

## Overview
Nodex is a venture architecture platform — the "venture passport" — making venture progress portable across accelerators, incubators, and funders. Lead architect: [[03-People/Gabe]]. Category: "Venture Architecture Network" / "Experience Intelligence."

**Core proposition:** The early and growth stage venture ecosystem lacks a shared source of truth. Nodex creates the venture passport to make that truth portable.

## Architecture

### Three-Layer Scoring
- **Layer 1 — Completeness:** Deterministic, binary, auditable. Field completeness evidence counts, revenue data presence, time-based metrics. Pure function: criteria measurable, versioned, reproducible. Maps to traffic lights.
- **Layer 2 — Coherence:** Cross-pillar tension detection. "Think Tetris." Systemic risks invisible to flat checklists.
- **Layer 3 — Human:** Governed human validation. Operators verify and stamp stage transitions on behalf of institutions.

### CIRCA Dimensions (5 scored + 2 maturity)
- **Scored:** Coherence, Capability, Validation, Viability, Risk Awareness
- **Maturity tracks:** Impact (drafted — 6 fields, 5 levels, SDG flow), Founder Growth (constraints only)

### Type-Polymorphic Rubric
Six venture types: SERVICE (fully designed), PHYSICAL PRODUCT, DIGITAL PRODUCT, PLATFORM, CREATIVE, CONSULTING (all at Base only).

### PILOT Stage Weights
Validation=0.9, Viability=0.6, Risk Awareness=0.6, Capability=0.55, Coherence=0.5 (Σ=3.15)

### Business Intelligence Twin (BIT)
See [[01-Projects/Human8-BIT]]. Conversational AI that builds venture profiles through dialogue, auto-maps to CIRCA pillars, scores each RBC pillar with reasoning. Modes: Default, Investor, Operator, Impact.

### Ontology Engine
Enter unstructured domain → create meaning layer → capture signal → compound intelligence → continuous loop.

## Design Principles

- Scoring rubric evolution must be usage-driven not committee-driven
- Our rubric is an ontology — it tells you when you are outside of it
- Don't fall into the Infinicube Trap — need perimeter definition
- Framework lets founders opt out with rationale rather than silently low-scoring them
- More deterministic engineering, less LLM dependency
- Governance lock: design changes escalate in cost exponentially through lifecycle

## Revenue Model

- White-label role architecture for institutions (universities, accelerators, corporate venture)
- Intelligence Cooperative — shared intelligence layer compounding across deployments
- API into [[01-Projects/Human8-Thrive-Hub]] bundle
- Long-term: venture tokenisation play (fixing secondary venture markets)

## Remaining Design Work

- 5 venture types need type-specific overlay criteria
- Field design (clusters, structured inputs, narrative prompts)
- Maturity level criteria (5 levels: Aware → Thriving)
- Cross-dimensional signal definitions
- Multi-founder handling UX
- BIT observation patterns for support routing
- Scoring engine architecture (weight tables, rubric versioning)
- Conversational AI onboarding → field population mapping

## Key People

| Person | Role |
|--------|------|
| [[03-People/Gabe]] | Lead systems architect |
| [[03-People/Ammar]] | UX/experience design input |
| [[03-People/Houda-Aoussar]] | Proposed equity contributor — Layer 1 build |
| Oliver Cook KC | IP architecture, legal structuring, investor lens |

## Status
**Active — architecture design phase. SERVICE type fully designed. 5 types remaining at Base criteria.**

## Corporate vehicle
- [[02-Entities/Human8]] — UK company, Oliver/Gabe/Ammar equal shareholders

## Open items
- [x] Define scope — ✅ completed via WhatsApp integration
- [ ] Complete type-specific criteria for 5 remaining venture types
- [ ] Houda onboarding — equity vs paid work decision
- [ ] Category charter ("Venture Architecture Network") needs formalisation
- [ ] Voice-first BIT onboarding (Boardy-style) — post-MVP

## Recordings

- [[00-Inbox/PLAUD/plaud-2026-01-11-01-11-meeting-accelerator-platform-mvp-and-investment-strategy|01-11 Meeting: Accelerator Platform, MVP, and Investment Strategy — 2026-01-11]]
- [[00-Inbox/PLAUD/plaud-2026-01-10-01-10-meeting-digital-incubator-onboarding-and-platform-features|01-10 Meeting: Digital Incubator Onboarding and Platform Features — 2026-01-10]]
- [[00-Inbox/PLAUD/plaud-2026-01-10-01-10-meeting-product-vision-roadmap-and-mvp-prototyping|01-10 Meeting: Product Vision, Roadmap, and MVP Prototyping — 2026-01-10]]
- [[00-Inbox/PLAUD/plaud-2026-01-10-01-10-strategic-definition-and-competitive-analysis-for-a-digital-incubator-platform|01-10 Strategic Definition and Competitive Analysis for a Digital Incubator Platform — 2026-01-10]]
