# RelayCart Documentation: product scope

## Status

Design baseline approved. Implementation has not started; no functioning features, pipelines, releases or deployments are claimed.

## Purpose

A public documentation portal assembled from versioned documentation owned by each product.

## Planned stack

VitePress and TypeScript

## Engineering contract

- This repository owns its source, checks, documentation and releases.
- Public interfaces are versioned and tested.
- The development harness is optional tooling, not a runtime dependency.
- Examples and demonstration data are synthetic.
- Architecture decisions and exact local commands will be documented
  as their implementation checkpoints pass.

## Approved design baseline

- VitePress publishes system architecture, ADRs, threat/trust boundaries, runbooks, demonstrations and engineering evidence.
- Aggregate pinned component-owned documentation bundles; label planned, implemented, stable and deployed states separately.
- Publish honest free-tier/cost/portability limitations, secrets inventory names only, and build/security/evaluation evidence without confidential data.
- Keep sample/documentation accessible independently of sleeping live services; communicate publicly after dogfooding and launch readiness.

## Required engineering evidence

Each component has applicable automated checks: unit, integration, functional/contract and security tests; dependency/container/IaC scanning and secret detection where relevant. Main builds, deployments, scheduled regressions and availability observations are distinct. Build/candidate numbers increment automatically; stable semantic versions are calculated from reviewed changes and promoted through the release-readiness gate. Retain immutable artifacts, sanitized evidence and compatible rollback instructions. These are requirements, not implementation claims.

Use the portable harness during development once its core is usable; record any bypasses and feedback. The application does not import the harness at runtime.

## Design references

- [Harness release scope](https://github.com/aenns/portable-ai-harness/blob/96cc799/docs/release-scope.md)
- [Harness architecture](https://github.com/aenns/portable-ai-harness/blob/40476cf/docs/architecture.md)
- [Harness configuration and commands](https://github.com/aenns/portable-ai-harness/blob/99d47a1/docs/configuration-and-commands.md)
- [RelayCart system architecture, revision 4](https://github.com/aenns/relaycart-docs/blob/f5cf12d/docs/architecture/system.md)
