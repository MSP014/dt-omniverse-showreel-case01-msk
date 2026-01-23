# ADR 002: QA & Security Protocols

## Status

Accepted

## Context

"Works on my machine" is not an acceptable delivery standard for an Urban Digital Twin. We deal with complex architectural data and transport logic where a single broken script can stop the pipeline. We also need to prevent credential leaks (e.g., Map API keys).

## Decision

We enforce a strict "Shift Left" strategy using `pre-commit` hooks and automated guardrails:

### 1. Guardrails (Pre-commit)

* **Linting:** `black` (Formatting), `flake8` (Logic), `isort` (Imports).
* **Security:**
  * `bandit`: Scans for common security issues (e.g., hardcoded passwords, unsafe exec).
  * `pip-audit`: Checks `requirements.txt` for known vulnerabilities.
* **Hygiene:** `check-added-large-files` (Max 10MB) to prevent repo bloating.

### 2. Testing

* `pytest` must pass locally before push.
* **Logic Validation**: Tests should verify procedural geometry generation (Houdini/Kit) and transport scheduling logic.
* **Note**: Tests are covered by Linters (Black/Flake8) but excluded from Bandit security scans to avoid false positives related to `assert` usage.

### 3. Secrets Management

* **Isolation**: All sensitive data (API keys, DB credentials) MUST be stored in a `.env` file.
* **Sanity**: The `.env` file MUST be included in `.gitignore`. Never commit secrets to version control.

## Consequences

* **Positive:** Higher code quality, reduced security risk, and blocked accidental large files.
* **Negative:** Initial setup friction; `pip-audit` requires maintenance of `requirements.txt`.
