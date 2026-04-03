# Gemini CLI Extension - Oracle Database

> [!NOTE]
> This extension is currently in beta (pre-v1.0), and may see breaking changes until the first stable release (v1.0).

Developers and Engineers can effortlessly connect, interact, and generate data insights with [OracleDB](https://www.oracle.com/database/) datasets and data using natural language commands.

Learn more about [Gemini CLI Extensions](https://github.com/google-gemini/gemini-cli/blob/main/docs/extensions/index.md).
> [!IMPORTANT]
> **We Want Your Feedback!**
> Please share your thoughts with us by filling out our feedback [form][form]. 
> Your input is invaluable and helps us improve the project for everyone.

[form]: https://docs.google.com/forms/d/e/1FAIpQLSfEGmLR46iipyNTgwTmIDJqzkAwDPXxbocpXpUbHXydiN1RTw/viewform?usp=pp_url&entry.157487=oracle-extension

## Why Use the Oracle DB Extension?

* **Natural Language to enteprise data  :** Find required Oracle tables and ask transactional or analytical questions in natural language.
* **Seamless Workflow:** Stay in your CLI. No need to constantly switch contexts to the oracle database admin console for connecting and generating  insights.
* **Run advanced sql queries :** Connect to enterprise data, Generate vectors and embedings, run sql specific queries using built-in advanced tools.

# Prerequisites

Before you begin, ensure you have the following:

* [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed with version **+v0.6.0**.
* Setup Gemini CLI [Authentication](https://github.com/google-gemini/gemini-cli/tree/main?tab=readme-ov-file#-authentication-options).

## Getting Started

### Installation

To install the extension, use the command:

```bash
gemini extensions install https://github.com/gemini-cli-extensions/oracledb
```

### Configuration

Set the following environment variables before starting the Gemini CLI. These variables can be loaded from a `.env` file.
```bash
export ORACLE_USER="<your-oracle-sql-user>"
export ORACLE_PASSWORD="<your-oracle-sql-password>"
```

Then you need to choose one of the following connection methods:

1. Host, Port, and Service Name
```bash
export ORACLE_HOST="<your-oracle-host>"
export ORACLE_PORT="<your-oracle-port>"
export ORACLE_SERVICE_NAME="<your-oracle-service-name>"
```

2. TNS Alias
```bash
export ORACLE_TNS_ALIAS="<the tns alias of your oracle database>"
export ORACLE_TNS_ADMIN="<the path to the TNS directory>"
```

3. Direct Connection String
```bash
export ORACLE_CONNECTION_STRING="<the connection string of your oracle database>"
```

#### Oracle Wallet / OCI databases

If you wish to use the Oracle Wallet, you can configure the following variable:

```bash
export ORACLE_WALLET="/path/to/my/wallet/directory"
```

Example:

```bash
export ORACLE_CONNECTION_STRING="127.0.0.1:1521/XEPDB1"
export ORACLE_USER="myuser"
export ORACLE_PASSWORD="mypassword"
export ORACLE_TNS_ALIAS="SECURE_DB_ALIAS"
export ORACLE_WALLET="/path/to/my/wallet/directory"
```

For OCI-based databases, the wallet authentication is triggered by setting tnsAdmin to the wallet directory and connecting via a tnsAlias.
You need to specify the following variable:

```bash
export ORACLE_USE_OCI=true
```

### Start Gemini CLI

To start the Gemini CLI, use the following command:

```bash
gemini
```

> [!WARNING]
> **Changing Instance & Database Connections**
> Currently, the database connection must be configured before starting the Gemini CLI and can not be changed during a session.
> To save and resume conversation history use command: `/chat save <tag>` and `/chat resume <tag>`.

## Usage Examples

Interact with Oracle using natural language:
 "List the top N SQL statements from the library cache based on a chosen resource metric (CPU, I/O, or Elapsed Time), following is an example of the sql" 

## Supported Tools
This extension provides a comprehensive set of tools:

*   `execute_sql`: Use this tool to execute any SQL statement.
*   `list_active_sessions`: Lists active database sessions.  
*   `get_query_plan`: Gets the execution plan for a SQL statement.  
*   `list_top_sql_by_resource`: Lists top SQL statements by resource usage.  
*   `list_tablespace_usage`: Lists tablespace usage.  
*   `list_invalid_objects`: Lists invalid objects.  

## Additional Extensions

Find additional extensions to support your entire software development lifecycle at [github.com/gemini-cli-extensions](https://github.com/gemini-cli-extensions)

## Troubleshooting

Use `gemini --debug` to enable debugging.

Common issues:

* "✖ Error during discovery for server: MCP error -32000: Connection closed": The database connection has not been established. Ensure your configuration is set via environment variables.
* "✖ MCP ERROR: Error: spawn /Users/USER/.gemini/extensions/oracle/toolbox ENOENT": The Toolbox binary did not download correctly. Ensure you are using Gemini CLI v0.6.0+.
* "cannot execute binary file": The Toolbox binary did not download correctly. Ensure the correct binary for your OS/Architecture has been downloaded. See [Installing the server](https://mcp-toolbox.dev/documentation/introduction/#install-toolbox) for more information.