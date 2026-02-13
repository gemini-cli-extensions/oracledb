# Setup
## Required Gemini CLI Version
To install this extension, the Gemini CLI version must be v0.6.0 or above. The version can be found by running: `gemini --version`.
gemini extensions install https://github.com/gemini-cli-extensions/oracledb

## Oracle Database MCP Server (Data Plane: Connecting and Querying)
This section covers connecting to a Oracle Database instance in different deployments and client configurations.

### 1. Authentication
Set the following environment variables before starting the Gemini CLI.

* `ORACLE_USER`: Your Oracle database username.
* `ORACLE_PASSWORD`: Your Oracle database password.

### 2. Connection Method
Choose **one** of the following connection methods and set the corresponding environment variables:

#### Method A: Host, Port, and Service Name
*   `ORACLE_HOST`: The hostname or IP address of your Oracle Database server.
*   `ORACLE_PORT`: The port number your Oracle Database is listening on.
*   `ORACLE_SERVICE_NAME`: The service name for the Oracle Database.

#### Method B: TNS Alias
*   `ORACLE_TNS_ALIAS`: The TNS alias of your Oracle Database from your `tnsnames.ora` file.
*   `ORACLE_TNS_ADMIN`: The path to the directory containing your `tnsnames.ora` file.

#### Method C: Direct Connection String
*   `ORACLE_CONNECTION_STRING`: The direct connection string for your Oracle Database (e.g., in EZConnect format).

### 3. Optional Configuration

#### Oracle Wallet / OCI
If you are connecting to an OCI-based database or using an Oracle Wallet:
*   `ORACLE_WALLET`: Path to the directory containing your Oracle Wallet files.
*   `ORACLE_USE_OCI`: Set to `true` to use the OCI (thick client) driver. This is typically required for wallet authentication. When using wallet authentication, the `ORACLE_TNS_ADMIN` variable should be set to the wallet directory path, and you should connect using a TNS alias.

### 4. Troubleshooting
*   **Missing Variables**: If a command fails with an error related to a missing configuration, it signifies a missing environment variable. Please review the setup instructions and ensure the necessary variables are set.
*   **Permission Errors**: If you encounter permission errors, ensure the user has the required database-level permissions. `CREATE SESSION` is required for any user to connect. For monitoring and diagnostic tools, `SELECT` privileges on various `V$` (Dynamic Performance Views) and `DBA_` (Data Dictionary Views) are often necessary.

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
When you create a new Oracle DB instance, or database using the available tools, the connection is not automatically established. You will need to perform the following steps:

1.  **(Optional) Save your conversation:** To avoid losing your progress, save the current session by running the command: `/chat save <your-tag>`
2.  **Stop the CLI:** Terminate the Gemini CLI.
3.  **Update Environment Variables:** Set or update your environment variables (e.g. `ORACLE_TNSALIAS`, `ORACLE_USER`) to point to the new resource.
4.  **Restart:** Relaunch the Gemini CLI
5.  **(Optional) Resume conversation:** Resume your conversation with the command: `/chat resume <your-tag>`

**Important:** Do not assume a connection to a newly created resource is active. Always follow the steps above to reconfigure your connection.
Instead of prompting the user for these values for specific tool calls, prompt the user to verify reuse of a specific value.
Make sure to not use the environment variable names like `ORACLE_TNSALIAS`, `${ORACLE_TNSALIAS}`, or `$ORACLE_TNSALIAS`. The value can be found by using command: `echo $ORACLE_USER`.
