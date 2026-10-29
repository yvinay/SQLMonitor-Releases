# Changelog

## 3.3.0-beta.1
The biggest update since the first public beta.

**Reports (new Reports page, run on request)**
- Indexes: unused (with the observation window), duplicate and overlapping (removal script with rollback), missing, and costly-but-rarely-read indexes. SQL Server, PostgreSQL and MySQL.
- Index usage by query: which statements seek, scan, look up or update each index, from cached and Query Store plans.
- Parameter sniffing: compiled parameter values compared with the column histogram, runtime spread, ranked fixes.
- Client timeouts (attention events) with the likely cause; chatty queries; connection churn.
- Inventory: server, database or whole estate, as a graphical HTML report or an Excel workbook.

**Inventory details**
- Every database's compatibility level and the release it behaves like; databases below 130 flagged.
- Azure SQL Database: edition, service objective, vCore/DTU, hardware generation (Gen4 flagged), elastic pools, limits, geo-replicas, automatic tuning.
- Azure SQL Managed Instance: backups treated as Azure-managed.

**Sessions and blocking**
- User, machine, IP address, application and status (Running, Runnable, Suspended, Sleeping) wherever queries are listed: Queries, database page, Locks, Response time, Time travel, Advisor and Reports.
- Sleeping sessions with an open transaction are shown and covered by the Advisor on SQL Server.
- Top queries remember who ran them.
- Live blocking keeps chains whole when the head blocker is connected to another database; special blockers (orphaned distributed transactions, latches) are explained.
- Blocking history: periods up to your retention setting, paging to older incidents, the full chain of every incident, filter.

**Team server and security**
- Server mode with a setup script for Windows Server and IIS: HTTPS at your own address, background service, sign-in for everyone.
- Roles, temporary passwords changed at first sign-in, sign-out on browser close and after 30 idle minutes, audit log.
- Until sign-in is on, only requests from the computer it runs on are answered.
- Cross-site request protection, trusted-proxy single sign-on, named and hashed API tokens, sign-in throttling, encrypted saved passwords with a separate key, least-privilege msdb permissions.

**Fixes**
- Leftover "Ongoing" blocking incidents after a restart are closed.

## 3.2.0-beta.1
First public beta.
- Estate overview for hundreds of databases, search, pause/resume
- Performance advisor with execution plan analysis and fix scripts
- Response time (wait sampling), time travel, change correlation, baselines
- Locks & deadlocks, queries, health checks, cost right-sizing
- SQL Server family, PostgreSQL, MySQL/MariaDB
- In-app feedback, update check, beta terms
