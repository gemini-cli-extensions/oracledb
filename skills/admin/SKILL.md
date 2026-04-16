---
name: admin
description: Skill for performing administrative operations on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

**PowerShell:**
`node <skill_dir>/scripts/<script_name>.js '{\"<param_name>\": \"<param_value>\"}'`

## Scripts

### backup_database
Initiates a backup using RMAN or a wrapper script.

### create_user
Creates a new database user.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| username | string | The username to create. | Yes |
| password | string | The password for the user. | Yes |

### drop_user
Drops a database user.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| username | string | The username to drop. | Yes |

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.
- 23ai/26ai features like schema privileges or new security defaults should be handled conditionally if scripts are expanded.

## Sources
- [Oracle Database Administrator's Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/index.html)
