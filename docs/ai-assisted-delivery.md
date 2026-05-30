# AI-Assisted Delivery Model

This project intentionally uses AI assistants as delivery collaborators with clear boundaries.

The objective is not to present AI-generated code as a shortcut. The objective is to show how a Salesforce architect can use AI responsibly to accelerate delivery while keeping requirements, security, validation and human accountability explicit.

## Tools used in the delivery model

The private implementation workflow uses tools such as:

- GPT for architecture discussion, requirement slicing, prompt design and review.
- Claude for secondary critique, wording review and challenge where useful.
- Codex-style local development assistance for repository inspection, file edits and validation support.

These tools are treated like junior delivery collaborators. They are given defined scope, source-of-truth documents and acceptance rules. They do not own the architecture, security posture or final decision.

## Operating principles

- Requirements are written before implementation.
- Each task is narrow and traceable to requirement IDs.
- The repository contains source-of-truth documentation.
- AI tools must inspect before editing.
- AI tools must not mix feature work, cleanup, formatting, API migration and coverage hardening in the same task.
- Every material change must report files changed, validation run, security impact and what was not done.
- Human review remains mandatory.
- Git, Salesforce validation and test output are the source of truth.

## Safety boundaries

AI tools are not given permission to:

- Invent requirements.
- Perform broad refactors without approval.
- Add remediation actions.
- Expose secrets, tokens, session IDs, certificate bodies or raw sensitive evidence.
- Add new objects, fields, permission sets or integrations without explicit approval.
- Mark requirements complete without validation evidence.
- Publish private implementation details to the public repository.

## Why this matters

This delivery model is part of the architecture story.

Modern Salesforce delivery increasingly involves AI-assisted development. The value is not in letting a model write unchecked code. The value is in using AI with the same discipline expected from a delivery team:

- Clear requirements.
- Defined ownership.
- Traceability.
- Review gates.
- Security constraints.
- Repeatable validation.
- Honest status reporting.

## Accountability

The project owner remains accountable for:

- Architecture decisions.
- Security boundaries.
- Requirement approval.
- Deployment decisions.
- Commit decisions.
- Public release decisions.

AI is used as a controlled accelerator, not as an autonomous delivery authority.
