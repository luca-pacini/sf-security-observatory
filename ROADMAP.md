# Salesforce Security Observatory Roadmap

Status: public roadmap
v1 status: in active development
Last reviewed: 2026-06-22

Salesforce Security Observatory is a read-only Salesforce security evidence tool.

It helps Salesforce teams review security posture by collecting sanitised scan evidence, showing compound risk, identifying native-control blind spots, comparing retained scans over time, and aligning evidence to the Security Benchmark for Salesforce. SBS alignment is a P0 v1 foundation, not a certification or formal compliance claim.

This project is an independent reference implementation. It is not affiliated with Salesforce or the Security Benchmark for Salesforce project.

## At a glance

```mermaid
flowchart LR
  v1["v1 now<br/>Explainability foundation<br/>SBS P0 foundation<br/>Retention discipline"]
  v11["v1.1<br/>SBS lifecycle hardening<br/>Native capability expansion<br/>Additional posture polish"]
  v12["v1.2<br/>Additional scanners<br/>Deeper posture coverage"]
  v2["v2<br/>Governance<br/>Attestation and accepted risk<br/>Entitlement comparison"]
  v1 --> v11 --> v12 --> v2
```

## What Observatory adds

A feature stays in scope only if it adds at least one of the following:

| Value | Meaning |
|---|---|
| Explainable evidence | Shows source, coverage status, posture, verification path, limitation and Observatory value-add. |
| Benchmark alignment | Maps observed and partial evidence to Security Benchmark for Salesforce controls where implementation is validated. |
| Compound-risk correlation | Combines signals across users, permissions, OAuth, API access, sessions, endpoints, certificates, and licences. |
| Native blind-spot visibility | Shows when a Salesforce-native capability is unavailable, disabled, not configured, or outside the current scan scope. |
| Drift and comparison | Shows what changed between retained scans. |

Where Salesforce already provides the core native capability, Observatory links to it or summarises it instead of duplicating it.

## v1 now

v1 focuses on trustworthy, explainable, short-term operational evidence with SBS alignment as a P0 delivery item.

| Area | Scope |
|---|---|
| Dashboard clarity | Clear dashboard cards with source, coverage status, posture, safe verification help, limitation and Observatory value-add where implemented. |
| SBS P0 foundation | Local SBS metadata, controlled admin upload, static scanner-to-SBS mappings, SBS version display and the coverage map are v1 P0 work. No v1 claim should mark them complete until implemented and validated. |
| Coverage map | Target v1 coverage view: Automated, Partial Evidence, Manual Required, Not Covered and Extended Check. |
| Failure visibility | Scanner failures show as Unknown/Error, never as a false Pass. |
| Retention discipline | Salesforce retains only the latest 3 completed scans once the v1 retention default correction is applied. |
| Safe export | CSV export is available for retained evidence and is protected against formula injection. |
| Scan comparison | Completed scans can be compared using retained evidence, with SBS-aware labels and incomplete/version-mismatch caveats where supported. |
| Native blind spots | Cards show when a native Salesforce capability is unavailable, disabled, not configured, or outside the current scan scope. |
| No remediation | Observatory reports posture only. It does not change security settings. |

## v1 exclusions

v1 does not include:

| Exclusion | Decision |
|---|---|
| Automatic remediation | No token revocation, API blocking, permission removal, endpoint change, certificate change, or key rotation. |
| AI summaries | No AI or Gemini advisory summaries. |
| Event Monitoring ingestion | No high-volume event-log ingestion. |
| Security Center clone | No attempt to replace Salesforce-native security products. |
| External warehouse sync | Long-term evidence storage is customer-owned and outside the app. |
| Scheduled scans | v1 is manual. |
| Formal SBS compliance claim | v1 provides SBS-aligned evidence and coverage visibility only where implemented. It does not provide certification or compliance scoring. |

## v1.1 next

v1.1 focuses on hardening the SBS lifecycle and expanding native capability coverage after the v1 SBS foundation is stable.

| Area | Direction |
|---|---|
| SBS lifecycle hardening | Improve upload history, version history, rollback posture and registry administration after the v1 registry is stable. |
| Advanced SBS reconciliation | Show deeper control changes between SBS versions after the v1 version display and caveat foundation is stable. |
| Native capability register | Expand Setup paths, licence dependencies, posture, limitations, and Observatory action per card. |
| Connected App and External Client App posture | Improve visibility where metadata access is safe and reliable. |
| API Access Control posture | Detect and explain posture where feasible without remediation. |
| Storage estimate improvement | Improve retained evidence footprint estimates. |
| Source-org awareness | Harden scan and comparison labels for future multi-org support. |

## v1.2 later

v1.2 may add more scanner coverage after v1 and v1.1 stability work is complete.

| Area | Direction |
|---|---|
| Public Content links | Optional scanner for public file or link exposure. |
| Field History Tracking | Optional scanner for configured sensitive-field lists. |
| Sites and Experience depth | Expand baseline exposure checks where safe. |
| Transaction Security | Inventory only, no blocking or remediation. |
| Permission source depth | Improve Profile, Permission Set, and Permission Set Group risk visibility. |
| Licence alignment | Improve over-licensed, missing-access, and unexpected-access views. |
| Historical baselines | Add daily, weekly, and monthly labels if storage-safe. |

## v2 future

v2 focuses on governance evidence and review workflows.

| Area | Direction |
|---|---|
| Manual attestation | Capture governance evidence for controls that cannot be scanned. |
| N/A justification | Explain controls that do not apply. |
| Accepted risk | Track owner, expiry, justification, and review status. |
| Functional role entitlement comparison | Compare expected access against actual access by role. |
| Historical drift reporting | Report repeated, worsened, improved, and resolved posture over time. |
| External reporting model | Provide replication-ready reporting objects or views. |
| Framework export | Export SBS-aligned evidence for wider governance reporting. |

## Synthetic data only

Everything shown in this project's public materials — examples, screenshots, and sample exports — comes from a development org using synthetic data, never customer data, org secrets, credentials, tokens, or real scan evidence.

## Maintainer

Maintained by SecuredForce Lab.

Contact: securedforcelab@gmail.com
LinkedIn: linkedin.com/in/lpacini

Security Benchmark for Salesforce (SBS) control references are used under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). SBS is an independent project of the Salesforce-Security-Benchmark community — see [securitybenchmark.org](https://www.securitybenchmark.org).
