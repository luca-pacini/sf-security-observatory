# Architecture Overview

Salesforce Security Observatory is a Salesforce-native security observability concept. It is designed as a sandbox-first architecture showcase rather than a generic dashboard.

## Core pattern

```text
LWC dashboard
-> SecurityObservatoryController
-> SecurityScanService
-> scanner classes
-> SOQL / Tooling API / safe metadata queries
-> Security Observatory evidence objects
-> dashboard metrics, findings, assets and drill-downs
```

## Design principles

- Read-only first.
- No remediation in version 1.
- Sanitised evidence only.
- Least-privilege setup.
- Named Credentials for callouts.
- Apex controllers kept thin.
- Scanner logic isolated in dedicated classes.
- Dashboard metrics separated from detailed evidence.
- Large detail views use safe drill-down and pagination patterns.
- Historical comparison and drift analysis are treated as product features, not ad hoc reports.

## Main capability areas

The private implementation is structured around these capability groups:

- Identity and login posture.
- API and OAuth exposure.
- Connected app posture.
- Licence and entitlement posture.
- Permission risk and assignment source.
- External endpoint governance.
- Health Check and setup risk indicators.
- Certificate and Named Credential visibility.
- Sites and Experience Cloud baseline exposure.
- Historical scan comparison and drift.

## Evidence model

The evidence model is designed to store only what is useful and safe:

- Scans.
- Findings.
- Scan details.
- Assets.
- Metrics.
- Source org context.

Evidence must not contain secrets, token values, session IDs, certificate bodies, private keys, raw sensitive headers or raw sensitive evidence.

## Publication note

This public repository intentionally does not include implementation code yet. The private implementation must first pass sanitisation, dependency review, coverage validation and public-readiness checks.
