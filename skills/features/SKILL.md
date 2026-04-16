---
name: features
description: Skill for managing advanced features on Oracle DB
---

## Usage

All scripts can be executed using Node.js. Replace `<param_name>` and `<param_value>` with actual values.

**Bash:**
`node <skill_dir>/scripts/<script_name>.js '{"<param_name>": "<param_value>"}'`

## Scripts

### enable_vector_search
Enables or configures Vector Search features (requires 23c or later).

### check_json_support
Checks the status and usage of JSON features in the database.

---
## Oracle Version Notes (19c vs 26ai)
- Baseline guidance is valid for Oracle 19c.
- **Vector Search**: Requires Oracle Database 23c or later (23ai/26ai). Not supported on 19c.

## Sources
- [Oracle Database JSON Developer's Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/adjsn/index.html)
- [Oracle Database 23c New Features](https://docs.oracle.com/en/database/oracle/oracle-database/23/nfdoc/index.html)
