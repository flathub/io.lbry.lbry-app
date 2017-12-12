# io.lbry.lbry-app
A browser and wallet for LBRY, the decentralized, user-controlled content marketplace.

* Website: https://lbry.io/
* LBRY Issues: https://github.com/lbryio/lbry-app/issues
* Packaging Issues: https://github.com/flathub/io.lbry.lbry-app/issues

## Install

```bash
flatpak install flathub io.lbry.lbry-app
```

## Building

```bash
flatpak install flathub org.freedesktop.Sdk
flatpak install flathub org.freedesktop.Platform
flatpak install flathub io.atom.electron.BaseApp

git clone https://github.com/flathub/io.lbry.lbry-app.git

flatpak-builder --force-clean --repo=lbry-repo lbry-app io.lbry.lbry-app.json
flatpak --user remote-add --no-gpg-verify --if-not-exists lbry-app lbry-repo
flatpak --user install lbry-app io.lbry.lbry-app

flatpak run io.lbry.lbry-app
```
