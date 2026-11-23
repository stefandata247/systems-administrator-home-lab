# Project 03 — Linux Service and SSH Administration

## 1. Project Overview

**Objective:** Manage Linux system services and configure Secure Shell (SSH) for remote administration.

This project demonstrates how to manage services, inspect system logs, and verify SSH availability.

## 2. Skills Demonstrated

- systemd service management
- SSH administration
- Remote access
- Linux service troubleshooting
- Log management
- Firewall configuration

## 3. Implementation Steps

### Step 1 — Check SSH Service

```bash
sudo systemctl status sshd
```

### Step 2 — Enable SSH at Boot

```bash
sudo systemctl enable sshd
```

### Step 3 — Start SSH

```bash
sudo systemctl start sshd
```

### Step 4 — Verify SSH Status

```bash
sudo systemctl is-active sshd
sudo systemctl is-enabled sshd
```

### Step 5 — Check Listening Ports

```bash
sudo ss -tulnp | grep ':22'
```

### Step 6 — Configure Firewall for SSH

```bash
sudo firewall-cmd --add-service=ssh --permanent
sudo firewall-cmd --reload
```

### Step 7 — Review SSH Logs

```bash
sudo journalctl -u sshd -n 50
```

### Step 8 — Test SSH Locally

```bash
ssh localhost
```

Exit the SSH session with:

```bash
exit
```

## 4. Verification

Confirm SSH is active, enabled, listening on port 22, and permitted by the firewall.

## 5. Screenshots

1. SSH service status
2. SSH enabled at startup
3. Listening port 22
4. Firewall configuration
5. Successful local SSH connection

## 6. Troubleshooting

Document SSH connection failures, service errors, firewall problems, and their verified resolutions.

## 7. Lessons Learned

Developed practical experience managing Linux services and configuring secure remote administration.

## 8. Project Status

Update after completing all tests.


