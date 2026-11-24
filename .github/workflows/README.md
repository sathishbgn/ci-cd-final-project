# GitHub Actions Workflows

This directory contains the GitHub Actions workflows for the CI/CD Tools and Practices Final Project.

## `workflow.yml` — CI workflow

Runs unit tests on every push and pull request to `main`.

**Triggers**

- `push` to `main`
- `pull_request` targeting `main`

**Job: `build`**

Runs on `ubuntu-latest` inside a `python:3.9-slim` container. Steps:

1. **Checkout** — checks out the repository (`actions/checkout@v3`).
2. **Install dependencies** — upgrades pip and installs `requirements.txt`.
3. **Run unit tests with nose** — runs `nosetests` with verbose spec output and coverage for the `service` package.

## Running the same checks locally

```bash
pip install -r requirements.txt
nosetests -v --with-spec --spec-color --with-coverage --cover-package=service
```
