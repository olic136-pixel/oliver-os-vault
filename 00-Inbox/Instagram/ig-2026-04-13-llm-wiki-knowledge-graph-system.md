---
type: inbox
status: active
projects:
  - '[[Human8]]'
  - '[[Human8-Nodex]]'
  - '[[Qlarifai-CRM]]'
entities:
  - '[[Human8]]'
jurisdictions: []
people: []
tags:
  - instagram
  - ai-agents
  - knowledge-management
  - rag
  - knowledge-graph
  - obsidian
  - claude
created: '2026-04-13'
last_reviewed: '2026-04-13'
source: instagram
instagram_url: 'https://www.instagram.com/p/DW12SKokRG0/'
instagram_author: '@jesserurka'
---
# LLM Wiki Pattern — Multi-Agent Knowledge Graph System

> Saved from Instagram — @jesserurka, 2026-04-13

## Core Insight
Andrej Karpathy (OpenAI co-founder) published an "LLM wiki pattern" that mirrors what @jesserurka claims to have already built for clients via their product "openclaw." The system ingests documents (PDFs, docs, markdown), uses a dedicated AI "Librarian" sub-agent to structure everything, and renders a 3D mind graph showing knowledge growth — with episodic memory weaving context between queries. Unlike standard RAG (which rediscovers information each query), this approach compounds knowledge into a cohesive multi-agent system. Oliver likely saved this because it closely mirrors the architecture aspirations for his own Obsidian-based knowledge vault and AI agent layer.

## Key Points
- Andrej Karpathy published an LLM wiki pattern for persistent, structured knowledge
- The system uses a dedicated sub-agent ("Librarian") with single responsibility for structuring ingested content
- Documents are ingested (PDFs, docs, markdown) and structured automatically
- A 3D mind graph visualisation shows knowledge growing over time
- Episodic memory weaves context between separate knowledge items
- Differentiates from standard RAG: this compounds knowledge rather than rediscovering it per query
- Live in production for client "openclaw" dashboards

## Relevance to Active Work
This is highly relevant to Oliver's [[Human8]] ecosystem and the [[Human8-Nodex]] knowledge-graph project. The "Librarian" sub-agent pattern could inform how the oliver-os vault ingestion agents are designed. The episodic memory concept connects to the ongoing work on contextual AI memory across [[Qlarifai-CRM]] and [[Human8-BIT]]. The Obsidian + Claude integration Oliver is already building follows a very similar architecture.

## Action Items
- [ ] Look up Andrej Karpathy's LLM wiki pattern paper/post for detailed architecture
- [ ] Evaluate the "Librarian" sub-agent pattern for oliver-os ingestion pipelines
- [ ] Consider episodic memory approaches for cross-session context in Human8 agents
- [ ] Check out openclaw's implementation for inspiration

## Source Content
**Author:** @jesserurka
**Caption:** Andrej Karpathy (OpenAI co-founder) just dropped his LLM wiki pattern. The exact system I already built. Not a demo. Live in client openclaw dashboards right now. My clients dump PDFs, docs, markdown → AI librarian structures everything → 3D mind graph shows their knowledge growing. Episodic memory weaving in-between. This isn't RAG where you rediscover info every query. This compounds into a cohesive multi-agent knowledge system.
**Hashtags:** #openclaw #claude #obsidian #aiagents #claudecode
**URL:** [View on Instagram](https://www.instagram.com/p/DW12SKokRG0/)

## Visual Notes
The video shows a diagram of a multi-agent knowledge system architecture: raw input flows through a dedicated sub-agent called "Librarian" (labelled "always on — single responsibility"), which then feeds into a "Knowledge Store" with connected nodes displayed as a 3D graph. The presenter sits at a desk with a laptop, explaining the architecture in a studio setting with ring lights.
