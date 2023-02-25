# RebornOS Software Template

[![Discord Server](https://dcbadge.vercel.app/api/server/cU5s6MPpQH?style=flat)](https://discord.gg/cU5s6MPpQH)
![GitHub](https://img.shields.io/github/license/rebornos-developers/rebornos-software-template)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/rebornos-developers/rebornos-software-template)
[![Release](https://github.com/RebornOS-Developers/rebornos-software-template/actions/workflows/release.yml/badge.svg)](https://github.com/RebornOS-Developers/rebornos-software-template/actions/workflows/release.yml)
[![Pre-Release (Git)](https://github.com/RebornOS-Developers/rebornos-software-template/actions/workflows/pre_release.yml/badge.svg)](https://github.com/RebornOS-Developers/rebornos-software-template/actions/workflows/pre_release.yml)

> **Note**: Please do a search and replace for `rebornos-software-template` and `RebornOS Software Template` to make it easy. Please *do not* match whole words for searching, because the project name is used with suffixes.

## Cloning

In order to download the source code to your local computer for testing, or for development, you can clone from the remote repository using either SSH, or HTTPS. Below are instructions on how to do so using Gitlab hosted code as remote.

### HTTPS

```bash
git clone https://github.com/RebornOS-Developers/rebornos-software-template.git 
```

OR

### SSH

```bash
git clone git@github.com:RebornOS-Developers/rebornos-software-template.git
```

## Packaging

Change to the project directory (`cd rebornos-software-template`) and run any of the below scripts:
- `sh packaging/setup.sh <MODE>`: Builds and installs a package
- `sh packaging/build-package.sh <MODE>`: Just builds a package without installing it locally
- `sh packaging/install-package.sh <MODE>`: Just installs a package locally, except if no built package is detected, a package is built.

- where `<MODE>` can be one of the below
     1. `local`: Selects *rebornos-software-template-local* from the local project that you have cloned already.
     2. `git`: Selects *rebornos-software-template-git* from the latest git commit.
     3. `stable`: Selects *rebornos-software-template* from the git tag corresponding to the [`pkgver` specified in the PKGBUILD](https://github.com/RebornOS-Developers/rebornos-software-template/blob/main/packaging/rebornos-software-template/PKGBUILD#L4). If `pkgver=0.1.2`, then the git tag `v0.1.2` is used for packaging. 
     
> **Note**: Any additional parameters passed to the above scripts are automatically sent to `makepkg` or `pacman` (whichever is applicable).
