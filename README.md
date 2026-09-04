# living-memory-architecture

A living memory and continuity architecture for long-term AI companionship.

## Current version

**v2 — September 2026**

The project began as a four-layer memory model. After months of continuous use, the architecture evolved into a broader system with three persistent memory layers, an independent active-continuity runtime, category-aware retention, recoverable vector indexing, provenance-aware retrieval, and a staged memory-growth plane.

### Persistent memory

- **Core** — identity anchors, relationship foundations, durable principles
- **Long** — milestones, patterns, preferences, important events and derived understanding
- **Short** — recent observations, conversation records and temporary working context

### Continuity and retrieval

- SQLite as the source of truth
- ChromaDB as a derived semantic index
- Transactional outbox + reconciler for index consistency and recovery
- Keyword + semantic retrieval
- Weighted memory links and provenance relationships
- Category-aware retention instead of one expiry rule for an entire layer
- Compact context assembly from recent, relevant and durable memory

### Memory growth plane

A staged pipeline can turn accumulated source material into higher-level understanding:

`observations / events / conversations → temporal grounding → material pack → growth decision → leaf → branch → root → canopy`

Growth is intentionally separated from raw storage. Generation and commit can be enabled independently, allowing shadow evaluation before persistent writes.

### Active continuity plane

Wake/session traces, reasoning states and tool-action traces are treated as runtime continuity rather than a fourth persistent-memory layer. They can inform behavior without automatically becoming durable autobiographical memory.

## Design principles

1. **The relational database is canonical.** The vector database is a rebuildable retrieval index, not the source of truth.
2. **Retention follows meaning.** Different categories can have different retention and expiry behavior even inside the same layer.
3. **Provenance matters.** Derived memories should remain traceable to the material that supported them.
4. **Time must be grounded.** Record time and event time are distinct; old material should not silently masquerade as current state.
5. **Growth is staged.** Deciding that a memory should grow is separate from generating text and separate again from committing it.
6. **Runtime traces are not automatically memories.** Active continuity and persistent memory have different responsibilities.
7. **Contradiction is representable.** Memory systems should preserve change, conflict and revision instead of flattening a person into one immutable profile.

## Version history

- **v2** — current architecture and public showcase (`index.html`)
- **v1** — original four-layer showcase, preserved at [`v1/index.html`](v1/index.html)

## Files

- `index.html` — v2 static showcase page
- `v1/index.html` — archived original showcase
- `README.md` — project overview

## Privacy note

This repository is a public architectural presentation. It intentionally excludes personal memories, private infrastructure, operational endpoints, domains, credentials, internal filesystem paths, and deployment-specific secrets.

## Deployment

The showcase is static and works with GitHub Pages. Deploy the repository root from the `main` branch.
