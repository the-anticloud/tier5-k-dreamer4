# Ledger Status

**Project:** `K_DREAMER4`  
**Tier:** TIER_5_WORLD_NEURO_EMBODIED  
**Identity:** Upstream `danijar/dreamerv3` @ `e3f02248693a` (MIT)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `danijar/dreamerv3` |
| Commit | `e3f02248693a79dc8b0ebd62c93683888ddaccfe` |
| Upstream licence | MIT |
| Licence class | permissive |
| Clone size | 6.35 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
