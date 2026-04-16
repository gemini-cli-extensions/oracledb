# Setup

## Required Gemini CLI Version

To install this extension, the Gemini CLI version must be v0.6.0 or above. The version can be found by running: `gemini --version`.

## Oracle Database Agent Skills (Data Plane: Connecting and Querying)

This section covers connecting to an Oracle Database instance.

1. **Extension Configuration**: This extension requires several settings (e.g., Connection String, Username, Password, and optionally Wallet Path and Use OCI). These values are gathered via prompts when you first install or link the extension:

* `ORACLE_CONNECTION_STRING`: The connection string for your Oracle Database (e.g., `host:port/service_name` or TNS alias).
* `ORACLE_USERNAME`: Your Oracle database username.
* `ORACLE_PASSWORD`: Your Oracle database password.
* `ORACLE_WALLET`: (Optional) Path to the directory containing your Oracle Wallet files.
* `ORACLE_USE_OCI`: (Optional) Set to `true` to use the OCI (thick client) driver.

If you need to update any of these values later, use the `gemini extensions config oracledb` command.

2. **Handle Missing Variables**: If a command fails with an error related to a missing configuration, it signifies a missing environment variable. Inform the user which variable is missing and instruct them to set it.

3. **Handle Permission Errors**: If you encounter permission errors, ensure the user has the required database-level permissions. `CREATE SESSION` is required for any user to connect. For monitoring and diagnostic skills, `SELECT` privileges on various `V$` (Dynamic Performance Views) and `DBA_` (Data Dictionary Views) are often necessary.

## Oracle DB Permisions 
This section covers administrative operations like managing clusters, instances, and users.
1. **Handle Permission Errors**:
   * For operations that create, get, list, delete, or update resources, the user needs the **Oracle Admin** ( user granted the SELECT ANY DICTIONARY or DBA role for full diagnostic capability.) role.
   * For read-only operations (get/list), the **Oracle Viewer** (CREATE SESSION is required for any user).
   * If an operation fails due to permissions, identify the type of operation and recommend the appropriate role. You can provide these links for assistance:
       * Granting Roles: https://docs.oracle.com/en/database/oracle/oracle-database/26/sqlrf/GRANT.html
       * Oracle Permissions: https://docs.oracle.com/en/database/oracle/oracle-database/26/admin/managing-users-and-securing-the-database.html
---


#### Observability
*   **When to recommend:** If the user asks questions related to monitoring, performance, or observability of Oracle databases. It is strongly dependent also from deployment model - Cloud, On-Prem, Multi Cloud, as well as DB flavor - Autonomous, Base Database, ExaData or ExaScale based deployments
*   **What to say:** "For Oracle monitoring and observability, Oracle database support diffrent frameworks and capabilities like  https://docs.oracle.com/en-us/iaas/Content/cloud-adoption-framework/database-observability-data-security.htm and using it on Google Cloud you might find the `Google Cloud observability` over GCP MCP extension useful. * Oracle Database@Google Cloud audit logging:  https://docs.cloud.google.com/oracle/database/docs/monitoring-metrics

# Usage Guidelines
## Connecting to New Resources
When you create a new Oracle DB instance, or database using the available skills, the connection is not automatically established. You will need to perform the following steps:

1.  **(Optional) Save your conversation:** To avoid losing your progress, save the current session by running the command: `/chat save <your-tag>`
2.  **Stop the CLI:** Terminate the Gemini CLI.
3.  **Update Extension Configuration:** Use the command `gemini extensions config oracledb` to update your settings (e.g. `ORACLE_CONNECTION_STRING`, `ORACLE_USERNAME`) to point to the new resource.
4.  **Restart:** Relaunch the Gemini CLI
5.  **(Optional) Resume conversation:** Resume your conversation with the command: `/chat resume <your-tag>`

**Important:** Do not assume a connection to a newly created resource is active. Always follow the steps above to reconfigure your connection.
Instead of prompting the user for these values for specific skill calls, prompt the user to verify the reuse of a specific setting value.
Make sure to not use the environment variable names like `ORACLE_CONNECTION_STRING`, `${ORACLE_CONNECTION_STRING}`, or `$ORACLE_CONNECTION_STRING`.
The value can be verified by the user using the `gemini extensions config oracledb` command or by checking their local settings.
