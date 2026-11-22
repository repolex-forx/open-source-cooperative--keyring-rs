# Repolex Knowledge Graph of open-source-cooperative/keyring-rs

RDF knowledge graph data for [open-source-cooperative/keyring-rs](https://github.com/open-source-cooperative/keyring-rs), parsed by [repolex](https://repolex.ai).

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
rlex download open-source-cooperative/keyring-rs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   ├── 04faa1fc015df37e336f246e2ed6f8235bd4c33e
│   │   │   └── chunk-001.nq.gz
│   │   └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   ├── 04faa1fc015df37e336f246e2ed6f8235bd4c33e.nq.gz
│   │   └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5.nq.gz
│   └── repolex
│       ├── 04faa1fc015df37e336f246e2ed6f8235bd4c33e
│       │   └── chunk-001.nq.gz
│       └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5
│           └── chunk-001.nq.gz
├── blob
│   ├── 335cad39bc42fbb1ca9013edc5cfe6f2bb47bbc8.nq.gz
│   ├── 45e373efbc61f4d2828565d192382671565b010d.nq.gz
│   ├── 47f6e38f542232e602b77a4c61d86621b3ba8684.nq.gz
│   ├── 5f5e2dc0d20e8fc92ec2d5d0d2d3d7168dd0f56b.nq.gz
│   ├── 70e126cb17be6d49800fa746fd35d73e6292363c.nq.gz
│   ├── 7e554dcb6083b16c4d76210d874ff5da45e1d40f.nq.gz
│   ├── 86930176b3ec3f72c9219dccd180bfdf6cdae5ce.nq.gz
│   ├── 87d92c8c24e0e39e90e7ee8f859fb2a6ec751c28.nq.gz
│   ├── 89fd204f31e0bd1217e17d75bfda6ba7ebed6efc.nq.gz
│   ├── 8be4771b227a66d5c043ee52c08c64d4edda9674.nq.gz
│   ├── 8f9ddb68a1673f0aee48cedc83211fe1362b0115.nq.gz
│   ├── 8fff472decde25d9d0ab453ac52d506137c31dc1.nq.gz
│   ├── 91cc7f771d573437eb5ac431eac20009f3284ac1.nq.gz
│   ├── a7f505c3c5056b3ff227cd07889d6f75b3076643.nq.gz
│   ├── ac3c5605d45b8f568fd575fc3f85e67b507c2a2a.nq.gz
│   ├── b277f0fe2e381963699ce05f130d76b3ead100a6.nq.gz
│   ├── b94e50a3834845b294bdd13dda4106d7cb14048d.nq.gz
│   ├── c23a779db4b211f441d319abb52fa79386e745df.nq.gz
│   ├── c32f440ba5ca5030d7893c150d4b8206b729995d.nq.gz
│   ├── c5cb2181858ae5994056ef2bf01fb384911c1a3a.nq.gz
│   ├── d9db0484184ba6aef1aaecbff5a05a50255f2635.nq.gz
│   ├── de779e302cbb0142fb90d3e7c26819d1647ca2fc.nq.gz
│   ├── e203988e591b92da05c77dc12536d503deeb740a.nq.gz
│   └── f54eefd2e0c52f8fd7c590781239daf304e2f1ed.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   ├── 04faa1fc015df37e336f246e2ed6f8235bd4c33e.nq.gz
│   └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5.nq.gz
├── filetree
│   ├── 04faa1fc015df37e336f246e2ed6f8235bd4c33e.nq.gz
│   └── 3a46e9ce493aa0b63be84e688cc0723acf6714c5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

17 directories, 39 files
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

[open-source-cooperative/keyring-rs](https://github.com/open-source-cooperative/keyring-rs)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
