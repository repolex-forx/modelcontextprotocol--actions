# Repolex Knowledge Graph of modelcontextprotocol/actions

RDF knowledge graph data for [modelcontextprotocol/actions](https://github.com/modelcontextprotocol/actions), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/actions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2c9cb4f4db3d54f0fa17d3232ec93c0b56facb1c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2c9cb4f4db3d54f0fa17d3232ec93c0b56facb1c
│           └── chunk-001.nq.gz
├── blob
│   ├── 09042beff2d7c896be4c4681e9be7995b2992f76.nq.gz
│   ├── 2514e012702ec77467613e0d575c5adcf0a9ace9.nq.gz
│   ├── 2aa87fee9e3f24e9cbd87295d888a0e2fe292d46.nq.gz
│   ├── 2acd70eea1ebcf74e2a60ffe3d0f561a5ca5150f.nq.gz
│   ├── 2b6cf97228307c8cf6da703abf78fe40af817c65.nq.gz
│   ├── 3271ac5a4f88396ca5801a32ab4485bf2d3a6073.nq.gz
│   ├── 538e8e539ce17ea0262630145e79411e628b28eb.nq.gz
│   ├── 7b6ee84552fedf02704cc1d379ff77f4c9846523.nq.gz
│   ├── 7fd2ace0f7c1e564111d6f1ccaae04238ad07416.nq.gz
│   ├── 9a5acedff56aee2e6731a444d283bf6071c49bcc.nq.gz
│   ├── a95186135b56d03af564f3c4a3a39f2ad4798e3e.nq.gz
│   ├── ab0be58a830f64617e9d8f76d40805f8cd124b74.nq.gz
│   ├── b42bec889e1f5188df6f33efc52960e330ce853c.nq.gz
│   └── d8c8ce66041cd8db9c849047bc8774c6c12f345a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2c9cb4f4db3d54f0fa17d3232ec93c0b56facb1c.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 21 files
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

[modelcontextprotocol/actions](https://github.com/modelcontextprotocol/actions)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
