# AuditMate – Complete System Auditing for Linux

AuditMate is an automated system auditing tool designed to give administrators full visibility into their Linux servers. It monitors system health, detects security issues, tracks changes over time, and provides actionable warnings—all with minimal setup.

---

## Open Source Core

AuditMate’s core functionality is open source. You can:

- View and contribute to the core scan and baseline features on GitHub.
- Customize the core for your needs.
- Run the core offline, fully free.

Advanced features like JSON export, premium license features, and detailed reports are part of the paid version and remain closed source. This allows AuditMate to stay sustainable while keeping the core transparent and community-friendly.

---

## Key Features

### 1. System Overview
AuditMate collects essential information about your system, including:
- Hostname, operating system, and kernel version
- Uptime and active users
- Admin and regular users
- Running services
- Installed packages
- Open ports
- Firewall state
- Pending system updates

### 2. Change Tracking
- **Baseline Comparison**: AuditMate saves a snapshot of your system to a baseline file (`baseline.json`) and compares future scans to it.
- **Diff Detection**: Changes are highlighted, showing what was added, removed, or modified since the last baseline.
- **Critical Alerts**: Certain changes, such as new admin accounts or an open SSH port, trigger critical warnings.

### 3. Warnings
AuditMate detects and flags potential security and system issues:
- Multiple admin users detected
- SSH port 22 open
- Firewall inactive or disabled
- System updates available

Warnings are categorized into **critical** and **non-critical**, reflected in the scan exit codes.

### 4. Automation
AuditMate supports fully automated scanning using cron:
- Schedule scans **daily**, **hourly**, **weekly**, **yearly**, or at custom minute intervals.
- Multiple scan times can be set for daily, weekly, or yearly schedules.
- Dry-run mode allows previewing scheduled scans before applying them.
- Summaries show all scheduled scan times for easy reference.

### 5. Licensing & Premium Features
- Premium features require a paid license.
- JSON export and detailed reports are unlocked with a valid license.
- Licenses can be activated on multiple devices.
- Ensures full reporting capabilities for premium users.

### 6. Output & Reporting
- Terminal summary provides immediate insights during a scan.
- Baseline diffs show exactly what has changed since the last scan.
- Premium reports can be exported in JSON for further analysis.
- Exit codes reflect scan severity:
  - `0` — No warnings
  - `1` — Non-critical warnings
  - `2` — Critical warnings

### 7. Flexibility
- Designed to run on any Linux system with minimal dependencies.
- Can be scheduled automatically but also run manually.
- Works in fully offline environments.
- Highly configurable for multiple scan frequencies and times per day.

---

## Pricing

| Plan | Price | Notes |
|------|-------|------|
| Free Tier | $0 | Core scanning & baseline features, offline support |
| Monthly | $25 | Full premium features |
| Yearly | $250 | Full premium features for one year |
| Founding Member | $200 | Price locked for life, includes **all premium features** (limited to first 100 signups) |

For early access or to become a founding member, **contact:** [audit-mate@proton.me](mailto:audit-mate@proton.me)

---

## Why AuditMate?

AuditMate is designed for system administrators who need:
- Automated monitoring without constant oversight
- Quick detection of security risks
- Historical tracking of system changes
- A lightweight tool that doesn’t overload your system

With AuditMate, you get visibility and peace of mind, letting you focus on managing your infrastructure instead of manually auditing it.

---

## Example Output

```text
========== AuditMate Summary ==========
Hostname: hp
OS: Ubuntu 24.04.3 LTS
Kernel: 6.6.87.2-microsoft-standard-WSL2
Uptime: up 17 hours

Admins: [root]
Regular Users: [nobody ubuntu]

Services running: 3
Packages installed: 3
Open ports: 15

Warnings:
- Firewall is inactive or disabled
- System updates are available
- SSH port 22 is open
======================================
Baseline saved to: auditmate-output/baseline.json
AuditMate scan completed with exit code 2
