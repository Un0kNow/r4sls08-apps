# R4SLS08 Installer

This App installs the R4SLS08 custom integration from its verified, immutable
payload. Keep the App running to receive native App updates.

The default settings retain five verified backups and allow 180 seconds for Home
Assistant Core health checks. A failed release is not retried automatically.

To restore a retained version, inspect
`/config/.r4sls08-installer/backups/<32-character-id>/backup.json`, select the
required backup ID, put it in `rollback_to`, save, and restart the App. Keep the
selection until you are ready to install a newer App release; clearing it lets
the payload in the currently installed image deploy on the next App start.
