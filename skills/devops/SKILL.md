---
name: devops
description: Skill for DevOps operations on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

## Scripts

### run_migration
Runs a database migration script.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| script_path | string | Path to the migration script. | Yes |

### check_deployment_status
Checks the status of the last deployment.

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.

## Sources
- [Oracle Database Administrator's Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/index.html)
