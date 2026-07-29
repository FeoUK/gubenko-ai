# Deployment

## Reference deployment boundary

The preferred deployment keeps the document corpus, vector index, model runtime, prompts and generated answers inside infrastructure controlled by the organization.

## Logical services

- reverse proxy and TLS termination;
- user-facing web application;
- application API;
- ingestion worker;
- embedding service;
- vector index;
- local model runtime;
- persistent storage;
- monitoring and log collection.

## Containerized option

A container-based deployment can provide repeatability and component isolation. A typical Compose or orchestrated deployment should define:

- explicit image versions;
- persistent volumes;
- internal service networks;
- health checks;
- CPU and memory limits;
- restart policies;
- environment-specific secrets supplied outside Git;
- controlled exposure through a reverse proxy.

## Deployment sequence

1. Prepare host storage and network boundaries.
2. Install the selected container and GPU runtime where required.
3. Provision secrets and TLS material.
4. Start storage, vector and model services.
5. Start the API and web interface.
6. Run health checks.
7. Ingest a controlled test corpus.
8. Execute representative retrieval tests.
9. Enable monitoring and backup jobs.

## Backup scope

Backups should cover configuration, ingestion manifests, source metadata and persistent indexes where rebuilding them is costly. The authoritative source documents should remain backed up by their owning system.

## Recovery principle

The index should be reproducible from approved source documents. Recovery documentation must distinguish data that must be restored from data that can be regenerated.

## Pending deployment evidence

- sanitized deployment diagram;
- example container configuration;
- health-check output;
- backup and restore test notes;
- resource-consumption measurements on named hardware.
