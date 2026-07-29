# Local AI Technical Support Platform

> Engineering Evidence Package

**Status:** Draft  
**Package maturity:** Architecture documented; artifact collection in progress  
**Public scope:** Sanitized, vendor-neutral and customer-neutral

## Purpose

This package documents the engineering rationale and evidence plan for a local Retrieval-Augmented Generation platform intended to help technical teams search internal documentation and obtain answers grounded in controlled knowledge sources.

It is not a claim that every optional component described here is already production-deployed. Implemented, proposed and pending-evidence items are explicitly separated.

## Package contents

- [Executive Summary](executive-summary.md)
- [Business Problem](business-problem.md)
- [Architecture](architecture.md)
- [Engineering Decisions](engineering-decisions.md)
- [Implementation](implementation.md)
- [Deployment](deployment.md)
- [Security](security.md)
- [Technology Map](technologies.md)
- [Evidence Index](evidence-index.md)
- [Lessons Learned](lessons-learned.md)
- [Roadmap](roadmap.md)

## Evidence directories

- `diagrams/` — architecture, data-flow and deployment diagrams.
- `screenshots/` — sanitized UI and administrative screenshots.
- `configs/` — sanitized configuration examples.
- `metrics/` — reproducible measurements and test methodology.
- `media/` — optional demo recordings and presentation assets.

Git does not preserve empty directories, so each evidence directory contains a short README describing what belongs there.

## Related portfolio material

- [Service Portfolio case study](../../service-portfolio/case-studies/local-ai-support.md)
- [Local AI Platform service](../../service-portfolio/services/local-ai-platform.md)
- [AI Infrastructure service](../../service-portfolio/services/ai-infrastructure.md)

## Review rule

Before this package is marked public-ready, every externally visible statement must be classified as one of:

- **Verified** — supported by an included or linked artifact;
- **Documented** — supported by design and implementation records but not publicly reproduced;
- **Planned** — not yet implemented or not yet verified;
- **Redacted** — verified internally but omitted for confidentiality.
