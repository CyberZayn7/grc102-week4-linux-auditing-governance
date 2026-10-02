# GRC102 Week 4: Linux Auditing and Security Governance Lab

## Student Information

- Name: Zainab Umar Shuaibu
- Programme: ICDFA Cohort 11
- Course: GRC102 – Information Security Governance
- Module: Monitoring and Auditing Security Controls

## Overview

This laboratory demonstrates the implementation of Linux auditing, authentication log analysis, security assessment, and governance monitoring practices using:

- auditd
- auditctl
- systemd-journald
- journalctl
- Lynis 3.1.4

The objective was to collect security evidence, identify control deficiencies, analyze authentication events, and map findings to governance and compliance requirements.

## Key Findings

### 1. Authentication Log Relocation

Traditional log analysis using `/var/log/auth.log` was unsuccessful because the system relied on `systemd-journald` instead.

### 2. SSH Authentication Failures

Multiple failed login attempts were successfully captured using:

```bash
journalctl -f -u ssh
```

### 3. Security Hardening Gaps

Lynis identified:

- Unencrypted root partition (`/dev/sda1`)
- Missing fail2ban
- Missing libpam-tmpdir
- Missing GRUB password protection

## Tools Used

- Kali Linux Rolling Release
- auditd
- auditctl
- journalctl
- systemd-journald
- Lynis 3.1.4

## Governance Alignment

The findings were mapped to:

- ISO/IEC 27001
- NIST Cybersecurity Framework
- Continuous Control Monitoring practices
- SIEM escalation procedures

## Repository Contents

| Folder | Purpose |
|----------|----------|
| report | Final lab report |
| evidence | Screenshots and supporting evidence |
| configurations | Audit configurations |
| docs | Governance and monitoring documentation |

## Author

Zainab Umar Shuaibu
