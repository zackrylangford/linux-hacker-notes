# Package Management Comparison

This page compares package management systems across different Linux distributions.

## Overview

| Distribution | Package Manager | Package Format | Command Examples |
|--------------|----------------|----------------|-----------------|
| Arch/EndeavourOS | pacman | .pkg.tar.xz | `pacman -S`, `pacman -Syu` |
| Ubuntu/Xubuntu/Pop!_OS | apt | .deb | `apt install`, `apt update` |
| Fedora | dnf | .rpm | `dnf install`, `dnf update` |
| openSUSE | zypper | .rpm | `zypper install`, `zypper update` |

## Arch-based Package Management (pacman)

### Key Commands

```bash
# Update package database and upgrade all packages
sudo pacman -Syu

# Install a package
sudo pacman -S package_name

# Remove a package
sudo pacman -R package_name

# Remove a package and its dependencies
sudo pacman -Rs package_name

# Search for a package
pacman -Ss search_term

# List installed packages
pacman -Q

# Get information about a package
pacman -Qi package_name
```

### AUR Helpers

For the Arch User Repository (AUR), common helpers include:

```bash
# Using yay
yay -S package_name
yay -Syu  # Update system and AUR packages

# Using paru
paru -S package_name
paru -Syu  # Update system and AUR packages
```

## Debian-based Package Management (apt)

### Key Commands

```bash
# Update package database
sudo apt update

# Upgrade installed packages
sudo apt upgrade

# Install a package
sudo apt install package_name

# Remove a package
sudo apt remove package_name

# Remove a package and its configuration files
sudo apt purge package_name

# Search for a package
apt search search_term

# List installed packages
apt list --installed

# Get information about a package
apt show package_name
```

### Additional Package Sources

```bash
# Add a PPA repository
sudo add-apt-repository ppa:user/repository

# Install from a .deb file
sudo dpkg -i package.deb
sudo apt install -f  # Fix dependencies if needed
```

## Common Tasks Across Distributions

| Task | Arch/EndeavourOS | Ubuntu/Debian |
|------|------------------|---------------|
| Update system | `sudo pacman -Syu` | `sudo apt update && sudo apt upgrade` |
| Install package | `sudo pacman -S pkg` | `sudo apt install pkg` |
| Remove package | `sudo pacman -R pkg` | `sudo apt remove pkg` |
| Search packages | `pacman -Ss term` | `apt search term` |
| Clean cache | `sudo pacman -Sc` | `sudo apt clean` |
| Fix broken packages | `sudo pacman -Syyu` | `sudo apt --fix-broken install` |

## Package Management Best Practices

1. **Regular Updates**: Keep your system updated regularly for security and stability
2. **Read Before Upgrading**: Check release notes before major upgrades
3. **Backup First**: Always backup important data before major system upgrades
4. **Use Official Repositories**: Prefer official repositories when possible
5. **Clean Package Cache**: Periodically clean package caches to free disk space