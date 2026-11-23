# Project 06 — Bash Automation and Backup

## 1. Project Overview

**Objective:** Develop Bash scripts to automate routine Linux Systems Administration tasks.

This project demonstrates how to create system health reports, monitor system resources, and automate file backups.

## 2. Skills Demonstrated

- Bash scripting
- Linux automation
- Disk monitoring
- Memory monitoring
- Backup management
- Script permissions
- Shell troubleshooting

## 3. Implementation Steps

### Step 1 — Create Script Directory

```bash
mkdir -p ~/admin-lab/scripts
cd ~/admin-lab/scripts
```

### Step 2 — Create System Health Script

Create `system-health.sh`:

```bash
#!/bin/bash

echo "===== SYSTEM HEALTH REPORT ====="
echo "Date: $(date)"
echo "Hostname: $(hostname)"

echo
echo "===== UPTIME ====="
uptime

echo
echo "===== MEMORY ====="
free -h

echo
echo "===== DISK SPACE ====="
df -h

echo
echo "===== END REPORT ====="
```

### Step 3 — Make Script Executable

```bash
chmod +x system-health.sh
```

### Step 4 — Execute Script

```bash
./system-health.sh
```

### Step 5 — Save Health Report

```bash
./system-health.sh > health-report.txt
```

### Step 6 — Create Backup Script

Create `backup-lab.sh`:

```bash
#!/bin/bash

SOURCE="/company"
DEST="$HOME/admin-lab/backups"

mkdir -p "$DEST"

DATE=$(date +%Y-%m-%d_%H-%M-%S)

tar -czf "$DEST/company-$DATE.tar.gz" "$SOURCE"

echo "Backup completed: $DEST/company-$DATE.tar.gz"
```

### Step 7 — Make Backup Script Executable

```bash
chmod +x backup-lab.sh
```

### Step 8 — Run Backup

```bash
./backup-lab.sh
```

### Step 9 — Verify Backup

```bash
ls -lh ~/admin-lab/backups
```

Test the archive:

```bash
tar -tzf ~/admin-lab/backups/company-*.tar.gz
```

## 4. Verification

Confirm:

- Health report generates successfully.
- Memory and disk information are displayed.
- Backup archive is created.
- Backup archive can be listed and inspected.

## 5. Screenshots

1. Script creation
2. Executable script permissions
3. Health report output
4. Backup script execution
5. Backup archive verification

## 6. Lessons Learned

Developed practical experience automating administrative tasks using Bash, monitoring system resources, and creating backup archives.

## 7. Project Status

Update after successful testing.


