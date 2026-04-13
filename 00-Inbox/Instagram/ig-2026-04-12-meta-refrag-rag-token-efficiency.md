---
type: inbox
status: active
projects:
  - '[[Qanun-Platform]]'
  - '[[Libertas-Practice]]'
entities: []
jurisdictions: []
people: []
tags:
  - instagram
  - rag
  - refrag
  - meta-ai
  - token-efficiency
  - vector-search
  - reinforcement-learning
created: '2026-04-12'
last_reviewed: '2026-04-12'
source: instagram
instagram_url: 'https://www.instagram.com/p/DV0_mycE1Sy/'
instagram_author: '@dailydoseofds_'
---
# Meta's REFRAG — 2-4x Less Tokens, 16x Larger Context Window for RAG

> Saved from Instagram — @dailydoseofds_, 2026-04-12

## Core Insight
_Meta AI researchers developed REFRAG, a new RAG approach that compresses and filters context at the vector level instead of dumping all retrieved chunks into the LLM. Results: 30.85x faster time-to-first-token, 16x larger context windows, 2-4x fewer decoder tokens, with no accuracy loss. Code not yet released._

## Key Points
- **Problem:** Classic RAG fetches similar chunks from vector DB and dumps them into LLM — most chunks contain irrelevant text, wasting tokens and compute
- **REFRAG solution** — 3 steps:
  1. **Chunk compression:** Each chunk → single compressed embedding (not hundreds of token embeddings)
  2. **Relevance policy:** Lightweight RL-trained policy evaluates compressed embeddings, keeps only relevant chunks
  3. **Selective expansion:** Only chosen chunks expanded back to full embeddings for LLM
- **Results:** 30.85x faster TTFT (3.75x better than previous SOTA), 16x larger context, outperforms LLaMA on 16 benchmarks, 2-4x fewer tokens, no accuracy loss
- Code not yet released by Meta but intended
- Side-by-side diagram comparing RAG vs REFRAG pipelines shown
- 1.2K likes, 9 comments

## Relevance to Active Work
_Highly relevant to [[Qanun-Platform]] (legal document RAG), [[Libertas-Practice]] (case law retrieval), and any other project using RAG. The REFRAG approach could dramatically reduce costs and improve response times for document-heavy applications._

## Action Items
- [ ] Monitor Meta's release of REFRAG code
- [ ] Evaluate REFRAG's applicability to Qanun Platform's legal document retrieval
- [ ] Compare REFRAG with LightRAG (from earlier saved post) for Oliver's use cases

## Source Content
**Author:** @dailydoseofds_
**Caption:** _Researchers from Meta built a new RAG approach (with 2-4x less token usage + 16x larger context window)..._
**URL:** [View on Instagram](https://www.instagram.com/p/DV0_mycE1Sy/)

## Visual Notes
_Infographic comparing RAG vs REFRAG pipeline architectures side by side. RAG shows direct query→embed→vector DB→LLM flow. REFRAG shows additional compression, RL relevance policy, and selective expansion steps. Posted 13 March._
