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


### execute_sql

Executes any SQL statement.

---

### list_tables

Lists all user tables in the connected schema, including segment size, row count, and last analyzed date. Filters by a comma-separated list of names. If names are omitted, lists all tables in the current user's schema.

---

### list_active_sessions

List the top N (default 50) currently running database sessions (STATUS='ACTIVE'), showing SID, OS User, Program, and the current SQL statement text.

---

### get_query_plan

Generate a full execution plan for a single SQL statement using EXPLAIN PLAN. This can be used to analyze query performance without execution. Requires the SQL statement as input as a parameter.

#### Parameters

| Name | Type | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| query | string | The SQL statement for which you want to generate plan (omit the EXPLAIN keyword). | Yes | |

---

### list_top_sql_by_resource

List the top N (default 5) SQL statements from the library cache based on a chosen resource metric (CPU, I/O, or Elapsed Time). Shows SQL ID, execution count, buffer gets, disk reads, CPU time, and elapsed time.

---

### list_tablespace_usage

List tablespace names, total size, free space, and used percentage to monitor storage utilization.

---

### list_invalid_objects

Lists all database objects that are in an invalid state, requiring recompilation (e.g., procedures, functions, views).

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.

## Sources
- [Oracle Database Administrator's Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/index.html)
