---
type: inbox
status: active
projects:
  - '[[TradeDar]]'
entities:
  - '[[TradeDar]]'
jurisdictions: []
people: []
tags:
  - instagram
  - machine-learning
  - quantitative-finance
  - asset-pricing
  - neural-networks
  - academic-paper
  - algorithmic-trading
created: '2026-04-12'
last_reviewed: '2026-04-12'
source: instagram
instagram_url: 'https://www.instagram.com/p/DXAD2Y9DDhM/'
instagram_author: '@vince.quant'
---
# Can Machine Learning Predict Stock Returns? — Gu, Kelly, Xiu (2020)

> Saved from Instagram — @vince.quant, 2026-04-12

## Core Insight
_A detailed breakdown of the seminal Gu, Kelly, and Xiu (2020) paper from the Review of Financial Studies on using machine learning for empirical asset pricing. The answer is yes — ML can predict stock returns — but strictly as a forecasting tool, not a causal explanation. Trees and shallow neural networks (3 hidden layers) outperform deeper architectures._

## Key Points
- **Paper:** Gu, Kelly, Xiu (2020) "Empirical Asset Pricing via Machine Learning" — Review of Financial Studies, 33(5), 2223–2273
- **Dataset:** Full universe of U.S. listed stocks from 1957 to 2016
- **Features:** 94 firm characteristics, 8 macro variables, 74 industry dummies → over 900 baseline signals
- **Best models:** Trees and shallow neural networks; performance peaks at ~3 hidden layers, not deeper
- **Key limitation:** These are predictive measurements, not economic mechanisms — signal is weak and noisy at stock level, clearer when aggregated into portfolios
- **All evaluation:** Strictly out-of-sample
- Notable comment from @macro_quant_rick questioning the choice of price as a label and the cross-validation method
- Comment from @jubor warns that models learn regime-specific randomness
- 657 likes, 12 comments, 10 reposts — high engagement for quant content

## Relevance to Active Work
_Highly relevant to [[TradeDar]] — this is a foundational paper for ML-based trading systems. The finding that shallow networks beat deep ones is an important architectural decision for any ML trading features. The emphasis on out-of-sample evaluation and portfolio-level aggregation are key design principles._

## Action Items
- [ ] Read the full paper: doi.org/10.1093/rfs/hhaa009
- [ ] Consider implementing shallow neural network models in TradeDar's ML pipeline
- [ ] Note the 94 firm characteristics as a feature engineering reference
- [ ] Apply out-of-sample evaluation discipline to any TradeDar ML models

## Source Content
**Author:** @vince.quant
**Caption:** _Can machine learning predict stock returns? In Gu, Kelly, and Xiu's 2020 Review of Financial Studies paper, the answer is yes, but strictly as a forecasting tool..._
**URL:** [View on Instagram](https://www.instagram.com/p/DXAD2Y9DDhM/)

## Visual Notes
_Video displays the paper title "GU, KELLY, XIU (2020) — Review of Financial Studies — 94 firm characteristics" as on-screen text, followed by subtitle "THEY BUILD A". Clean, academic presentation style. 657 likes, posted 12 hours ago._
