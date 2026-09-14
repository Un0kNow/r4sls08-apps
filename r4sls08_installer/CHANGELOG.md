# 1.0.8

- Add Eltuno branding to the Installer App and the R4SLS08 integration, including
  light/dark and high-resolution integration images.
- Include branding in release exports and support the first metadata promotion
  from the original repository without images.
- Bundle integration 0.5.23 with the Eltuno assets.

# 1.0.7

- Keep the Installer App running when a newer integration was installed manually.
  Report installed and bundled versions with `READY: newer_installed`; do not
  replace the integration, create a deployment transaction or restart Core.
- Preserve strict payload validation, downgrade protection and explicit rollback.
- Bundle integration 0.5.22 with resilient DI-to-relay mappings across entity
  renames, missing-target repairs, and on-demand DI diagnostics.

# 1.0.1

- Release the tested transactional installer through the private source-tag build.

# 1.0.0

- First production installer release.
- Verifies a source-commit-bound payload before an atomic install or update.
- Preserves verified backups and restores the previous integration on failure.
