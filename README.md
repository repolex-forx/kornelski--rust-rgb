# Repolex Knowledge Graph of kornelski/rust-rgb

RDF knowledge graph data for [kornelski/rust-rgb](https://github.com/kornelski/rust-rgb), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download kornelski/rust-rgb
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 10d080dc228b3a5e1db8933af02fd0a4c391c902
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 10d080dc228b3a5e1db8933af02fd0a4c391c902.nq.gz
│   └── repolex
│       └── 10d080dc228b3a5e1db8933af02fd0a4c391c902
│           └── chunk-001.nq.gz
├── blob
│   ├── 01c71a16eb7a749dfa8cb11246ff5f8e42fd47e6.nq.gz
│   ├── 06c808925a879896bc9d03efc35c17580dc8fee6.nq.gz
│   ├── 0e20355914162048531ae7e1200a56cf3126a386.nq.gz
│   ├── 0fa356c3e24b6264679282b6477c76a95108fc52.nq.gz
│   ├── 139ace5698e594e1b14b0ebed28c7a5a5ca89629.nq.gz
│   ├── 22761ba7ee19a94703411264d274ae1da1d326ff.nq.gz
│   ├── 244421d246878bb7fe93fcf8dfc028700bea51bd.nq.gz
│   ├── 24c4abaab0d9213042fe16e70936db2a1d16a4f1.nq.gz
│   ├── 2e28ba28da6327cfe7472e9d51707d532c9b2b61.nq.gz
│   ├── 3608f6176c576d43065455f53cbca6f337d2e291.nq.gz
│   ├── 4868d7b050363817376ff38a97545cb364cc7b09.nq.gz
│   ├── 53457514ae2b1cf0635c82ec02572ce2762ea0b0.nq.gz
│   ├── 5919c4077dab1eff082933d7140cd2baf67e352e.nq.gz
│   ├── 60b7c68905843344a592d3d373938593def69a98.nq.gz
│   ├── 68defcbf633df33a945e6d4f0dd197ef3fb81336.nq.gz
│   ├── 7284a149d2f7683c7bd7f9142dfe023a2c2084e9.nq.gz
│   ├── 787d60e93daa80df598de7e6ec0a2a812630f544.nq.gz
│   ├── 84f9466af9c10f8e4905b15908c074975e49c1f5.nq.gz
│   ├── 8fd20ca46ab563912b3386e636e96b9612d1c0f4.nq.gz
│   ├── 91641c29230b5ade1be4eb5e14313215c1edc22c.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── aea3f4c07dfdc536df504d5bf6c0301a00266df9.nq.gz
│   ├── b0e0c054d33a2e815458cb7588295d3f669c4c51.nq.gz
│   ├── c591b3dff5ea2e1d22a5150fa2fe7d5f0391f44b.nq.gz
│   ├── c5da70f616941b6f18bbd429377045781a88c2db.nq.gz
│   ├── c9df9e084ecf559d3c761641ced14d6d571fb350.nq.gz
│   ├── d09005e96d12fd6a955048d2e1df59f279cad8c5.nq.gz
│   ├── d168e754689cca762475e713bfe7be9fd2721d15.nq.gz
│   ├── d6ce5f0dde00da6663e9004fd87248cf10364497.nq.gz
│   ├── dca8493e66ec7dd0af558c240a855fedf32aa02c.nq.gz
│   ├── e3f2dbe717b4fe0c0b5b3fe1ecd3be730b0dcc00.nq.gz
│   └── fbf8c7430a54429937ba3ad034952cbb00a276b6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 10d080dc228b3a5e1db8933af02fd0a4c391c902.nq.gz
├── filetree
│   └── 10d080dc228b3a5e1db8933af02fd0a4c391c902.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 42 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[kornelski/rust-rgb](https://github.com/kornelski/rust-rgb)

---
*Parsed on 2026-11-23 by [repolex](https://repolex.ai)*
