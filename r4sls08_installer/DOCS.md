# Velnio Installer

This App installs the Velnio R4SLS08 custom integration from its verified, immutable
payload. Keep the App running to receive native App updates.

The default settings retain five verified backups and allow 180 seconds for Home
Assistant Core health checks. A failed release is not retried automatically.

If you manually install an integration version newer than the one bundled in
this App, the installer keeps it and reports `READY: newer_installed`. The log
shows both versions. The App stays running without replacing files or restarting
Core. Update the Installer App when a newer bundled integration is available.
Do not set `rollback_to` merely to clear a version mismatch; it explicitly
restores the selected older backup. `retry_failed_release` does not allow an
automatic downgrade.

To restore a retained version, inspect
`/config/.r4sls08-installer/backups/<32-character-id>/backup.json`, select the
required backup ID, put it in `rollback_to`, save, and restart the App. Keep the
selection until you are ready to install a newer App release; clearing it lets
the payload in the currently installed image deploy on the next App start.
