# Lessons Learned

## Knowledge quality dominates model size

A larger language model does not correct missing, contradictory or poorly maintained source material. Document ownership and curation are part of the system architecture.

## Retrieval must be evaluated independently

When an answer is weak, the failure may occur before generation. The retrieved passages, metadata filters and chunk boundaries should be inspected before changing the model.

## Citations improve technical trust

Engineering users need a path back to the authoritative document. A fluent answer without inspectable evidence is less useful in operational work.

## Local AI is an infrastructure product

Running a model is only one component. Storage, networking, TLS, authentication, monitoring, backups, updates and capacity planning determine whether the platform is maintainable.

## Re-indexing is a lifecycle requirement

An index is not a one-time build artifact. Document additions, corrections, removals and version changes require a controlled refresh process.

## Uncertainty is a feature

The platform should clearly report when retrieved evidence is insufficient. A technically honest non-answer is safer than plausible but unsupported instructions.

## Public evidence requires deliberate preparation

Real deployments often contain confidential documents, names, domains and network details. A publishable case needs synthetic examples or carefully sanitized artifacts rather than raw production screenshots.
