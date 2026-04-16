---
name: performance
description: Skill for performance tuning operations on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

## Scripts

### analyze_table
Gathers statistics for a specific table.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| table_name | string | The name of the table to analyze. | Yes |

### flush_shared_pool
Flushes the shared pool (use with caution in production).

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.

## Sources
- [Oracle Database SQL Tuning Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/tgsql/index.html)
