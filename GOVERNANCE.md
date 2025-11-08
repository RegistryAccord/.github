# RegistryAccord Governance

This document defines how the RegistryAccord (RA) project is governed. It applies to all RA protocol repositories, specifications, SDKs, reference services, and the conformance program. All participating repositories should link to this file rather than duplicating it.

## Principles

- Neutral and protocol‑first: all interoperability‑affecting changes happen in the open via public processes.
- Open participation: any contributor may propose changes through issues and RFCs.
- Transparency: decisions, rationales, and timelines are documented and publicly accessible.
- Stability: additive evolution is preferred; breaking changes require migration windows and fixtures.

## Roles and Responsibilities

### Contributors
- Submit issues, RFCs, code, tests, and documentation.
- Follow the Code of Conduct and contribution guidelines.
- Engage constructively during reviews and discussions.

### Maintainers
- Review and merge contributions in one or more repositories.
- Safeguard specification quality and compatibility.
- Manage releases, labels, and issue triage.
- Escalate contentious or breaking changes to the TSC.

### Technical Steering Committee (TSC)
- Charter and steward the project's technical direction and roadmap priorities.
- Resolve disputes that cannot be settled at the maintainer level.
- Approve breaking changes, deprecations, and governance amendments.
- Periodically review maintainer and TSC membership.

### Working Groups (optional)
- Time‑bounded or ongoing groups focused on specific areas (e.g., Identity, Content, Storage, Payments, Feeds, Revenue, Analytics, Conformance).
- Propose designs and implementation plans within their scope.
- Report progress and recommendations to maintainers and the TSC.

## Decision‑Making

### Trivial Changes
- Documentation fixes, non‑functional refactors, and clearly scoped bug fixes are approved via standard PR review by maintainers.

### Non‑Trivial Changes
- Require an RFC. The RFC must include:
  - Motivation and goals
  - API/Schema diffs (OpenAPI 3.1, JSON Schema Draft 2020-12)
  - Semantics and error handling (RFC 7807)
  - Security, privacy, and compliance considerations
  - Migration and deprecation impact
  - Conformance and test updates
  - Rollout and versioning plan (date-based versioning)

### Controversial or Breaking Changes
- Public discussion is required; TSC approval is mandatory.
- Must include timelines, migration guidance, fixtures, and deprecation headers (RFC 8594).

### Lazy Consensus
- If no substantial objections are raised within a reasonable review window, changes may proceed with maintainer approval.

## RFC Workflow

1. Open an issue describing the problem and scope.
2. Draft an RFC with required artifacts (APIs/schemas, examples, tests).
3. Request reviews from relevant maintainers/working groups.
4. Iterate until accepted or rejected with rationale.
5. Track implementation via linked issues/PRs.
6. Update conformance tests alongside implementation.

## Versioning and Deprecations

- Date-based versioning for APIs (e.g., `2025-11-01`) as specified in RA-API-Version header.
- Additive‑first policy: add before changing; avoid removal when possible.
- Deprecations include:
  - Clear timelines and target removal versions
  - Migration steps and example payloads
  - Conformance fixtures that assert both legacy and new behaviors during the window
  - Deprecation headers per RFC 8594

## Releases

- Each repo designates release owners who manage freezes, tags, artifacts, and notes.
- Required checks: linting, unit tests, contract tests, and (where applicable) conformance suites must pass.
- Release notes include upgrade impact, migration guides, and security considerations.

## Conformance and Compatibility

- A public conformance harness validates behavior and wire contracts against the specs.
- Implementations that pass receive versioned compatibility badges.
- Conformance evolves with specs; badges reflect supported protocol versions.

## Security and Code of Conduct

- Responsible disclosure: report security issues privately via the published security contact; do not file public issues.
- The Code of Conduct applies across all repos and community spaces.
- Violations may lead to moderation actions by maintainers or the TSC.

## Membership

### Becoming a Maintainer
- Earned via sustained, high‑quality contributions (code, specs, reviews, docs, community support).
- Nominated by an existing maintainer and confirmed by the TSC.

### Stepping Down or Removal
- Maintainers may step down voluntarily at any time.
- Inactive maintainers may be rotated to emeritus status after review.
- The TSC may remove maintainers for repeated violations of policy or failure to fulfill responsibilities.

### TSC Composition
- Selected from active maintainers with a track record in project stewardship.
- Membership is reviewed periodically to ensure diversity of expertise and perspective.
- Conflicts of interest must be disclosed.

## Conflict Resolution

- Start with respectful discussion in issues or RFCs.
- Escalate to maintainers of affected repositories.
- If unresolved, the TSC mediates and issues a final decision with rationale.

## Amendments

- Governance changes follow the RFC process and require TSC approval.
- Amendments are documented with versioned history and rationale.

## Repository Notes (Template)

Each repo may append:
- Release owners and rotation schedule
- CI status checks and required gates
- Supported versions and deprecation windows
- Contacts and working group affiliations

## Contact

- General governance questions: info@registryaccord.com
- Security reports: use the private security contact listed in the SECURITY policy for the affected repository