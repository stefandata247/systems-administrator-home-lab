# Project 04 — RHEL 10 Security Hardening

## 1. Project Overview

**Objective:** Review and improve the security configuration of a RHEL 10 server.

This project focuses on SELinux, firewalld, SSH security, system services, and authentication auditing.

## 2. Skills Demonstrated

- Linux security administration
- SELinux
- Firewall management
- SSH security
- Authentication auditing
- System hardening

## 3. Implementation Steps

### Step 1 — Inspect SELinux

```bash
getenforce
sestatus
```

Target configuration: Enforcing.

### Step 2 — Inspect Firewall

```bash
sudo systemctl status firewalld
sudo firewall-cmd --state
sudo firewall-cmd --list-all
```

### Step 3 — Inspect Listening Ports

```bash
sudo ss -tulnp
```

### Step 4 — Inspect SSH Security Settings

```bash
sudo sshd -T | grep -E 'permitrootlogin|passwordauthentication'
```

Document the current configuration before making changes.

### Step 5 — Inspect Login Activity

```bash
last
sudo journalctl -u sshd --since today
```

### Step 6 — Review Running Services

```bash
systemctl --type=service --state=running
```

Identify services that are unnecessary for the lab. Research their purpose before disabling anything.

## 4. Verification

Document:

- SELinux status
- Firewall status
- Open ports
- SSH configuration
- Authentication activity
- Running services

## 5. Screenshots

1. SELinux status
2. Firewall status
3. Listening ports
4. SSH security configuration
5. Login audit information

## 6. Troubleshooting

Record security configuration errors, access issues, and any corrective actions.

## 7. Lessons Learned

Developed practical experience inspecting Linux security controls and identifying potential configuration weaknesses.

## 8. Project Status

Update after completing security checks and documenting the results.


