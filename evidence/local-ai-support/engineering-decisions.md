# Engineering Decisions

## ADR-001 — Prefer local model execution

**Decision:** Design the platform so the language model and embeddings can run inside infrastructure controlled by the organization.

**Rationale:** Confidential technical material should not require transmission to a public AI API. Local execution also permits offline operation and direct control over model versions.

**Trade-offs:** GPU and memory requirements, model lifecycle management, and lower convenience than fully managed cloud services.

## ADR-002 — Use Retrieval-Augmented Generation

**Decision:** Treat internal documents as retrieved context rather than attempting to encode organizational knowledge only through model training.

**Rationale:** Documents can be updated independently, retrieved passages can be cited, and the knowledge source remains inspectable.

**Trade-offs:** Retrieval quality, chunking and metadata become critical. A strong model cannot compensate for a weak index.

## ADR-003 — Keep components replaceable

**Decision:** Separate ingestion, embeddings, vector storage, retrieval, generation and user access behind clear interfaces.

**Rationale:** Models and vector databases evolve quickly. The architecture should permit component replacement without redesigning the entire platform.

**Trade-offs:** More interfaces, configuration and integration testing than a single bundled application.

## ADR-004 — Require source-aware answers

**Decision:** User-facing answers should include references to retrieved source material where the interface permits it.

**Rationale:** Technical users need to inspect the authoritative procedure, not only trust generated prose.

**Trade-offs:** Citation formatting and source navigation require metadata discipline.

## ADR-005 — Treat ingestion as an operational process

**Decision:** Index creation, updates and rebuilds must be repeatable and observable.

**Rationale:** A knowledge assistant becomes unreliable when its index silently diverges from the source repository.

**Trade-offs:** Requires scheduling, error reporting, document version handling and backup planning.

## ADR-006 — Avoid premature technology lock-in

**Decision:** Public evidence remains vendor-neutral until exact deployed components are verified and approved for disclosure.

**Rationale:** The portfolio should document engineering reasoning without inventing or leaking customer-specific details.
