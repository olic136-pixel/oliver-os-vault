---
created: '2026-04-08'
last_reviewed: '2026-04-08'
type: system
---

# Active Matters

```dataview
TABLE defendant, offence, court, status, last_reviewed
FROM "08-Matters"
WHERE type = "matter" AND status = "active"
SORT last_reviewed DESC
```

## All matters

```dataview
TABLE defendant, offence, court, status
FROM "08-Matters"
WHERE type = "matter"
SORT status ASC, last_reviewed DESC
```
