# Technology Map

This document records technology roles without claiming a final vendor selection where public evidence is not yet available.

| Capability | Technology category | Selection criteria |
|---|---|---|
| Model execution | Local LLM runtime | Hardware compatibility, model support, quantization, observability, licensing |
| Embeddings | Embedding model/service | Retrieval quality, language coverage, model size, local execution |
| Vector search | Vector database or vector extension | Filtering, persistence, backup, scale, operational familiarity |
| Application API | Python service framework | Clear interfaces, validation, streaming support, ecosystem |
| User interface | Web application | Source display, usability, authentication integration |
| Document processing | Parsers and normalization tools | Supported formats, deterministic extraction, error reporting |
| Reverse proxy | Nginx, Apache or equivalent | TLS, access control, request limits, operational fit |
| Packaging | Containers | Reproducibility, isolation, version control |
| Host platform | Linux | Runtime support, automation, monitoring, security controls |
| Monitoring | Metrics, health checks and logs | Failure visibility, resource tracking, alerting |

## Selection policy

A component should be selected only after considering:

- compatibility with the target hardware;
- security and data-locality constraints;
- quality on the organization's languages and document types;
- operational complexity;
- backup and recovery requirements;
- upgrade path and vendor lock-in;
- reproducible testing against representative questions.

## Publication rule

Exact versions and product names should be added only when supported by a sanitized configuration, deployment record or repository reference that can be published safely.
