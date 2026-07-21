# Release Checklist

## Pre-Release

- [ ] All required CI checks passed
- [ ] `vendor` lock file updated and reviewed
- [ ] Offline build (`./scripts/build_offline.sh`) passed
- [ ] API/schema compatibility reviewed
- [ ] Security and license scan completed

## Artifacts

- [ ] Source bundle created
- [ ] Offline Docker base image tar present
- [ ] Release notes generated
- [ ] SBOM generated and archived

## Validation

- [ ] Runtime smoke on amd64
- [ ] Cross-compile smoke on aarch64
- [ ] Key scenario replay/record verification

## Publish

- [ ] Tag pushed (`CROS2-YYYY.MM.PATCH`)
- [ ] Release notes published
- [ ] Rollback plan documented

