# Setup
## Required Gemini CLI Version
To install this extension, the Gemini CLI version must be v0.6.0 or above. The version can be found by running: `gemini --version`.
gemini extensions install https://github.com/gemini-cli-extensions/oracledb

## Oracle Database MCP Server (Data Plane: Connecting and Querying)
This section covers connecting to a Oracle Database instance in different deployments  and client configurations.
1. **Verify Environment Variables**: The extension requires the following environment variables to be set before the Gemini CLI is started:
   * `ORACLE_CONNECTION_STRING`: The Oracle Connection String .
   * `ORACLE_USER`: The reguser ion of your Oracle instance.
   * `ORACLE_PASSWORD`: The Password of your Oracle instance.

2. **Handle Missing Variables**: If a command fails with an error message containing a placeholder like `$`, it signifies a missing environment variable. Inform the user which variable is missing and instruct them to set it.

3. **Handle Permission Errors**: If you encounter permission errors, ensure the user has the **Oracle SQL Client** role and the correct database-level permissions.
Connect Permission: CREATE SESSION is required for any user.
Monitoring Permissions: Generally, SELECT on various V$ (Dynamic Performance Views) and DBA_ (Data Dictionary Views) views is required (e.g., V$SESSION, V$SQL, DBA_TABLES).

## Oracle SQL Admin MCP Server (Control Plane: Creating and Managing Infrastructure)
This section covers administrative operations like managing clusters, instances, and users.
1. **Handle Permission Errors**:
   * For operations that create, get, list, delete, or update resources, the user needs the **Oracle Admin** ( user granted the SELECT ANY DICTIONARY or DBA role for full diagnostic capability.) role.
   * For read-only operations (get/list), the **Oracle Viewer** (CREATE SESSION is required for any user).
   * If an operation fails due to permissions, identify the type of operation and recommend the appropriate role. You can provide these links for assistance:
       * Granting Roles: https://docs.oracle.com/en/database/oracle/oracle-database/26/sqlrf/GRANT.html
       * Oracle Permissions: https://docs.oracle.com/en/database/oracle/oracle-database/26/admin/managing-users-and-securing-the-database.html
---
# Additional Tools
This section provides context on additional tools that can be recommended to the user based on their queries.
*   **execute_sql**  - Executes any single SQL query or DML statement.
*   **list_tables**  - Lists tables and their segment information (size, row count).
*   **list_active_sessions**  - Lists currently active sessions and their executing SQL.
*   **get_query_plan**  - Generates the execution plan for a specified SQL ID or SQL text.
*   **list_top_sql_by_resource**  - Lists top SQL statements by CPU, I/O, or total elapsed time from V$SQL.
*   **list_tablespace_usage**  -Lists the utilization and free space for all tablespaces.
*   **list_invalid_objects**  - Lists all database objects (indexes, procedures, views) that are currently in an INVALID status.

#### Observability
*   **When to recommend:** If the user asks questions related to monitoring, performance, or observability of Oracle databases. It is strongly dependent also from deployment model - Cloud, On-Prem, Multi Cloud, as well as DB flavor - Autonomous, Base Database, ExaData or ExaScale based deployments
*   **What to say:** "For Oracle monitoring and observability, you might find the `Google Cloud observability` over GCP MCP extension useful. * Oracle Database@Google Cloud audit logging:  https://docs.cloud.google.com/oracle/database/docs/monitoring-metrics
---
# Usage Guidelines
## Connecting to New Resources
When you create a new Oracle DB instance, or database using the available tools, the connection is not automatically established. You will need to perform the following steps:

1.  **(Optional) Save your conversation:** To avoid losing your progress, save the current session by running the command: `/chat save <your-tag>`
2.  **Stop the CLI:** Terminate the Gemini CLI.
3.  **Update Environment Variables:** Set or update your environment variables (e.g. `ORACLE_TNSALIAS`, `ORACLE_USER`) to point to the new resource.
4.  **Restart:** Relaunch the Gemini CLI
5.  **(Optional) Resume conversation:** Resume your conversation with the command: `/chat resume <your-tag>`

**Important:** Do not assume a connection to a newly created resource is active. Always follow the steps above to reconfigure your connection.
Instead of prompting the user for these values for specific tool calls, prompt the user to verify reuse of a specific value.
Make sure to not use the environment variable names like `ORACLE_TNSALIAS`, `${ORACLE_TNSALIAS}`, or `$ORACLE_TNSALIAS`. The value can be found by using command: `echo $ORACLE_USER`.
