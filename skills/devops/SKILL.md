---
name: devops

description: Skill for DevOps, SQL, and PL/SQL development and operations on Oracle DB
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

### compile_package
Compiles a PL/SQL package.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| package_name | string | The name of the package to compile. | Yes |

### trace_session
Enables tracing for a specific session.
#### Parameters
| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| sid | number | Session ID to trace. | Yes |

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.

## Sources
- [Oracle Database SQL Language Reference](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/index.html)
- [Oracle Database PL/SQL Packages and Types Reference](https://docs.oracle.com/en/database/oracle/oracle-database/19/arpls/index.html)
- [Oracle Database Administrator's Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/index.html)
