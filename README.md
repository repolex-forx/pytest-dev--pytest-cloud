# Repolex Knowledge Graph of pytest-dev/pytest-cloud

RDF knowledge graph data for [pytest-dev/pytest-cloud](https://github.com/pytest-dev/pytest-cloud), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-cloud
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d4409d69af7d8a0691d09395cc897773429089db
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d4409d69af7d8a0691d09395cc897773429089db
│           └── chunk-001.nq.gz
├── blob
│   ├── 000ad0b3b7a6c234c066393eddc748f703f22dbb.nq.gz
│   ├── 209eef43f42477b96af0d0321c2657003aae34b1.nq.gz
│   ├── 30462d56b797b9f9c1ba7d7b4da9ec35b1d38d2d.nq.gz
│   ├── 63f227d90d83745acd5ceb478e50648f09a910fe.nq.gz
│   ├── 6f38b05bd47cd3f335f6546f2e4abbc13bcb3878.nq.gz
│   ├── 7543ab195e14353f25b1ed8d3342442797b9d24d.nq.gz
│   ├── 760e3e99f92075d802d42727770dbcad876cf79e.nq.gz
│   ├── 7a5b6ecfffb01bcf9c4d32759c82543624d06ac9.nq.gz
│   ├── 86745d053ea70672e6e41fa54cdcadca11cda9b4.nq.gz
│   ├── 9166873b52741bb8511c5ec40c3da65f4cba3853.nq.gz
│   ├── 93203c4f5a439f17276d3aa2a25d804414960f69.nq.gz
│   ├── 9f156be4325b5a496538f162180bd611bbba4e25.nq.gz
│   ├── a851a04ec87d5b0c29c01e1b5a0f45a0fce4c628.nq.gz
│   ├── bf04c589c402601ce130a5b95d9a5ae413b47e2b.nq.gz
│   ├── c3f263973181e259a9ad8b19acea81f868b55d6a.nq.gz
│   ├── c712d2595247bf32129c8609dcf822e238412a20.nq.gz
│   ├── cb8f2f657b4977c025a6b381a3bd678819e5888e.nq.gz
│   ├── d0d434f0756da77e14f42057eadacb4efaea345c.nq.gz
│   ├── d1b0b7b92ea4b6e12b60c0538ce87bf20598ad6d.nq.gz
│   ├── d420712d8bbf0195c02e3317e4395b2c2ffeacf6.nq.gz
│   ├── d4fe28579cbfc45195d3ef00174007074d7b5a47.nq.gz
│   ├── ea6d2500cf538cc53b9ecbce585ea116f978a7c8.nq.gz
│   └── eb35d1acb5477c9e2ad297d7a1f19f8096d287f1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d4409d69af7d8a0691d09395cc897773429089db.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[pytest-dev/pytest-cloud](https://github.com/pytest-dev/pytest-cloud)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
