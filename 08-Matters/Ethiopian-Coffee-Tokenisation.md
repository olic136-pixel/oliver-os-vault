---
created: '2026-04-12'
entities:
  - Human8
last_reviewed: '2026-04-12'
people:
  - Gabe
  - Ammar
projects:
  - Human8
source: whatsapp-enriched
status: concept
tags:
  - human8
  - tokenisation
  - coffee
  - blockchain
  - supply-chain
type: matter
---

# Ethiopian Coffee Tokenisation

**Type:** Supply chain tokenisation project
**Status:** Concept — architecture designed, no build
**Period:** October 2025
**Parties:** [[02-Entities/Human8]], Avastra (avastra.ch — Ethiopian coffee)

## Architecture (Oliver's design)

1. **Cooperative level:** Mobile verification app (offline-capable, GPS, camera). Reps check harvest, take geo-stamped photos.
2. **Oracle layer:** App → cooperative DB → oracle (handles offline sync). Posts verification data to smart contract.
3. **Warehouse level:** QR-marked bags scanned. Inspect, weigh, mark inspection via oracle. Record as deliverable, issue token.
4. **Token:** ERC-1155 or ERC-721. E.g. "1 kilo of 2026 harvest beans from Farm X (Grade A)."
5. **Settlement:** Tokens burnt on delivery request.
6. **Contract:** Yield Assignment Agreement (YAA) between farmer and token issuer.

## Regulatory Strategy
- **Phase 1:** Traceability only — less regulation, lower legal costs. Prove concept.
- **Phase 2 (future):** Trading — likely "financial instrument" classification → extensive regulatory roadmap.
- **SBT option:** Soulbound tokens as non-transferable futures replacement. Dodge regulation.
- **Decision:** Start traceability, keep trading idea between founders only.

## Gabe's IoT Enhancement
Sensors at checkpoints automating token creation. Conveyor belt scanning of 60-70kg bags. Higher investment, better margins.

## References
- DeSPoke.io — clothing supply chain blockchain verification
- chekkitapp.com — Gabe's cousin's company, similar solution without blockchain
- EUDR compliance — makes provenance advantageous for EU market

## Related
- [[01-Projects/Human8]]
- [[03-People/Gabe]]
- [[03-People/Ammar]]
