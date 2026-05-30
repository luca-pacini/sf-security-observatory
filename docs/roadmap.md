# Roadmap

This roadmap is intentionally public-safe. It describes the portfolio direction without exposing private implementation details or real org evidence.

## Phase 1: Portfolio landing page

Status: in progress.

- Public README.
- Architecture overview.
- AI-assisted delivery model.
- Security boundaries.
- High-level roadmap.

## Phase 2: Private implementation hardening

Status: private.

- Complete repo inventory and reference checks.
- Validate cleanup candidates.
- Remove or move out-of-scope metadata only after reference checks, tests and dry-run deploy validation.
- Confirm project-owned Apex coverage target.
- Validate supported API version posture.
- Keep requirements tracker current.

## Phase 3: Sanitised implementation publication review

Status: not started.

- Review all Apex, LWC and metadata for public suitability.
- Remove org-specific values, names, URLs and environment references.
- Replace real examples with fake sample data.
- Confirm no secrets, auth artefacts or sensitive evidence exist.
- Add public-safe screenshots only if they use synthetic data.

## Phase 4: Public reference implementation

Status: deferred.

- Publish selected sanitised Apex and LWC patterns.
- Publish setup guidance.
- Publish validation commands.
- Consider package structure only after MVP stabilises.

## Explicitly not in public scope yet

- Real org data.
- Named Credential values.
- Real scan output.
- Production screenshots.
- Installable package.
- Automated remediation.
