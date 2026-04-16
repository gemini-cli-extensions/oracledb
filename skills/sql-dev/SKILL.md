---
name: sql-dev
description: Skill for SQL development operations on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

## Scripts

### format_sql
Formats a SQL statement according to standard rules.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| sql_text | string | The SQL text to format. | Yes |

### explain_plan
Generates an execution plan for a SQL statement.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| query | string | The SQL statement for which you want to generate plan. | Yes |

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.

## Sources
- [Oracle Database SQL Language Reference](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/index.html)
