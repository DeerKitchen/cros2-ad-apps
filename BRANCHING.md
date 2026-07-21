# Branching and Release Policy

## Branches

- `main`: stable development line.
- `release/x.y`: release maintenance.
- `hotfix/*`: urgent fixes from release branch.

## Versioning

- Use semantic versioning: `MAJOR.MINOR.PATCH`.
- Internal distro tags: `CROS2-YYYY.MM.PATCH`.
- Lock files must be versioned with release.

## Release Flow

1. Branch from `main` to `release/x.y`.
2. Freeze lockfile and dependency versions.
3. Run full CI (online + offline build verification).
4. Tag release and publish changelog + SBOM.

## Hotfix Rules

- Hotfix PR must target `release/x.y`.
- Cherry-pick or merge back to `main` after release.
- No force push on protected branches.

