# POC installation and updates

Requires Home Assistant OS with Supervisor, a supported 64-bit architecture,
and registry read access. Home Assistant Container has no Supervisor App store.

1. Configure registry credentials once through the App store menu's registry
   settings (Registries). For GHCR use hostname `ghcr.io`, the GitHub username
   and a PAT classic with `read:packages`. That user also needs package read access.
2. Add the public Git repository URL through the store's Repositories menu.
3. Install **R4SLS08 Installer** version **0.1.0** and click Start.
4. The log must report `R4SLS08_INSTALLER_POC version=0.1.0` and `POC_READY`.
5. Leave the POC running and automatic App updates disabled for this test.
6. After the publisher announces 0.1.1, refresh/check for updates in the store.
7. Open **Settings → Updates → R4SLS08 Installer → Update**.
8. Confirm installed version **0.1.1**, running state, and a new startup log
   containing `R4SLS08_INSTALLER_POC version=0.1.1` and `POC_READY`.

The POC does not mount Home Assistant configuration, call Core or Supervisor
APIs, or contain an integration payload. Core should remain running throughout.
An App that was stopped before Update may need to be started manually afterward.

If installation reports unauthorized/denied, check package read access, token
scope/expiry and organization SSO. If no update appears, check repository refresh,
metadata version and App update entity. A version must have a published image
tag with both supported architectures before metadata is changed.

Uninstalling this POC removes only the App. No integration rollback is necessary.
