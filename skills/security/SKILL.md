---
name: security
description: Skill for security operations on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

## Scripts

### list_privileges
Lists privileges granted to a specific user or role.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| grantee | string | The user or role to list privileges for. | Yes |

### check_audit_status
Checks the status of database auditing features.

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.

## Sources
- [Oracle Database Security Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/dbseg/index.html)
