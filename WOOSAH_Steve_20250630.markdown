# WOOSAH (Weekly Operations Overview: Status and Asks for Help)
**Week Ending: June 30, 2025**  
**Submitted by: Steve**  
**Department: Database Operations**

## Wins
- **Backup Reliability**: Executed full and differential backups across key instances (`DEN11SQL002`, `DEN11SQL026\DMOPSU`, `rogue1-prod-az-sqlmi`) with 100% success, covering critical databases like `DELTEKCP`, `NERVEDB`, and `Rogue1`.
- **Index Optimization**: Reorganized fragmented indexes on `Saleslogix` and `Thingworx` databases (`DEN11SQL044-D\D01`, `DEN11SQL055-T\PTCT`), reducing query latency by ~15%.
- **Security Audit**: Reviewed and updated permissions on `SSGCrowd` and `SSGJIRA` databases (`ent-app-atlassian-jira-ssg-prod-sqlmi`), removing 5 stale accounts to align with compliance standards.
- **Monitoring Enhancement**: Deployed new SQL Agent alerts on `DEN11SQL020` for `SSISDB` and `Staging` databases, improving proactive incident detection.

## Misses Near Term Deliverables Due Date
- **Maintenance Window Delay**: Planned index rebuilds for `Costpoint_Archive` (`DVWDB010`) were postponed to next week due to overlapping application testing. Rescheduled for July 5, 2025.
- **ReportServer Tuning**: Performance analysis for `ReportServer` database (`DEN11SQL028`) is behind schedule due to higher-priority backup tasks. Expected completion by July 7, 2025.

## Topics for Discussion
- **Azure SQL MI Scaling**: Exploring capacity adjustments for `rogue1-prod-az-sqlmi` to handle increased load on `Rogue1` and `TCMax` databases. Input needed on budget and timelines.
- **SQL Agent Job Standardization**: Proposing a review of SQL Agent job configurations across `DEN11SQL` instances to streamline schedules and reduce overlaps.

## Need Support, Issues, Risks, FYI
- **Need Support**: Requesting guidance on integrating third-party monitoring tools (e.g., SolarWinds) with `DEN11SQL027\ITAPPS` for better visibility into `BOE` and `DMS` performance.
- **Issue**: Intermittent latency observed in `Windchill` database queries (`DEN11SQL066-P\PTCP`). Investigating potential network or index issues; no impact to production yet.
- **Risk**: Aging hardware on `DVWDB002\D02` may impact `SwordARM` and `TCMax` database performance if not addressed in Q3. Planning hardware refresh discussion.
- **FYI**: Completed training on Azure SQL Managed Instance administration to support future migrations (e.g., `atlassian-test-az-sqlmi1`).