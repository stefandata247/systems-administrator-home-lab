# Systems Administration Troubleshooting Log

## Issue 001 — RHEL Repository SSL Certificate Error

**Environment:** RHEL 10 ARM64

**Problem:** Unable to download repository metadata because of an SSL certificate verification failure.

**Error:**
`Curl error (60): SSL certificate problem: self-signed certificate in certificate chain`

**Diagnostic commands:**

```bash
sudo dnf repolist
curl -Iv https://cdn.redhat.com/
timedatectl
```

**Investigation:**

Investigate system time, certificate trust, network filtering, and possible HTTPS inspection.

**Resolution:**

Document the actual root cause and the verified corrective action once resolved. Do not disable SSL certificate verification.

**Verification:**

```bash
sudo dnf repolist
sudo dnf makecache
```

**Status:** Update after successful resolution.


