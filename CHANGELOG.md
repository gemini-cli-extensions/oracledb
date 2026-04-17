# Changelog

## [0.2.0](https://github.com/gemini-cli-extensions/oracledb/compare/0.1.1...0.2.0) (2026-04-17)


### ⚠ BREAKING CHANGES

* add support for skills ([#30](https://github.com/gemini-cli-extensions/oracledb/issues/30))

### Features

* **skill:** Attach user agent metadata for generated skill ([mcp-toolbox#​2697](https://redirect.github.com/googleapis/mcp-toolbox/issues/2697)) ([9598a6a](https://redirect.github.com/googleapis/mcp-toolbox/commit/9598a6a32597b9c9abdb0f20c06d86a01b0d011f)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **skill:** Update skill generation logic ([mcp-toolbox#​2646](https://redirect.github.com/googleapis/mcp-toolbox/issues/2646)) ([c233eee](https://redirect.github.com/googleapis/mcp-toolbox/commit/c233eee98cd9621526cb286245f3874f5bd6e7da)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **skills:** Add Claude Code support to generated scripts ([mcp-toolbox#​2966](https://redirect.github.com/googleapis/mcp-toolbox/issues/2966)) ([a1609e1](https://redirect.github.com/googleapis/mcp-toolbox/commit/a1609e10a2eaf4ea68eae36acec3eed355b8a052)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **skills:** Add codex user agent ([mcp-toolbox#​2973](https://redirect.github.com/googleapis/mcp-toolbox/issues/2973)) ([070e939](https://redirect.github.com/googleapis/mcp-toolbox/commit/070e9399c02f088d43175ce6bf343378beb7f584)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **skills:** Tool invocation via npx ([mcp-toolbox#​2916](https://redirect.github.com/googleapis/mcp-toolbox/issues/2916)) ([377dc5b](https://redirect.github.com/googleapis/mcp-toolbox/commit/377dc5b00145a0044eef39314dd6b0ef5966fcd7)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **source/oracledb:** Add Oracle DB for MCP tools and configurations, updated tools and documentation ([mcp-toolbox#​2625](https://redirect.github.com/googleapis/mcp-toolbox/issues/2625)) ([e350fc7](https://redirect.github.com/googleapis/mcp-toolbox/commit/e350fc7879182aaf592a70c3509ed061164b3913)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* add claude code plugin config ([#32](https://github.com/gemini-cli-extensions/oracledb/issues/32)) ([97fa626](https://github.com/gemini-cli-extensions/oracledb/commit/97fa626a49b39e1faa3267bcb5f3d8ef952d052b))
* add codex plugin config ([#33](https://github.com/gemini-cli-extensions/oracledb/issues/33)) ([21485e2](https://github.com/gemini-cli-extensions/oracledb/commit/21485e2c759e4ffc4644ca3cb318cd178ca21e7f))


### Bug Fixes

* **oracle:** Enable DML operations and resolve incorrect array type error ([mcp-toolbox#​2323](https://redirect.github.com/googleapis/mcp-toolbox/issues/2323)) ([72146a4](https://redirect.github.com/googleapis/mcp-toolbox/commit/72146a4b1605bcdd3e1038106bfb1f899e677e39)) ([c66ad3c](https://github.com/gemini-cli-extensions/oracledb/commit/c66ad3cf883c3769f5aa47871fab246d03b3c5de))
* **oracle:** Normalize encoded proxy usernames in go-ora DSN ([mcp-toolbox#​2469](https://redirect.github.com/googleapis/mcp-toolbox/issues/2469)) ([b1333cd](https://redirect.github.com/googleapis/mcp-toolbox/commit/b1333cd27117655f8ab09f222721e14bea74b487)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **oracle:** Update oracle-execute-sql tool interface to match source signature ([mcp-toolbox#​2627](https://redirect.github.com/googleapis/mcp-toolbox/issues/2627)) ([81699a3](https://redirect.github.com/googleapis/mcp-toolbox/commit/81699a375b7e5af37945f4124aa4c5f2a1a9f7a6)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **skill:** Fix env variable propagation ([mcp-toolbox#​2645](https://redirect.github.com/googleapis/mcp-toolbox/issues/2645)) ([5271368](https://redirect.github.com/googleapis/mcp-toolbox/commit/52713687208994c423da64333cb0a04fb483f794)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **skills:** Fix integer parameter parsing through agent skills ([mcp-toolbox#​2847](https://redirect.github.com/googleapis/mcp-toolbox/issues/2847)) ([4564efe](https://redirect.github.com/googleapis/mcp-toolbox/commit/4564efe75436b4081d9f3d1f7c912bc64c13f850)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **skills:** Fix skill generation template ([mcp-toolbox#​2914](https://redirect.github.com/googleapis/mcp-toolbox/issues/2914)) ([a01a15e](https://redirect.github.com/googleapis/mcp-toolbox/commit/a01a15ed1aa9a83eda8362578fed2e3a3c8dde99)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))
* **skills:** Prevent empty strings overriding optional env vars in node scripts ([mcp-toolbox#​2963](https://redirect.github.com/googleapis/mcp-toolbox/issues/2963)) ([c52adeb](https://redirect.github.com/googleapis/mcp-toolbox/commit/c52adeba76fc13d0e6e415f6393def0648e478d6)) ([85518a0](https://github.com/gemini-cli-extensions/oracledb/commit/85518a012996e149156e319bfaa07daf9c42999b))


## [0.1.1](https://github.com/gemini-cli-extensions/oracledb/compare/0.1.0...0.1.1) (2026-02-19)


### Bug Fixes

* do not use Gemini CLI settings ([#11](https://github.com/gemini-cli-extensions/oracledb/issues/11)) ([3945c60](https://github.com/gemini-cli-extensions/oracledb/commit/3945c6098b589bb0fd9397b8e63193dbcedcf461))

## [0.1.0](https://github.com/gemini-cli-extensions/oracledb/compare/0.1.0...0.1.0) (2026-02-13)

### Features

* initial release for the OracleDB Gemini CLI Extension ([#1](https://github.com/gemini-cli-extensions/oracledb/issues/1)) ([7c9ef86](https://github.com/gemini-cli-extensions/oracledb/commit/7c9ef86b02313c40a2acfa4ac77164159f297524))
