# Download link
https://s3.usershare.nl/workstation/install.iso
https://s3.usershare.nl/workstation/install.iso-CHECKSUM
They will only be updated occasionally

# Rebase Instructions
To rebase an existing atomic Fedora installation to the latest build:

If you are comming from another build like silverblue first rebase to the unsigned image, to get the proper signing keys and policies installed:

`rpm-ostree rebase ostree-unverified-registry:ghcr.io/bluefora/workstation:latest`

Reboot to complete the rebase:

`systemctl reboot`

If you are on any Bluefora build or rebased to unsigned from another buid (see above).
Rebase to the signed image, like so:

`rpm-ostree rebase ostree-image-signed:docker://ghcr.io/bluefora/workstation:latest`

Reboot again to complete the installation

`systemctl reboot`

# NVidia version
`rpm-ostree rebase ostree-unverified-registry:ghcr.io/bluefora/workstation-nvidia:latest`
`systemctl reboot`

# Developer version
`rpm-ostree rebase ostree-unverified-registry:ghcr.io/bluefora/developer:latest`
`systemctl reboot`

