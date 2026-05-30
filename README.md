# Salesforce Security Observatory

A sandbox-first Salesforce security architecture showcase.

This public repository is a sanitised portfolio landing page for a private Salesforce implementation. It explains the product concept, architecture, security boundaries and delivery approach without publishing implementation code, org-specific metadata or sensitive evidence.

## Purpose

Salesforce Security Observatory is designed to show how a Salesforce-native security observability product can be built using:

- Lightning Web Components for a security posture dashboard.
- Apex orchestration and scanner services.
- Safe SOQL and Tooling API reads.
- Sanitised evidence capture.
- Read-only scanning.
- Licence, entitlement, identity, API and endpoint exposure visibility.
- Historical comparison and drift analysis.

This is not a remediation tool. It does not revoke access, block APIs, remove permissions or change endpoints.

## Architecture

```text
LWC dashboard
-> SecurityObservatoryController
-> SecurityScanService
-> scanner classes
-> SOQL / Tooling API / safe metadata queries
-> Security_Scan__c, Security_Finding__c, Security_Scan_Detail__c, Security_Asset__c, metrics and dashboard DTOs
```

The implementation is intentionally Salesforce-native. The design demonstrates separation of concerns between UI, controller, service orchestration, scanner logic, evidence storage and dashboard presentation.

## Current public status

This repository currently contains documentation only.

Implementation code remains private until the project has passed final sanitisation, dependency review, coverage validation and packaging/publication checks.

## Security boundaries

The project is designed around strict security boundaries:

- Read-only posture scanning.
- No production remediation actions.
- No token revocation.
- No API blocking.
- No automatic permission removal.
- No endpoint changes.
- No storage or display of access tokens, refresh tokens, session IDs, secrets, certificate bodies, private keys or raw sensitive evidence.
- Named Credentials for callouts.
- Least-privilege setup.
- Sanitised evidence only.
- Metrics without safe drill-downs are not clickable.

## AI-assisted delivery model

This project also demonstrates disciplined AI-assisted Salesforce delivery.

GPT, Claude and Codex-style tools are treated as project collaborators, not uncontrolled code generators. They are used with explicit requirements, narrow task scopes, source-of-truth documentation, validation commands and human review.

The AI operating model is documented here:

- [AI-assisted delivery model](docs/ai-assisted-delivery.md)

## Documentation

- [Architecture overview](docs/architecture/overview.md)
- [AI-assisted delivery model](docs/ai-assisted-delivery.md)
- [Roadmap](docs/roadmap.md)
- [Security policy](SECURITY.md)

## What this project is intended to show

- Salesforce security architecture thinking.
- Apex service and scanner design.
- LWC dashboard design with safe drill-downs.
- Tooling API usage through secure integration patterns.
- Data minimisation and evidence sanitisation.
- Requirements-driven delivery.
- Human-led use of AI assistants within clear engineering boundaries.

## What is not published here yet

- Apex classes.
- LWC source.
- Salesforce metadata.
- Named Credential values.
- Real org configuration.
- Real scan output.
- Screenshots using real data.
- Installation package.

Those items will only be considered for publication after sanitisation and final review.

## Status

Portfolio landing page: active.

Implementation publication: pending sanitisation and validation.
