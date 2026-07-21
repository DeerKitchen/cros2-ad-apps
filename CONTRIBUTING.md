# Contributing Guide

## Commit and PR Rules

- Use small, reviewable PRs (recommended < 800 LOC changed).
- One PR should solve one problem.
- Include **why** in commit message and PR description.
- Add/adjust tests for behavior changes.

## Branch Policy

- `main`: protected, release-ready only.
- `release/*`: hotfix and patch maintenance.
- `feature/*`: regular development branches.

## Required Checks

- Lint and format
- Unit/integration tests
- Docker offline build smoke
- Security scan (if configured)

## Review and Ownership

- Core runtime (`platform/`, `mw/`, `vendor/`) requires owner approval.
- Schema/message changes require compatibility note and migration path.
- Breaking changes must be marked clearly in PR title/body.

