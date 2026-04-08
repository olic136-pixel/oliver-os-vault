---
created: '2026-04-08'
entities: []
jurisdictions:
  - ADGM-FSRA
  - DIFC-DFSA
  - VARA-Dubai
  - El-Salvador-DASP
last_reviewed: '2026-04-08'
people: []
projects:
  - Qanun-Platform
source: manual
status: active
tags:
  - qanun
  - saas
  - regulatory
  - ai
  - malis
  - lexis
type: project
---

# Qanun Platform

## Overview
Qanun is a UAE-focused, Middle East and offshore regulatory intelligence SaaS platform. It is in active development — not yet deployed commercially. The platform grew directly from the regulatory intelligence built while structuring Fuutura across multiple jurisdictions. Qanun is not incorporated — it is a product in development, operating under no legal entity of its own yet.

## Product description
Qanun provides AI-powered regulatory intelligence for compliance professionals operating in:
- ADGM/FSRA
- DIFC/DFSA
- VARA (Dubai)
- Offshore jurisdictions

**Core products:**
- **Research** (gold) — AI-powered regulatory research using the MALIS 10-agent pipeline and LEXIS 7-agent legal research system
- **Studio / Compliance Studio** (teal) — regulatory document suite builder, multi-jurisdiction positioning

## Technical stack
- Backend: FastAPI (Python), deployed on Hetzner
- Frontend: Next.js on Vercel
- Pipeline: MALIS (10-agent, 63,397-provision corpus), LEXIS (7-agent)
- Vector store: Pinecone with voyage-law-2 embeddings
- MCP servers: adgm-corpus, malis-intelligence, lexis, obsidian-vault, filesystem, github
- Corpus: 63,397 ADGM/FSRA, DIFC/DFSA, El Salvador provisions indexed

## Regulatory corpus coverage
- ADGM/FSRA — full rulebook coverage
- DIFC/DFSA — full rulebook coverage
- VARA Dubai — included
- El Salvador — included
- Expanding to additional jurisdictions

## Brand and design
- Navy #0B1829, Gold #C4922A, Teal #0F7A5F
- Inter font 400/600
- Two-product architecture: Research (gold), Studio (teal)

## Current development status
- Production deployment: Hetzner (FastAPI + Caddy + systemd at api.qanun.io)
- Frontend: Vercel (qanun.io)
- Obsidian vault integration: active
- Compliance Studio: in development
- Commercial launch: not yet

## Open items
- [ ] Compliance Studio — complete multi-jurisdiction document builder
- [ ] Commercial launch strategy — UAE/Middle East market
- [ ] Entity structure — Qanun not yet incorporated

## Key decisions log
| Date | Decision | Made by |
|------|----------|---------|
| | UAE/Middle East/offshore positioning confirmed | Oliver |
| | Grew from Fuutura multi-jurisdiction regulatory work | — |
| | Two-product brand: Research + Studio | Oliver |

## History
- Built from scratch using Claude Code
- MALIS pipeline: 9 phases, LangGraph, 31-tool MCP server
- LEXIS: 7-agent legal research system with context budget design
- Competitive analysis completed vs aosphere, Regology, Harvey, Legora
- Full brand identity and design system established
- Production deployment on Hetzner with webhook-based auto-deploy
