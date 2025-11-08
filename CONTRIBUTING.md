# Contributing to RegistryAccord (RA)

Thank you for your interest in contributing to RegistryAccord! This document explains how to propose changes, file issues, submit code and documentation, and participate in the specs, SDKs, reference services, and conformance program. All RA repositories should link to this file and add only repo‑specific details.

## Table of Contents

- Code of Conduct
- Scope of this Repository
- Ways to Contribute
- Before You Start (Issues vs RFCs)
- Development Workflow
- Commit, Branch, and PR Guidelines
- Testing and Conformance
- Versioning and Deprecations
- Security Policy
- Licensing and Contributor Terms
- Getting Help

## Code of Conduct

Participation in this project is governed by the community Code of Conduct. Be respectful, inclusive, and constructive in all interactions.

## Scope of this Repository

This repo contains the canonical protocol specifications and schemas (e.g., OpenAPI 3.1, JSON/JSON‑LD), examples, error envelopes, version headers, and conformance artifacts that define how RegistryAccord interoperates.

## Ways to Contribute

- Specifications and Schemas: author or refine OpenAPI/JSON artifacts; add examples and validation rules.
- Reference Implementations: improve services (Identity, Content Registry, Storage, Payments, Feeds, Revenue, Analytics).
- SDKs: enhance TypeScript/JS, Python, and Go clients; add typing, retries, pagination, idempotency, and consistent errors.
- Conformance: expand test scenarios, fixtures, and compatibility checks; improve reporting.
- Documentation: architecture, quickstarts, runbooks, diagrams, and migration guides.
- Tooling/Infra: docker‑compose, Helm/Terraform templates, CI workflows, code generators.

## Before You Start (Issues vs RFCs)

- Use an Issue for:
  - Bug reports with minimal reproductions and logs.
  - Small enhancements or documentation fixes.
  - Questions about behavior or examples.

- Use an RFC for:
  - New resources, fields, or events.
  - Semantic changes to existing APIs/schemas.
  - Deprecations and migrations.
  - Cross‑service features and security/privacy changes.

RFCs should include:
- Motivation and goals
- API/Schema diffs (OpenAPI, JSON/JSON‑LD) with examples
- Error semantics and versioning impact
- Security, privacy, and compliance considerations
- Migration and deprecation plan
- Conformance/test updates
- Rollout plan and timelines

## Development Workflow

1. Fork and create a feature branch: `feat/<slug>` or `fix/<slug>`.
2. Make changes with accompanying spec updates and examples.
3. Add or update tests (unit, contract, conformance).
4. Run linters and formatters locally; ensure CI passes.
5. Open a Pull Request referencing the Issue/RFC and describe the change, risks, and migration notes.
6. Respond to review feedback; keep PRs focused and incremental.

## Developer Certificate of Origin (DCO)

All contributions must be signed with the Developer Certificate of Origin (DCO). This is a legal attestation that you are the author of the work.

You do this by adding a `-s` flag to your `git commit` command:

**`git commit -s -m "Your commit message"`**

This will add a line to your commit message that looks like:
`Signed-off-by: Your Name <your-email@example.com>`

Pull Requests without a DCO sign-off on *every commit* will be rejected.

## Commit, Branch, and PR Guidelines

- Branch names: `feat/<short>`, `fix/<short>`, `docs/<short>`, `chore/<short>`.
- Commit style: Conventional Commits recommended, e.g.,
  - `feat(registry): add lineage query filter`
  - `fix(identity): correct token expiry check`
  - `docs(quickstart): clarify storage checksums`
- PR checklist:
  - Linked Issue or RFC
  - Updated OpenAPI/JSON artifacts and examples
  - Tests added/updated
  - Docs and migration notes (if applicable)
  - Lint/format and CI green
  - Backward‑compatibility reviewed

## Testing and Conformance

- Unit tests: service logic and schema validation.
- Contract tests: request/response parity with OpenAPI/JSON examples.
- Conformance: run the public harness against your changes; update fixtures as required.
- CI: PRs must pass all required checks before merge.

## Versioning and Deprecations

- Explicit versions (e.g., REST v1) and version headers.
- Additive‑first evolution; avoid breaking changes.
- Deprecations require:
  - Announced timelines and target removal version
  - Migration steps and examples
  - Conformance updates that cover legacy and new behavior during the window

## Security Policy

- Do not disclose vulnerabilities publicly.
- Report security issues privately to the project security contact listed in the repository SECURITY policy (or email the project team).
- Include details to reproduce the issue and assess impact.

## Licensing and Contributor Terms

- License: Apache‑2.0 for this repository; contributions are accepted under the same license.
- Attribution: preserve LICENSE and NOTICE files and attributions where present.
- Contributor terms: DCO (Signed‑off‑by) or CLA (if required) as specified by the repository. Ensure you have the right to contribute any code/content you submit.

## Getting Help

- For contribution questions, open a discussion or issue.
- For roadmap and governance queries, refer to the governance docs or contact the maintainers.
- For coordination or mentorship, reach out to the maintainers or the community email.

Thank you for helping build an open, interoperable content ecosystem with RegistryAccord!