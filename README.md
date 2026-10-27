# SQL Monitor (beta)

**Database performance monitoring with a built-in advisor, for SQL Server, Azure SQL, PostgreSQL and MySQL.**
Free public beta. Your data never leaves your machine.

> Replace "SQL Monitor" with your product name before announcing: the name is used by an existing commercial product.

**[Download the latest beta](../../releases/latest)** &nbsp;|&nbsp; [Website](https://github.com/yvinay/SQLMonitor-Releases/) &nbsp;|&nbsp; [Send feedback](../../issues/new/choose) &nbsp;|&nbsp; [Discussions](../../discussions)

![Estate overview](docs/img/estate.png)

## What it does

- **Finds the query behind the problem**: CPU, IO, log, blocking, memory, parallelism, plan regressions, missing indexes, with the reason from the execution plan and a copy-ready fix.
- **Response time analysis**: samples active sessions every 2 seconds and shows where database time goes, by query and wait.
- **Time travel**: click any moment to see what was running and who was blocking whom.
- **Deadlocks explained**: lock graphs, recurring patterns, and how to prevent them.
- **Change correlation**: schema, setting, version and plan changes and deployment markers on every chart.
- **Health checks**: backups vs. RPO, Availability Groups, Agent jobs, CHECKDB, capacity forecasts, configuration, security, end of support.
- **Cost right-sizing**: over-provisioned elastic pools, databases, instances and VMs, with monthly savings.
- **Built for large estates**: risk-sorted view of hundreds of databases, search, pause/resume per server.

## Supported platforms

Azure SQL Database (incl. elastic pools), Azure SQL Managed Instance, SQL Server 2016 SP2+ on VMs and on-premises, Amazon RDS for SQL Server, PostgreSQL 10+ (incl. Azure and AWS), MySQL 5.7/8.x and MariaDB (incl. Azure and AWS).

## Install

1. Download `SQLMonitorSetup-<version>.exe` from [Releases](../../releases). Windows 10/11 or Server 2016+, 64-bit.
2. Optional: verify it: `Get-FileHash .\SQLMonitorSetup-<version>.exe -Algorithm SHA256` and compare with the `.sha256` file.
3. Run it. The app opens in your browser with **demo data**, so you can explore everything before connecting a server.
4. Create a read-only monitoring login with the setup scripts (Start menu > SQL Monitor > Setup scripts), then add your server under **Servers**.

SQL Server monitoring needs the Microsoft ODBC Driver 18 (the installer checks and links to it). A Docker image for a shared, multi-user installation is available on request during the beta.

## Safety and privacy

- **Read-only**: it reads monitoring views. It never changes data; fix scripts are shown for you to run yourself.
- **Your data stays with you**: metrics, settings and query text are stored locally. No telemetry. Passwords go to Windows Credential Manager.
- **Optional network use**: update check (reads this repository's release list) and AI explanations (off by default, your own Anthropic key, literals masked).
- Details: [Privacy](PRIVACY.md) &middot; [Beta terms](BETA-TERMS.md) &middot; [Security](SECURITY.md)

## Feedback shapes the roadmap

Use **Send feedback** in the app (it fills in the version for you), or:
- [Report a problem](../../issues/new?template=bug_report.yml)
- [Suggest an improvement](../../issues/new?template=feature_request.yml)
- [Vote on ideas in Discussions](../../discussions)

The source code is not public during the beta.
