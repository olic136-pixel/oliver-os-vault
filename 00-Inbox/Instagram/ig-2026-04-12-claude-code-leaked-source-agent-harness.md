---
type: inbox
status: active
projects:
  - '[[Human8]]'
  - '[[Human8-Nodex]]'
  - '[[Qanun-Platform]]'
entities:
  - '[[Human8]]'
jurisdictions: []
people: []
tags:
  - instagram
  - claude-code
  - agent-harness
  - architecture
  - async-patterns
  - developer-tools
created: '2026-04-12'
last_reviewed: '2026-04-12'
source: instagram
instagram_url: 'https://www.instagram.com/p/DW07WLfjH42/'
instagram_author: '@aantoinelee'
---
# 4 Lessons from Claude Code's Leaked Source Code for Agent Harness Design

> Saved from Instagram — @aantoinelee, 2026-04-12

## Core Insight
_A breakdown of 4 key architectural patterns found in Claude Code's source code that inform best practices for building agent harnesses. Lesson #1 covers the Async Generator Core Loop pattern — the fundamental execution model. Notable comment from @articate clarifies that LLM context is resent fully each turn and that compaction can actually increase cost by invalidating cache._

## Key Points
- Lesson #1: Async Generator Core Loop — the core execution pattern is one async generator
- The video analyses Claude Code's actual source architecture
- Practical implications for anyone building their own agent harness
- Important comment from @articate: every turn resends full context to the LLM API; cache only covers what was seen in the last 5 minutes; compaction means paying for an LLM to shorten conversation but invalidates cache
- 708 likes, 10 comments, 8 reposts — technical audience

## Relevance to Active Work
_Directly relevant to [[Human8]] and any custom agent tooling Oliver is building. Understanding Claude Code's own architecture helps build better agent harnesses for [[Qlarifai-CRM]], [[Qanun-Platform]], or [[Human8-Nodex]]._

## Action Items
- [ ] Study the async generator core loop pattern for agent harness design
- [ ] Consider cache invalidation implications when implementing context compaction

## Source Content
**Author:** @aantoinelee
**Caption:** _4 lessons from Claude Code's leaked source code that will help you build the BEST agent harness_
**URL:** [View on Instagram](https://www.instagram.com/p/DW07WLfjH42/)

## Visual Notes
_Video shows presenter (young man with microphone, outdoors near Claude Code branding) with on-screen text "#1 Async Generator Core Loop" and subtitle "is one async generator". Posted 4 days ago._
