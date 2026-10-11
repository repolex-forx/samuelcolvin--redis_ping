# Repolex Knowledge Graph of samuelcolvin/redis_ping

RDF knowledge graph data for [samuelcolvin/redis_ping](https://github.com/samuelcolvin/redis_ping), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/redis_ping
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── eaae9c32eca5584e2e6da40afb260c2143c5577c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── eaae9c32eca5584e2e6da40afb260c2143c5577c
│           └── chunk-001.nq.gz
├── blob
│   ├── 3ed142511a212fe0f9af09022a60b77a7b3cde32.nq.gz
│   ├── 7bed982e04d4efbc27382b5b610d7767923bac6d.nq.gz
│   ├── cfdbb6eec53b0e3aad02438ec8587bca11c54f51.nq.gz
│   └── ea8c4bf7f35f6f77f75d92ad8ce8349f6e81ddba.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── eaae9c32eca5584e2e6da40afb260c2143c5577c.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 10 files
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

[samuelcolvin/redis_ping](https://github.com/samuelcolvin/redis_ping)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
