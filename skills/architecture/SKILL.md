---
name: architecture
description: Skill for database architecture operations on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

## Scripts

### check_ha_status
Checks the High Availability status (Data Guard, RAC, etc.).

### list_nodes
Lists cluster nodes in a RAC environment.

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.

## Sources
- [Oracle Database High Availability Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/high-availability.html)
