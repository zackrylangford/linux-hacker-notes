# Scripts

This section contains useful scripts for Linux system administration and automation.

## Backup Scripts

```bash
#!/bin/bash
# Simple backup script
BACKUP_DIR="/backup"
SOURCE_DIR="/home/user/documents"
DATE=$(date +%Y-%m-%d)

mkdir -p $BACKUP_DIR
tar -czf $BACKUP_DIR/backup-$DATE.tar.gz $SOURCE_DIR
echo "Backup completed: $BACKUP_DIR/backup-$DATE.tar.gz"
```

## System Maintenance

```bash
#!/bin/bash
# System update script
apt update
apt upgrade -y
apt autoremove -y
echo "System updated successfully"
```

## Networking Scripts

- Coming soon