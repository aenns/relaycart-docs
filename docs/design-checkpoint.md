# Step 03 — Approved design checkpoint

Review date: 7 October 2026

Status: design review complete; publication is established by the merged checkpoint PRs. Implementation has not started.

## Recorded decisions and source precedence

The approved scope and component/system design documents below govern implementation. Older build-guide suggestions that conflict with approved direct-model writes, candidate-first dogfooding or launch timing are superseded. Examples and CLI contracts are design fixtures until implemented and tested.

- [Harness release scope](https://github.com/aenns/portable-ai-harness/blob/96cc799/docs/release-scope.md)
- [Harness architecture](https://github.com/aenns/portable-ai-harness/blob/40476cf/docs/architecture.md)
- [Harness configuration and commands](https://github.com/aenns/portable-ai-harness/blob/99d47a1/docs/configuration-and-commands.md)
- [RelayCart system architecture, revision 4](https://github.com/aenns/relaycart-docs/blob/f5cf12d/docs/architecture/system.md)

## Consistency review

- The harness is a Python product supporting project-owned tasks across languages and infrastructure; it is not an application runtime dependency.
- RelayCart separates static web/docs, order API, inference and gateway; PostgreSQL owns transaction truth and MongoDB holds documents/projections.
- Independent repositories and artifact versions use pinned contracts and a compatible deployment manifest.
- Gateway security complements API authorization; secrets stay in their intended environment with documented rotation and protected state.
- RAG retrieves authorized evidence, returns references and handles insufficient evidence; deterministic CI and real-model evaluations are labelled separately.
- Main build automation, candidate/stable versioning, vulnerability scanning and functional/integration testing are required implementation work.
- Correlation is preserved across delayed work; aggregation is optional/protected and sampled availability results expose freshness and limitations.
- Free hosting remains selected. Sleeping services, quotas, cold starts and shared free-instance hours are explicitly documented; monitoring cannot imply an uptime guarantee.
- Portability must be demonstrated by deployment/restore/security exercises, with provider infrastructure and identity migration tradeoffs recorded.
- Candidate harness builds will be used during development and improved from feedback before stable/public launch.

## Domain and expenditure decision

Adrian confirmed purchasing adrianenns.com through Porkbun on 7 October 2026. DNS, HTTPS hosting and application custom domains are not configured yet. The domain is the only planned paid item; no paid hosting is authorized by this checkpoint. The paid deployment profile remains an optional future decision.

## Completion evidence and next work

Step 03A scope and Step 03B architecture/contracts were merged before this review. Step 03C corrects stale baseline records, records this review and marks reviewed designs approved. Completion requires all seven checkpoint PRs merged plus clean local main branches matching refreshed origin/main references; final verification output is the publication evidence.

Next implementation work starts with an installable minimal harness core and meaningful tests, then expands through the approved command/configuration contracts. Use it on itself and the other components as soon as usable. No running product, security test result, release, deployment or uptime measurement is claimed by this design checkpoint.
