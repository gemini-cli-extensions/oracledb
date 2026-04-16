---
name: monitoring
description: Skill for monitoring operations on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

## Scripts

### check_alert_log
Checks the database alert log for errors or specific patterns.

### list_wait_events
Lists top wait events in the database to identify bottlenecks.

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.

## Sources
- [Oracle Database Administrator's Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/index.html)
