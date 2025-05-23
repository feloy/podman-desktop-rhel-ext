# Macadam Extension

The RHEL extension helps the user run RHEL VMs.

## Pre-requisites

### On Windows

The `macadam` binary is embedded in the extension, nothing needs to be installed.

### On Mac

When initialized, the extension checks if the necessary binaries are present in `/opt/macadam/bin`. If they are not, the extension installs them in this directory.

> If this installation fails, you can run the installer manually, using the installer found at https://github.com/crc-org/macadam/releases/tag/v0.1.0. After this, you need to restart the extension which should find and use the binaries.

## Install the extension

OCI Images to install the extensions are available at https://github.com/redhat-developer/podman-desktop-rhel-ext/pkgs/container/podman-desktop-rhel-ext.

The latest development image is ghcr.io/redhat-developer/podman-desktop-rhel-ext:next

## Contributing

Want to help develop and contribute to the Macadam extension?

You can use pnpm watch --extension-folder from the Podman Desktop directory to automatically rebuild and test the Macadam extension:

Note: make sure you have the appropriate [pre-requisites](https://github.com/podman-desktop/podman-desktop/blob/main/CONTRIBUTING.md#prerequisites-prepare-your-environment) installed.

```
git clone https://github.com/containers/podman-desktop
git clone https://github.com/redhat-developer/podman-desktop-rhel-ext
cd podman-desktop-rhel-ext
pnpm install
pnpm build
cd ../podman-desktop
pnpm watch --extension-folder ../podman-desktop-rhel-ext
```
