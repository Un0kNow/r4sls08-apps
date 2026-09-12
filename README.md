# R4SLS08 Apps

This repository contains only public Home Assistant App metadata and documentation.
The image is distributed through an authenticated, private container registry.

## R4SLS08 Installer — POC

The POC reports its image version in the App log and remains running. It does
not install the R4SLS08 integration or restart Home Assistant Core.

On Home Assistant OS, configure the supplied registry read credentials in the
App store's registry settings, add this repository URL to the App store, then
install and start **R4SLS08 Installer**. Never put registry credentials in a Git
URL or App options. Supported architectures: amd64 and aarch64.

Updates appear through Home Assistant's standard App update mechanism after a
new image has been published and the repository metadata version has increased.
See the App's Documentation tab for the POC verification steps.
