# Oracle Database Agent Skills

> [!NOTE]
> Currently in beta (pre-v1.0), and may see breaking changes until the first stable release (v1.0).

This repository provides a set of agent skills to interact with [Oracle Database](https://www.oracle.com/database/) instances. These skills can be used with various AI agents, including [Gemini CLI](https://google-gemini.github.io/gemini-cli/), Claude Code, and Codex, to manage your databases, execute queries, explore schemas, and troubleshoot issues using natural language prompts.

> [!IMPORTANT]
> **We Want Your Feedback!**
> Please share your thoughts with us by filling out our feedback [form][form].
> Your input is invaluable and helps us improve the project for everyone.

[form]: https://docs.google.com/forms/d/e/1FAIpQLSfEGmLR46iipyNTgwTmIDJqzkAwDPXxbocpXpUbHXydiN1RTw/viewform?usp=pp_url&entry.157487=oracle-extension

## Table of Contents

- [Why Use Oracle Database Agent Skills?](#why-use-oracle-database-agent-skills)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Configuration](#configuration)
  - [Installation & Usage](#installation--usage)
    - [Gemini CLI](#gemini-cli)
    - [Claude Code](#claude-code)
    - [Codex](#codex)
    - [Antigravity](#antigravity)
- [Usage Examples](#usage-examples)
- [Supported Skills](#supported-skills)
- [Additional Agent Skills](#additional-agent-skills)
- [Troubleshooting](#troubleshooting)

## Why Use Oracle Database Agent Skills?

- **Seamless Workflow:** Integrates seamlessly into your AI agent's environment. No need to constantly switch contexts for common database tasks.
- **Natural Language Queries:** Stop wrestling with complex commands. Explore schemas and query data by describing what you want in plain English.
- **Full Database Insights:** Monitor active sessions, analyze query plans, and manage tablespace usage using natural language.
- **Code Generation:** Accelerate development by asking your agent to generate data classes and other code snippets based on your table schemas.

## Prerequisites

Before you begin, ensure you have the following:

- One of these AI agents installed:
  - [Gemini CLI](https://github.com/google-gemini/gemini-cli) version **v0.6.0** or higher
  - [Claude Code](https://claude.com/product/claude-code) version **v2.1.94** or higher
  - [Codex](https://developers.openai.com/codex) **v0.117.0** or higher
  - [Antigravity](https://antigravity.google) **v1.14.2** or higher
- Access to an Oracle Database instance.
- Oracle Database permissions:
  - `CREATE SESSION` for basic connectivity.
  - `SELECT` privileges on `V$` and `DBA_` views for monitoring and diagnostics.

## Getting Started

### Configuration

Please keep these settings handy during the installation process:

- `ORACLE_CONNECTION_STRING`: The connection string for your Oracle Database (e.g., `host:port/service_name` or TNS alias).
- `ORACLE_USERNAME`: Your Oracle database username.
- `ORACLE_PASSWORD`: Your Oracle database password.
- `ORACLE_WALLET`: (Optional) Path to the directory containing your Oracle Wallet files.
- `ORACLE_USE_OCI`: (Optional) Set to `true` to use the OCI (thick client) driver.

### Installation & Usage

To start interacting with your database, install the skills for your preferred AI agent, then launch the agent and use natural language to ask questions or perform tasks.

For the latest version, check the [releases page][releases].

[releases]: https://github.com/gemini-cli-extensions/oracledb/releases

<!-- {x-release-please-start-version} -->

<details open>
<summary id="gemini-cli">Gemini CLI</summary>

**1. Install the extension:**

```bash
gemini extensions install https://github.com/gemini-cli-extensions/oracledb
```

During the installation, enter your configuration settings as described in the [configuration section](#configuration).

**2. (Optional) Manage Configuration:**
To view or update your configuration in Gemini CLI:

- Terminal: `gemini extensions config oracledb [setting name] [--scope <scope>]`
- Gemini CLI: `/extensions list`

**3. Start the agent:**

```bash
gemini
```

_(Tip: Run `/extensions list` to verify your configuration and active extensions.)_

> [!WARNING]
> **Changing Database Connections**
> Currently, the database connection must be configured before starting the agent and cannot be changed during a session.
> To save and resume conversation history in Gemini CLI use command: `/chat save <tag>` and `/chat resume <tag>`.

</details>

<details>
<summary id="claude-code">Claude Code</summary>

**1. Set env vars:**
In your terminal, set your environment vars as described in the [configuration section](#configuration).

**2. Start the agent:**

```bash
claude
```

**3. Add the marketplace:**

```bash
/plugin marketplace add https://github.com/gemini-cli-extensions/oracledb.git#0.1.1
```

**4. Install the plugin:**

```bash
/plugin install oracledb@oracledb-marketplace
```

_(Tip: Run `/plugin list` inside Claude Code to verify the plugin is active, or `/reload-plugins` if you just installed it.)_

</details>

<details>
<summary id="codex">Codex</summary>

**1. Clone the Repo:**

```bash
git clone --branch 0.1.1 git@github.com:gemini-cli-extensions/oracledb.git
```

**2. Install the plugin:**

```bash
mkdir -p ~/.codex/plugins
cp -R /absolute/path/to/oracledb ~/.codex/plugins/oracledb
```

**3. Set env vars:**
Enter your environment vars as described in the [configuration section](#configuration).

**4. Create or update marketplace.json:**
`~/.agents/plugins/marketplace.json`

```json
{
  "name": "my-google-data-cloud-marketplace",
  "interface": {
    "displayName": "Google Data Cloud Skills"
  },
  "plugins": [
    {
      "name": "oracledb",
      "source": {
        "source": "local",
        "path": "./plugins/oracledb"
      },
      "policy": {
        "installation": "AVAILABLE",
        "authentication": "ON_INSTALL"
      },
      "category": "Database"
    }
  ]
}
```

_(Tip: Run `codex plugin list` or use the `/plugins` interactive menu to verify your installed plugins.)_

</details>

<details>
<summary id="antigravity">Antigravity</summary>

**1. Clone the Repo:**

```bash
git clone --branch 0.1.1 https://github.com/gemini-cli-extensions/oracledb.git
```

**2. Install the skills:**

Choose a location for the skills:
- **Global (all workspaces):** `~/.gemini/antigravity/skills/`
- **Workspace-specific:** `<workspace-root>/.agents/skills/`

Copy the skill folders from the cloned repository's `skills/` directory to your chosen location:

```bash
cp -R oracledb/skills/* ~/.gemini/antigravity/skills/
```

**3. Set env vars:**
Set your environment vars as described in the [configuration section](#configuration).

_(Tip: Antigravity automatically discovers skills in these directories at the start of a session.)_

</details>

<!-- {x-release-please-end} -->

## Usage Examples

Interact with Oracle Database using natural language:

- **Query Data:**
  - "Show me the first 10 rows from the EMPLOYEES table."
  - "What is the total salary by department?"
- **Monitor and Analyze:**
  - "List all active sessions."
  - "Explain the execution plan for this query: SELECT * FROM orders WHERE order_id = 100"
  - "What is the tablespace usage?"
- **Object Health:**
  - "List all invalid objects in the schema."

## Supported Skills

The following skills are available in this repository:

- [Oracle Database Skills](./skills/oracledb/SKILL.md) - Use these skills to manage and monitor Oracle databases by executing SQL statements, exploring schema metadata, analyzing query performance, monitoring active sessions and resource consumption, and managing storage and object health.

## Additional Agent Skills

Find additional skills to support your entire software development lifecycle at [github.com/gemini-cli-extensions](https://github.com/gemini-cli-extensions).

## Troubleshooting

Use the debug mode of your agent (e.g., `gemini --debug`) to enable debugging.

Common issues:

- "✖ Error during discovery for server: MCP error -32000: Connection closed": The database connection has not been established. Ensure your configuration is set correctly.
- "✖ MCP ERROR: Error: spawn .../toolbox ENOENT": The Toolbox binary did not download correctly. Ensure you are using the latest version of your agent.
- "cannot execute binary file": The Toolbox binary did not download correctly. Ensure the correct binary for your OS/Architecture has been downloaded.
