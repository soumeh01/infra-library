# infra-library

A central catalogue of production-ready GitHub Actions workflows, CI/CD
templates, and helper scripts that can be pulled into any repository via
`uses: arm-chatgpt/infra-library/...`.

## Why this exists

* **DRY your pipelines** – define common jobs once and share them company-wide.
* **Consistent standards** – security scans, test matrices, release tagging and
  artefact publishing all follow the same rules.
* **Faster onboarding** – new projects inherit best-practice workflows out of
  the box.

## What you’ll find here

* `workflows/`   – versioned Composite Actions (build, test, release, deploy).  
* `scripts/`     – language-agnostic helper scripts (bash, Python, PowerShell).  
* `templates/`   – starter YAMLs and `.github` snippets to drop into a repo.  

## Getting started

1. Add the required secrets to **Settings → Secrets and Variables** in your repo.
2. Reference a workflow:

```yaml
# .github/workflows/ci.yml
name: CI
on: [push, pull_request]

jobs:
  build:
    uses: arm-chatgpt/infra-library/workflows/ci@v1
