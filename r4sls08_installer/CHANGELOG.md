# 1.0.11

- Mark Velnio Installer as stable for normal Home Assistant App updates.
- Bundle integration 0.5.28 and preserve the existing App identity, installation
  path, verified backups, rollback and Core restart behavior.
- Publish releases from master when VERSION increases: test both architectures,
  publish the private image, then publish the verified public metadata and logo.

# 1.0.10

- Replace Eltuno branding with the approved Velnio master artwork in the
  Installer App and R4SLS08 integration, including light/dark and 2× images.
- Display Velnio in the App and integration names while preserving the existing
  technical slugs, entity identities, and update path.

- Bundle integration 0.5.28 with separate single-click, double-click and hold
  mappings, preserved targets across entity renames, and hold confirmation from
  fresh input samples.

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
