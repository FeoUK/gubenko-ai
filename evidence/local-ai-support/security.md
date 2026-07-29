# Security

## Security objective

Keep confidential technical knowledge under organizational control while providing useful AI-assisted retrieval.

## Primary controls

### Data locality

Source documents, embeddings, prompts and generated answers should remain within the approved infrastructure boundary unless an explicitly reviewed integration requires otherwise.

### Access control

Authentication should be enforced before access to the assistant. Where document sensitivity differs, retrieval must apply authorization-aware metadata filters rather than relying only on the user interface.

### Transport security

External user access should be terminated through TLS. Internal service exposure should be minimized and restricted to required network paths.

### Secret management

Passwords, API tokens, private keys and model-repository credentials must not be committed to Git. They should be injected through protected environment files, secret stores or platform-native mechanisms.

### Logging and privacy

Logs should support diagnosis without recording unnecessary confidential text. Query logging, retention and access must follow organizational policy.

### Document governance

The AI platform does not replace source ownership. Approved source repositories remain authoritative, and ingestion should record document identity, version and processing status.

## Threat considerations

- unauthorized retrieval of restricted documents;
- prompt injection embedded in documents;
- data exfiltration through optional external integrations;
- stale documents producing unsafe instructions;
- model output presented without adequate source support;
- exposed administrative endpoints;
- leaked secrets in configuration or screenshots;
- excessive retention of user queries.

## Mitigation direction

- allowlisted document sources and formats;
- content sanitization and ingestion validation;
- retrieval filters based on user context;
- network egress restrictions for local-only deployments;
- source citations and explicit insufficient-evidence responses;
- protected administrative interfaces;
- regular dependency and image updates;
- redaction review before publishing evidence.

## Evidence still required

Security controls remain design claims until supported by sanitized configuration, network diagrams, access-control tests or audit records.
