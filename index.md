# AuditMate – Complete System Auditing for Linux

## Open Source Core

AuditMate’s **core functionality** is open source and fully free. You can:  

- View and contribute to the core scan and baseline features on GitHub.  
- Customize the core to fit your needs.  
- Run the core **completely offline**, without any internet connection.  
- Enjoy a **free tier** with essential auditing capabilities.  

Advanced features, including **JSON export and premium license features**, are part of the paid version and remain closed source. This ensures sustainability while keeping the core transparent and community-friendly.

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

This gives you a snapshot of your system at a glance.

### 2. Change Tracking
- **Baseline Comparison**: Saves a snapshot of your system to `baseline.json` and compares future scans against it.  
- **Diff Detection**: Highlights added, removed, or modified items since the last baseline.  
- **Critical Alerts**: Certain changes, like new admin accounts or an open SSH port, trigger critical warnings.

### 3. Warnings
AuditMate flags potential security and system issues:  
- Multiple admin users detected  
- SSH port 22 open  
- Firewall inactive or disabled  
- System updates available  

Warnings are categorized as **critical** or **non-critical**.

### 4. Automation
- Schedule scans **daily**, **hourly**, **weekly**, **yearly**, or at custom minute intervals.  
- Multiple scan times can be set for daily, weekly, or yearly schedules.  
- Dry-run mode previews scheduled scans before applying them.  
- Optional summaries show all scheduled scan times for easy reference.

### 5. Licensing & Premium Features
- Paid licenses unlock advanced features like JSON export and detailed reports.  
- Licenses can be used on multiple devices.  
- Core functionality remains free for basic auditing, with optional upgrades for full reporting.

### 6. Output & Reporting
- Terminal summary provides immediate insights during a scan.  
- Baseline diffs show exactly what has changed since the last scan.  
- Premium reports can be exported in JSON for further analysis.  
- Exit codes reflect scan severity:  
  - `0` — No warnings  
  - `1` — Non-critical warnings  
  - `2` — Critical warnings  

### 7. Flexibility
- Runs on any Linux system with minimal dependencies.  
- Can be scheduled automatically or run manually.  
- Fully offline, no internet required.  
- Configurable for multiple scan frequencies and times per day.

---

## Pricing

| Plan | Price | Notes |
|------|-------|------|
| Free Tier | $0 | Core scanning & baseline features, offline support |
| Monthly | $25 | Full premium features |
| Yearly | $250 | Full premium features |
| Early Access / Founding Member | $200 first 100 | Price locked for life |

For early access or to become a founding member, **contact:** [audit-mate@proton.me](mailto:audit-mate@proton.me)

---

## Why AuditMate?

AuditMate is designed for administrators who need:  
- Automated monitoring without constant oversight  
- Quick detection of security risks  
- Historical tracking of system changes  
- A lightweight tool that doesn’t overload your system  

AuditMate gives **visibility and peace of mind**, letting you focus on managing infrastructure instead of manually auditing it.

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
