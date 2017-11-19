# org.quetoo.Quetoo

## Prerequisites

```bash
flatpak install flathub org.freedesktop.Sdk
flatpak install flathub org.freedesktop.Platform
```

## Build

```bash
cd ~/Coding
git clone https://github.com/maci0/org.quetoo.Quetoo.git
flatpak-builder --repo=quetoo-repo build org.quetoo.Quetoo/org.quetoo.Quetoo.json
```
## Install & Test

```bash
flatpak --user remote-add --no-gpg-verify --if-not-exists quetoo-repo quetoo-repo
flatpak --user install quetoo-repo org.quetoo.Quetoo

mkdir ~/.quetoo
cp -r ~/Coding/quetoo-data/target/default ~/.quetoo

flatpak run org.quetoo.Quetoo

```
