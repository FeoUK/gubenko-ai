# Evidence Index

This index tracks the artifacts required to move the case from a documented architecture to an evidence-backed public case study.

## Status legend

- `available` — included or linked and reviewed;
- `internal` — exists but is not yet sanitized for publication;
- `pending` — must still be collected or produced;
- `not applicable` — intentionally excluded.

## Architecture evidence

| Artifact | Status | Publication requirement |
|---|---|---|
| High-level component diagram | pending | Remove customer identifiers and internal addresses |
| Data-flow diagram | pending | Show document, embedding, retrieval and generation paths |
| Deployment diagram | pending | Generalize hosts, networks and storage |
| Trust-boundary diagram | pending | Identify local and optional external dependencies |

## Implementation evidence

| Artifact | Status | Publication requirement |
|---|---|---|
| Sanitized ingestion workflow | pending | Use non-confidential example documents |
| Retrieval request/response example | pending | Remove source-sensitive text |
| Source-citation example | pending | Use an approved public or synthetic corpus |
| Error-handling example | pending | Demonstrate insufficient-context behavior |

## Configuration evidence

| Artifact | Status | Publication requirement |
|---|---|---|
| Container configuration fragment | pending | Remove secrets, domains, addresses and private image names |
| Reverse-proxy fragment | pending | Replace real endpoints and certificates |
| Environment template | pending | Include variable names only; no values |
| Health-check definition | pending | Generalize service names where necessary |

## Operational evidence

| Artifact | Status | Publication requirement |
|---|---|---|
| Service health screenshot | pending | Redact host and user information |
| Resource metrics | pending | Document hardware and test conditions |
| Indexing log excerpt | pending | Remove filenames and sensitive document text |
| Backup/restore test | pending | Record procedure and outcome |

## Quality evidence

| Artifact | Status | Publication requirement |
|---|---|---|
| Representative question set | pending | Use synthetic or approved questions |
| Retrieval relevance review | pending | Define scoring method before publishing results |
| Unsupported-question test | pending | Verify refusal or uncertainty behavior |
| Version-conflict test | pending | Document expected treatment of stale material |

## Ownership evidence

| Artifact | Status | Publication requirement |
|---|---|---|
| Architecture decision records | available | This package contains initial ADRs |
| Personal contribution statement | available | Documented in the package summary and portfolio case |
| Commit or PR references | pending | Link only to repositories safe for disclosure |
| Deployment notes | pending | Sanitize operational details |

## Next evidence collection order

1. Create diagrams from the documented architecture.
2. Prepare a synthetic, publishable document corpus.
3. Capture an end-to-end query with source citations.
4. Publish sanitized deployment and health-check fragments.
5. Measure retrieval and response behavior under documented test conditions.
