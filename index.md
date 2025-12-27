AuditMate — What It Does (Current State)

AuditMate is a lightweight, local system auditing tool for Linux servers and machines.
It performs security and configuration checks, tracks changes over time, and supports automated scans via cron — without requiring agents, cloud access, or subscriptions.

Core Capabilities
1. System Auditing

AuditMate collects:

Hostname, OS, kernel, uptime

Admin users and regular users

Running services

Installed package count

Open network ports

Firewall status

Available system updates

All data is collected locally.

2. Warnings & Risk Detection

AuditMate flags common security issues, including:

SSH port 22 open

Firewall inactive or disabled

Multiple admin users

Pending system updates

Warnings are clearly printed in the terminal.

3. Baseline Tracking & Change Detection

On first run, AuditMate saves a baseline snapshot

On subsequent runs, it compares the current system state against the baseline

Differences are displayed clearly (added/removed users, services, ports, etc.)

This allows users to:

Detect unexpected changes

Monitor drift over time

Validate system hardening

4. Exit Codes for Automation

AuditMate exits with meaningful codes:

0 → No warnings

1 → Non-critical warnings

2 → Critical security issues

This makes it automation-friendly for:

cron

CI/CD

monitoring scripts

5. Scheduled Scans (Cron Automation)

AuditMate includes helper scripts that let users:

Schedule scans daily, hourly, weekly, yearly, or every X minutes

Schedule multiple times per day

Use 12-hour (AM/PM) format

Preview schedules with a dry-run

View a human-readable cron summary

No cron knowledge required.

6. Licensing (Local, Offline)

AuditMate supports:

Signed license files

Offline verification using public/private key cryptography

Feature gating (e.g., JSON export for paid users)

No online checks, no tracking, no phone-home behavior.

7. Reports

Human-readable terminal output

Optional JSON report export (paid feature)

Logs saved automatically for automated runs

🎯 What AuditMate Is Designed For

Personal servers

Homelabs

Small businesses

Developers

Security-conscious admins

Environments without cloud access

🚫 What AuditMate Does NOT Do

No agents

No telemetry

No remote control

No forced updates

No SaaS dependency

🔮 Optional Future Features (Not Required)

These are nice-to-have, not necessary for v1.

Short-Term Enhancements

Configurable warning thresholds

Custom ignore rules

Severity levels per warning

Better formatted reports (Markdown / HTML)

Medium-Term

Per-server licensing (optional)

Baseline history (not just latest)

Export diffs as JSON

Web dashboard (local-only)

Long-Term / v2 Ideas

Agent mode

Centralized dashboard

Email / webhook alerts

Fleet management

Role-based access

Update channels

🧠 Bottom Line

AuditMate is:

Simple

Offline-friendly

Automation-ready

Non-intrusive

Predictable
