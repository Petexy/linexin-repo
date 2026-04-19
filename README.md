# linexin-repo

The official package repository for [Linexin](https://petexy.github.io/Linexin/).

## Adding linexin-repo to Arch Linux

### 1. Import the signing key

```bash
sudo pacman-key --recv-keys D983B0DF839B8A5E5699BA3499455E14A4CD88E6 --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key D983B0DF839B8A5E5699BA3499455E14A4CD88E6
```

### 2. Add the repository

Add the following to `/etc/pacman.conf`:

```ini
[linexin-repo]
SigLevel = Optional DatabaseOptional TrustedOnly
Server = https://petexy.github.io/linexin-repo/x86_64
```

### 3. Sync and install the keyring

```bash
sudo pacman -Sy linexin-keyring
```

This installs the keyring package which will manage the signing key automatically for future updates.
