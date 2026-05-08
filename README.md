# Repolex Knowledge Graph of open-source-cooperative/keyring-rs

RDF knowledge graph data for [open-source-cooperative/keyring-rs](https://github.com/open-source-cooperative/keyring-rs), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download open-source-cooperative/keyring-rs
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5.nq.gz
│   └── repolex
│       └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5
│           └── chunk-001.nq.gz
├── blob
│   ├── 335cad39bc42fbb1ca9013edc5cfe6f2bb47bbc8.nq.gz
│   ├── 45e373efbc61f4d2828565d192382671565b010d.nq.gz
│   ├── 47f6e38f542232e602b77a4c61d86621b3ba8684.nq.gz
│   ├── 70e126cb17be6d49800fa746fd35d73e6292363c.nq.gz
│   ├── 7e554dcb6083b16c4d76210d874ff5da45e1d40f.nq.gz
│   ├── 86930176b3ec3f72c9219dccd180bfdf6cdae5ce.nq.gz
│   ├── 87d92c8c24e0e39e90e7ee8f859fb2a6ec751c28.nq.gz
│   ├── 89fd204f31e0bd1217e17d75bfda6ba7ebed6efc.nq.gz
│   ├── 8be4771b227a66d5c043ee52c08c64d4edda9674.nq.gz
│   ├── 8f9ddb68a1673f0aee48cedc83211fe1362b0115.nq.gz
│   ├── 8fff472decde25d9d0ab453ac52d506137c31dc1.nq.gz
│   ├── 91cc7f771d573437eb5ac431eac20009f3284ac1.nq.gz
│   ├── ac3c5605d45b8f568fd575fc3f85e67b507c2a2a.nq.gz
│   ├── b277f0fe2e381963699ce05f130d76b3ead100a6.nq.gz
│   ├── c32f440ba5ca5030d7893c150d4b8206b729995d.nq.gz
│   ├── c5cb2181858ae5994056ef2bf01fb384911c1a3a.nq.gz
│   ├── d9db0484184ba6aef1aaecbff5a05a50255f2635.nq.gz
│   ├── de779e302cbb0142fb90d3e7c26819d1647ca2fc.nq.gz
│   └── f54eefd2e0c52f8fd7c590781239daf304e2f1ed.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5.nq.gz
├── filetree
│   └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 29 files
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

## Source repository

[open-source-cooperative/keyring-rs](https://github.com/open-source-cooperative/keyring-rs)

---
*Parsed on 2026-05-08 by [repolex](https://repolex.ai)*
