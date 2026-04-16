---
name: plsql
description: Skill for PL/SQL development and debugging operations on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

## Scripts

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
- [Oracle Database PL/SQL Packages and Types Reference](https://docs.oracle.com/en/database/oracle/oracle-database/19/arpls/index.html)
