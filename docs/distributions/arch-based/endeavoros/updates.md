# EndeavourOS Updates

This page covers how to update your EndeavourOS system and best practices for system maintenance.

## Basic System Update

EndeavourOS, being Arch-based, uses `pacman` as its package manager. To update your system:

```bash
# Update package databases and upgrade all packages
sudo pacman -Syu
```

## Using AUR Helpers

For packages from the Arch User Repository (AUR), you can use helpers like `yay`:

```bash
# Update system packages and AUR packages
yay -Syu

# Update only AUR packages
yay -Sua
```

## Update Frequency

Since EndeavourOS is a rolling release distribution, it's recommended to:

- Update at least once a week
- Check the [EndeavourOS news](https://endeavouros.com/news/) before major updates
- Consider joining the [EndeavourOS forum](https://forum.endeavouros.com/) to stay informed about critical updates

## Handling Partial Updates

Partial updates are not recommended in Arch-based systems. Always use `-Syu` to ensure all packages are updated together.

## Dealing with Package Conflicts

If you encounter package conflicts during updates:

1. Read the conflict message carefully
2. Check the [Arch news](https://archlinux.org/news/) for any known issues
3. Search the [EndeavourOS forum](https://forum.endeavouros.com/) for solutions
4. In most cases, accepting the default resolution is safe

## After Updates

After major updates, consider:

1. Checking if any `.pacnew` configuration files were created:
   ```bash
   find /etc -name "*.pacnew"
   ```

2. Rebooting if the kernel or graphics drivers were updated

## Troubleshooting

If your system won't boot after an update:

1. Boot from the EndeavourOS live USB
2. Mount your system and chroot into it:
   ```bash
   sudo mount /dev/sdaX /mnt  # Replace sdaX with your root partition
   sudo arch-chroot /mnt
   ```
3. Downgrade problematic packages or reinstall the kernel