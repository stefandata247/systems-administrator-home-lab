# Project 05 — Linux Network Troubleshooting

## 1. Project Overview

**Objective:** Diagnose and troubleshoot network connectivity and DNS resolution issues on a RHEL 10 virtual machine.

This project demonstrates how to inspect network interfaces, IP addresses, routing, DNS, and listening ports.

## 2. Skills Demonstrated

- TCP/IP networking
- IP address configuration
- DNS troubleshooting
- NetworkManager
- Routing
- Connectivity testing
- Port inspection

## 3. Implementation Steps

### Step 1 — Inspect Network Interfaces

```bash
ip addr
```

### Step 2 — Inspect Routing Table

```bash
ip route
```

### Step 3 — Inspect NetworkManager

```bash
nmcli device status
nmcli connection show
```

### Step 4 — Test Internet Connectivity

```bash
ping -c 4 example.com
```

### Step 5 — Test DNS Resolution

```bash
getent hosts redhat.com
```

Optional additional test:

```bash
nslookup redhat.com
```

### Step 6 — Inspect DNS Configuration

```bash
cat /etc/resolv.conf
nmcli device show
```

### Step 7 — Inspect Listening Ports

```bash
sudo ss -tulnp
```

## 4. Troubleshooting Scenarios

| Scenario | Diagnostic command |
|---|---|
| No internet | `ip route` |
| DNS failure | `getent hosts redhat.com` |
| Incorrect IP | `ip addr` |
| Network connection failure | `nmcli device status` |
| Port not listening | `ss -tulnp` |
| Firewall issue | `firewall-cmd --list-all` |

## 5. Verification

Record actual connectivity results, DNS resolution, IP configuration, and routing information.

## 6. Screenshots

1. Network interfaces
2. Routing table
3. NetworkManager status
4. Ping results
5. DNS resolution results
6. Listening ports

## 7. Lessons Learned

Developed practical Linux networking and troubleshooting skills, including IP addressing, routing, DNS, and network connectivity diagnostics.

## 8. Project Status

Update after completing all tests.


