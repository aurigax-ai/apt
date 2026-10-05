# Ostia APT repository

APT repository for [Ostia](https://github.com/aurigax-ai/ostia) on Debian and Ubuntu (x86_64).

The repository files live in the [`stable` release](https://github.com/aurigax-ai/apt/releases/tag/stable) of this repo, not in git. They are updated by the Ostia release workflow for every release.

## Install

```sh
sudo install -d -m 0755 /etc/apt/keyrings
curl -fsSL https://github.com/aurigax-ai/apt/releases/download/stable/ostia.gpg | sudo tee /etc/apt/keyrings/ostia.gpg >/dev/null
echo 'deb [signed-by=/etc/apt/keyrings/ostia.gpg] https://github.com/aurigax-ai/apt/releases/download/stable ./' | sudo tee /etc/apt/sources.list.d/ostia.list
sudo apt update && sudo apt install ostia
```

## Upgrade

```sh
sudo apt update && sudo apt upgrade
```

## Uninstall

```sh
sudo apt remove ostia
sudo rm /etc/apt/sources.list.d/ostia.list /etc/apt/keyrings/ostia.gpg
```

## Signing key

`Ostia APT Repository <aurigax.ai@gmail.com>`, ed25519, fingerprint:

```
09A9 4718 94A9 3B84 0503  0648 2E07 4C4A F7EE E2CC
```

Check it with `gpg --show-keys /etc/apt/keyrings/ostia.gpg`.
