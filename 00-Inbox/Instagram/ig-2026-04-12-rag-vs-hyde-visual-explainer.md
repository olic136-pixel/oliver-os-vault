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
  - hyde
  - hypothetical-document-embedding
  - vector-search
  - retrieval
  - contriever
created: '2026-04-12'
last_reviewed: '2026-04-12'
source: instagram
instagram_url: 'https://www.instagram.com/p/DVgZQqhDnk1/'
instagram_author: '@dailydoseofds_'
---
# RAG vs HyDE — Hypothetical Document Embedding Explained

> Saved from Instagram — @dailydoseofds_, 2026-04-12

## Core Insight
_A visual explainer comparing standard RAG with HyDE (Hypothetical Document Embedding). HyDE solves the fundamental RAG problem that questions are not semantically similar to their answers — by first generating a hypothetical answer, then embedding that answer for retrieval instead of the question._

## Key Points
- **Core RAG problem:** Questions aren't semantically similar to answers — "What is ML?" matches "What is AI?" more than "Machine learning is fun"
- **HyDE solution** — 4 steps:
  1. Use LLM to generate a hypothetical answer (H) for query (Q) — doesn't need to be correct
  2. Embed the answer using a contriever model to get embedding E
  3. Use E to query vector DB and retrieve relevant context (C)
  4. Pass H + C + Q to LLM for final answer
- The contriever model acts as a near-lossless compressor that filters out hallucinated details
- Produces vectors more similar to actual documents than the question would be
- Trade-off: improved retrieval but increased latency and more LLM usage
- Side-by-side diagram: RAG (Query→Embed→VectorDB→LLM) vs HyDE (Query→LLM→Hypothetical Response→Embed→VectorDB→LLM)
- 1.4K likes, 9 comments
- Comment from @dalerka99: "Actually, HyDE is part of agentic RAG" (10 likes)

## Relevance to Active Work
_Relevant to [[Qanun-Platform]] and [[Libertas-Practice]] for legal document retrieval. HyDE could improve retrieval quality for legal queries where the question format differs greatly from the answer format (e.g., "Is this clause enforceable?" vs actual contract language). Should be evaluated alongside REFRAG._

## Action Items
- [ ] Evaluate HyDE for Qanun Platform's legal query retrieval
- [ ] Compare HyDE + REFRAG as complementary approaches
- [ ] Test whether the latency trade-off is acceptable for legal research use cases

## Source Content
**Author:** @dailydoseofds_
**Caption:** _RAG vs. HyDE, visually explained! RAG is great, but it has a major problem: Questions are not semantically similar to their answers._
**URL:** [View on Instagram](https://www.instagram.com/p/DVgZQqhDnk1/)

## Visual Notes
_Infographic showing RAG vs HyDE architectures side by side. RAG: Query→Embedding→Vectors→VectorDB→Context→LLM→Response. HyDE: Query→LLM→Hypothetical Response→Embedding→Vectors→VectorDB→Context→LLM→Response. Posted 5 March._
