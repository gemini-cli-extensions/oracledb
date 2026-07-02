# Changelog

## [0.2.5](https://github.com/gemini-cli-extensions/oracledb/compare/0.2.4...0.2.5) (2026-07-02)


### Features

* **deps:** update dependency googleapis/mcp-toolbox to v1.6.0 ([#58](https://github.com/gemini-cli-extensions/oracledb/issues/58)) ([23c7de3](https://github.com/gemini-cli-extensions/oracledb/commit/23c7de3e75419f4e5de8d0f939a8176c4eebb8c7))

## [0.2.4](https://github.com/gemini-cli-extensions/oracledb/compare/0.2.3...0.2.4) (2026-07-02)


### Features

* **auth/google:** Require audience or clientId for mcpEnabled ([mcp-toolbox#​3450](https://redirect.github.com/googleapis/mcp-toolbox/issues/3450)) ([59f7b6e](https://redirect.github.com/googleapis/mcp-toolbox/commit/59f7b6e8eaceffca042cb7e2f2b6e5e9284b6bc3)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **mcp:** Add URL parameter binding for HTTP transport ([mcp-toolbox#​3112](https://redirect.github.com/googleapis/mcp-toolbox/issues/3112)) ([0cc7b37](https://redirect.github.com/googleapis/mcp-toolbox/commit/0cc7b37b733b6a99dad5281af4024b26d730106a)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **scylladb:** Adding support for ScyllaDB source and tool ([mcp-toolbox#​3119](https://redirect.github.com/googleapis/mcp-toolbox/issues/3119)) ([2dada83](https://redirect.github.com/googleapis/mcp-toolbox/commit/2dada8306c8737e445c4f8cd3d213b72713c1834)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **server:** Add support for toolset filtering in prebuilt CLI flag ([mcp-toolbox#​3245](https://redirect.github.com/googleapis/mcp-toolbox/issues/3245)) ([7cc4f65](https://redirect.github.com/googleapis/mcp-toolbox/commit/7cc4f65a8e767e0da37cf21f0ff2568b38d32b8e)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **skills:** Generate skills offline without live source connections ([mcp-toolbox#​3388](https://redirect.github.com/googleapis/mcp-toolbox/issues/3388)) ([4c860b6](https://redirect.github.com/googleapis/mcp-toolbox/commit/4c860b66b03f0ebf86205e73cd8521ad90ccebe4)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **skills:** Tolerate missing env vars during offline skills-generate ([mcp-toolbox#​3399](https://redirect.github.com/googleapis/mcp-toolbox/issues/3399)) ([ea5d3e5](https://redirect.github.com/googleapis/mcp-toolbox/commit/ea5d3e5b9e60bf808e10d21b522954d76f7741b6)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **tools:** Decouple tool initialization from sources ([mcp-toolbox#​3355](https://redirect.github.com/googleapis/mcp-toolbox/issues/3355)) ([32a24e3](https://redirect.github.com/googleapis/mcp-toolbox/commit/32a24e35b5bf107bcf5e89af2a9b7af3740747ee)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* Enable per source level flags for sql commenter ([mcp-toolbox#​3465](https://redirect.github.com/googleapis/mcp-toolbox/issues/3465)) ([ecce6b7](https://redirect.github.com/googleapis/mcp-toolbox/commit/ecce6b7bb551b947b0951cd684cce627a4b6cf1b)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))


### Bug Fixes

* **auth/dataplex:** Fix failing source with service account credentials ([mcp-toolbox#​3369](https://redirect.github.com/googleapis/mcp-toolbox/issues/3369)) ([ba4deef](https://redirect.github.com/googleapis/mcp-toolbox/commit/ba4deef140358e5876d73d355d664f629f7aeccc)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **bigquery:** Wire maximumBytesBilled into prebuilt config ([mcp-toolbox#​3385](https://redirect.github.com/googleapis/mcp-toolbox/issues/3385)) ([4abbf6e](https://redirect.github.com/googleapis/mcp-toolbox/commit/4abbf6e82cc4af4c1903d9143337c965987475a9)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **config:** Add doc/line context to parse errors ([mcp-toolbox#​2957](https://redirect.github.com/googleapis/mcp-toolbox/issues/2957)) ([4b097da](https://redirect.github.com/googleapis/mcp-toolbox/commit/4b097daa2143817e55a9e557e8c1dea054bfc7b8)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **npm:** Source binary version from cmd/version.txt ([mcp-toolbox#​3417](https://redirect.github.com/googleapis/mcp-toolbox/issues/3417)) ([6ffbdec](https://redirect.github.com/googleapis/mcp-toolbox/commit/6ffbdecaea98db5c16dc9eeca8fb73e4bbc48102)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **prebuilt/alloydb-omni:** Require password env var explicitly ([mcp-toolbox#​3398](https://redirect.github.com/googleapis/mcp-toolbox/issues/3398)) ([fcbe3e7](https://redirect.github.com/googleapis/mcp-toolbox/commit/fcbe3e70d3d4e671e97e424187dba907d7c5b10b)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **server:** Fail if MCP auth is enabled together with enable-api ([mcp-toolbox#​3435](https://redirect.github.com/googleapis/mcp-toolbox/issues/3435)) ([a6ff910](https://redirect.github.com/googleapis/mcp-toolbox/commit/a6ff910a602adece11f0a6581d6211e5927f7182)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* **server:** Return errors instead of panicking in InitializeConfigs ([mcp-toolbox#​3397](https://redirect.github.com/googleapis/mcp-toolbox/issues/3397)) ([f48b01d](https://redirect.github.com/googleapis/mcp-toolbox/commit/f48b01dc1775e4583a06689a2e67fb06e5dd3c68)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* Bound MCP HTTP body size ([mcp-toolbox#​3216](https://redirect.github.com/googleapis/mcp-toolbox/issues/3216)) ([d4f4342](https://redirect.github.com/googleapis/mcp-toolbox/commit/d4f434251392fb597779a90a12c63d21533ea187)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))
* Escape delimiter characters in applyEscape to prevent SQL injection ([mcp-toolbox#​2811](https://redirect.github.com/googleapis/mcp-toolbox/issues/2811)) ([932519a](https://redirect.github.com/googleapis/mcp-toolbox/commit/932519a9551861bf5f18787dc43b20d06350343f)) ([d5a2625](https://github.com/gemini-cli-extensions/oracledb/commit/d5a26255c6f2ffb32b5920735512629014622693))

## [0.2.3](https://github.com/gemini-cli-extensions/oracledb/compare/0.2.2...0.2.3) (2026-06-17)


### Features

* **ci:** Add support for windows/arm64 binary distribution ([mcp-toolbox#​3231](https://redirect.github.com/googleapis/mcp-toolbox/issues/3231)) ([10abf3b](https://redirect.github.com/googleapis/mcp-toolbox/commit/10abf3b9e195a03f535e3807b7df9883899ef7c0)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))
* **datalineage:** Add Data Lineage integration ([mcp-toolbox#​3285](https://redirect.github.com/googleapis/mcp-toolbox/issues/3285)) ([19353c3](https://redirect.github.com/googleapis/mcp-toolbox/commit/19353c37e17ab1f3599cafa04337a32a7baec1c3)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))
* **server:** Ignore unknown tools at startup with `--ignore-unknown-tools` flag ([mcp-toolbox#​3353](https://redirect.github.com/googleapis/mcp-toolbox/issues/3353)) ([5f0304f](https://redirect.github.com/googleapis/mcp-toolbox/commit/5f0304f71231cce322ab2a3e458af07b392a06fc)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))


### Bug Fixes

* **auth:** Separate Google and Generic MCP OAuth verification ([mcp-toolbox#​3341](https://redirect.github.com/googleapis/mcp-toolbox/issues/3341)) ([dfd66ee](https://redirect.github.com/googleapis/mcp-toolbox/commit/dfd66ee7de6fe9750d932d30bf3b67a2f4d2a176)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))
* **auth/generic:** Enforce issuer presence in opaque token validation ([mcp-toolbox#​3360](https://redirect.github.com/googleapis/mcp-toolbox/issues/3360)) ([1d8df0d](https://redirect.github.com/googleapis/mcp-toolbox/commit/1d8df0df590383ba56091b6e4d7c37ab7d7d9749)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))
* **mcp:** Support annotations and metadata within Tools to earlier MCP schemas ([mcp-toolbox#​3300](https://redirect.github.com/googleapis/mcp-toolbox/issues/3300)) ([9a88c72](https://redirect.github.com/googleapis/mcp-toolbox/commit/9a88c72792563e4868c82a4f3be55e6af25c1477)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))
* **oracle:** Remove trailing semicolons from prebuilt tools ([mcp-toolbox#​3215](https://redirect.github.com/googleapis/mcp-toolbox/issues/3215)) ([fcad02d](https://redirect.github.com/googleapis/mcp-toolbox/commit/fcad02de73ffe9c6ecf29572f0f92674aacbe493)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))
* **server:** Return null id for batch request rejection ([mcp-toolbox#​3333](https://redirect.github.com/googleapis/mcp-toolbox/issues/3333)) ([0b18d58](https://redirect.github.com/googleapis/mcp-toolbox/commit/0b18d58aea131baceb1c70f300879de8ecdf569e)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))
* **server/auth:** Centralize tool scopes validation ([mcp-toolbox#​3335](https://redirect.github.com/googleapis/mcp-toolbox/issues/3335)) ([adce4ab](https://redirect.github.com/googleapis/mcp-toolbox/commit/adce4abb27327aae4e9736581df7a544b55c939e)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))
* **telemetry:** Allow GCP project override ([mcp-toolbox#​2960](https://redirect.github.com/googleapis/mcp-toolbox/issues/2960)) ([3c83ba5](https://redirect.github.com/googleapis/mcp-toolbox/commit/3c83ba5ab1d2ab38369e0b5c47396fabf6ecabef)) ([8a6d74a](https://github.com/gemini-cli-extensions/oracledb/commit/8a6d74a51804c5d637fe3243b407ef57c280fc96))

## [0.2.2](https://github.com/gemini-cli-extensions/oracledb/compare/0.2.1...0.2.2) (2026-06-17)


### Features

* **deps:** update dependency googleapis/mcp-toolbox to v1.3.0 ([#43](https://github.com/gemini-cli-extensions/oracledb/issues/43)) ([5623910](https://github.com/gemini-cli-extensions/oracledb/commit/56239109760fd8ea838a56c946400347467bfa6d))

## [0.2.1](https://github.com/gemini-cli-extensions/oracledb/compare/0.2.0...0.2.1) (2026-05-11)


### Features

* Add support for HTTPS/TLS listener ([mcp-toolbox#​3126](https://redirect.github.com/googleapis/mcp-toolbox/issues/3126)) ([8bc385d](https://redirect.github.com/googleapis/mcp-toolbox/commit/8bc385d7d6fd9ed2ad13503d9feb503de0b512b1)) ([c18a28b](https://github.com/gemini-cli-extensions/oracledb/commit/c18a28b47feee09332e51263e75a703fac6e1e68))


### Bug Fixes

* **mcp:** Implement router-level logger injection for MCP auth ([mcp-toolbox#​3067](https://redirect.github.com/googleapis/mcp-toolbox/issues/3067)) ([ccc7cf5](https://redirect.github.com/googleapis/mcp-toolbox/commit/ccc7cf5ee8a1bacb6b57faf41ae5a1cc3da5299e)) ([c18a28b](https://github.com/gemini-cli-extensions/oracledb/commit/c18a28b47feee09332e51263e75a703fac6e1e68))
* Allow converting string literal block with list ([mcp-toolbox#​3050](https://redirect.github.com/googleapis/mcp-toolbox/issues/3050)) ([36ab2a9](https://redirect.github.com/googleapis/mcp-toolbox/commit/36ab2a98f9f2d03c27eea389d2281bfc4581ffa1)), closes [mcp-toolbox#​3023](https://redirect.github.com/googleapis/mcp-toolbox/issues/3023) ([c18a28b](https://github.com/gemini-cli-extensions/oracledb/commit/c18a28b47feee09332e51263e75a703fac6e1e68))
* Prevent test.db from being created during unit tests ([mcp-toolbox#​3042](https://redirect.github.com/googleapis/mcp-toolbox/issues/3042)) ([d10d2ca](https://redirect.github.com/googleapis/mcp-toolbox/commit/d10d2caeb7c9eda7d17d6dbd9f63363b2bc23a7a)) ([c18a28b](https://github.com/gemini-cli-extensions/oracledb/commit/c18a28b47feee09332e51263e75a703fac6e1e68))
* Remove hardcoded \* allowed origin for sse ([mcp-toolbox#​3054](https://redirect.github.com/googleapis/mcp-toolbox/issues/3054)) ([c4c7bd9](https://redirect.github.com/googleapis/mcp-toolbox/commit/c4c7bd917e686de68e2be866cfe3872c3439efae)) ([c18a28b](https://github.com/gemini-cli-extensions/oracledb/commit/c18a28b47feee09332e51263e75a703fac6e1e68))

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
