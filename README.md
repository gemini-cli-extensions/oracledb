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

You will be prompted to configure the following settings during installation. These settings are saved in an `.env` file within the extension's directory.

*   `ORACLE_CONNECTION_STRING`: The connection string for your Oracle database.
*   `ORACLE_USER`: The database username.
*   `ORACLE_PASSWORD`: The password for the database user.
*   `ORACLE_USE_OCI`: (Optional) Set to `true` or `false`. Indicates if your Oracle instance is deployed in cloud.
*   `ORACLE_WALLET`: (Optional) Your Oracle wallet location (for cloud-based deployments using Wallet authentication).

To view or update your configuration:

**List Settings:**
*   Terminal: `gemini extensions list`
*   Gemini CLI: `/extensions list`

**Update Settings:**
*   Terminal: `gemini extensions config oracledb [setting name] [--scope <scope>]`
    *   `setting name`: (Optional) The single setting to configure.
    *   `scope`: (Optional) The scope of the setting in (`user` or `workspace`). Defaults to `user`.
*   Currently, you must restart the Gemini CLI for changes to take effect. We recommend using `gemini --resume` to resume your session.

Alternatively, you can manually set these environment variables before starting the Gemini CLI:

```bash
export ORACLE_CONNECTION_STRING="<your-oracle-connection-string>"
export ORACLE_USER="<your-oracle-sql-user>"
export ORACLE_PASSWORD="<your-oracle-sql-password>"
export ORACLE_USE_OCI="true" # Optional
export ORACLE_WALLET="your-oracle-wallet-location" # Optional
``` 

> [!NOTE]
> * If you run the Oracle DB instance in a cloud deployment model using private IPs, you must run Gemini CLI in the same Virtual Private Cloud (VPC) network.
> * See [Troubleshooting](#troubleshooting) for debugging your configuration.

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
* "cannot execute binary file": The Toolbox binary did not download correctly. Ensure the correct binary for your OS/Architecture has been downloaded. See [Installing the server](https://googleapis.github.io/genai-toolbox/getting-started/introduction/#installing-the-server) for more information.