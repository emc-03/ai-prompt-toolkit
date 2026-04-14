# Security Policy

## Purpose

This repository is a public prompt toolkit and does not contain production systems or sensitive infrastructure.
This document explains how to report issues and what to expect.

---

## Supported Scope

This repository includes:

* Markdown files (`.md`)
* Prompt templates
* Documentation

There are **no active services, APIs, or deployed environments** associated with this repository.

---

## Reporting a Vulnerability

If you discover a potential security issue, please **do not open a public issue**.

Instead:

* Report it privately via GitHub (if enabled), or
* Open an issue with **limited detail** (avoid sharing sensitive information)

When reporting, include:

* A clear description of the issue
* Steps to reproduce (if applicable)
* Potential impact

---

## What to Avoid

Do **not** include the following in issues or pull requests:

* API keys
* passwords
* tokens
* private URLs
* raw logs containing sensitive data

Use placeholders instead:

```text
[REDACTED_API_KEY]
[REDACTED_TOKEN]
```

---

## Security Practices

This repository follows these basic practices:

* `.env` files and secrets are excluded via `.gitignore`
* No credentials or sensitive data should be committed
* Example data should always be sanitized
* Prompts are designed to avoid exposing sensitive information

---

## Known Limitations

Since this is a public repository:

* All content is visible to anyone
* Do not assume privacy for any committed data
* Avoid including real system details or internal architecture

---

## Responsibility

Contributors are responsible for:

* Not committing sensitive information
* Reviewing content before pushing
* Following safe data handling practices

---

## Final Note

If you are unsure whether something is sensitive:

> Do not commit it.

Err on the side of caution and use placeholders or redacted values.
