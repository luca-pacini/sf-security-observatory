# Salesforce Security Observatory — Landing Page

Public marketing / landing page for **Salesforce Security Observatory**, a native Salesforce security scanning tool.

This repository contains the static landing page only. It is served via GitHub Pages and collects install-link requests through a Formspree form.

## Purpose

- Present what the tool does, how it works, and who built it.
- Capture install-link requests from interested Salesforce admins and architects.
- Stay entirely static — no build step, no framework, no external JavaScript, CSS, or fonts.

## Contents

| File | Description |
| --- | --- |
| `index.html` | Single-page static landing page. |
| `styles.css` | Dark, security-tool styling. System fonts only. |
| `README.md` | This file. |

## No Salesforce source code here

> **This repository contains no Salesforce source code or package files.**

The Salesforce implementation (Apex, LWC, metadata, package definitions) lives in a separate **private** repository. Nothing in this public repo should ever include source code, package metadata, org identifiers, usernames, callback URLs, tokens, session IDs, secrets, screenshots, or customer data.

## GitHub Pages setup

Pages should be served from the `main` branch root.

If Pages is not already enabled, configure it manually:

1. Go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Set **Branch** to **`main`** and **Folder** to **`/ (root)`**.
4. Click **Save**.

The site will publish at: `https://luca-pacini.github.io/sf-security-observatory/`

## Formspree endpoint replacement

The lead-capture form in `index.html` posts to a placeholder endpoint:

```html
<form action="https://formspree.io/f/REPLACE_ME" method="POST">
```

To activate it:

1. Create a free form at [formspree.io](https://formspree.io/) and copy your form's endpoint (it looks like `https://formspree.io/f/abcd1234`).
2. In `index.html`, replace `https://formspree.io/f/REPLACE_ME` with your real endpoint.
3. Commit and push. Submissions will then be delivered to the email configured in Formspree.

No API keys or secrets are stored in this repo — Formspree identifies the form by the public endpoint ID only.

## Safety checklist before publishing

Confirm **none** of the following are present anywhere in this repo before pushing or going live:

- [ ] Salesforce source code (Apex, LWC, triggers, metadata).
- [ ] Package metadata or a managed package install URL.
- [ ] Org IDs, usernames, or login URLs.
- [ ] Callback URLs, OAuth client/consumer secrets.
- [ ] Access tokens, refresh tokens, session IDs, or any secrets.
- [ ] Private keys or certificate bodies.
- [ ] Screenshots, real scan output, or production/customer data.
- [ ] External JavaScript, external CSS, Google Fonts, or stock art.
- [ ] Analytics or tracking scripts.
- [ ] A real Formspree endpoint committed before you intend the form to be live (placeholder is `REPLACE_ME`).

## Licence terms

`[LICENCE TERMS URL]`

This tool is free to use. Source is proprietary. Replace the placeholder above with the published licence terms URL when available.

---

© 2026 Luca Pacini. Independent tool, not affiliated with Salesforce Inc.
