# Repolex Knowledge Graph of aio-libs/aiohttp-benchmarks

RDF knowledge graph data for [aio-libs/aiohttp-benchmarks](https://github.com/aio-libs/aiohttp-benchmarks), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiohttp-benchmarks
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 018d6a3dd9a343c0b1f1408b71ef4dd1d4d7a7fc
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 018d6a3dd9a343c0b1f1408b71ef4dd1d4d7a7fc
│           └── chunk-001.nq.gz
├── blob
│   ├── 06ce419425acd80c8ca98651637522e8700bccef.nq.gz
│   ├── 13b8db6d18184f305f23c6a11dc4921318d98072.nq.gz
│   ├── 375a195dcf336f81e993299e8b9c726f73f261d6.nq.gz
│   ├── 5330508a467f84c95695402950d38be86b46317c.nq.gz
│   ├── 69f9f3858a152a65c89295116c4a20e0b9bb9906.nq.gz
│   ├── 72f658314bbae902302d9b461d1574c32f0518a9.nq.gz
│   ├── 77346024471f6797e28eb27514548e8d2d711d22.nq.gz
│   ├── a440a51c54bed957f58a78a510f76e30b914f8ff.nq.gz
│   ├── aeaec49ccf973613d5c6a5fdaf88a5de5eb6c16d.nq.gz
│   ├── b39d6c78f33607bd271b840ae710e3dce8bce0bb.nq.gz
│   ├── bd45c2cc2afac0a15453e573a68ccc61287db16d.nq.gz
│   ├── c85160f0c6cc6677a3c3e52cefb487210341ab7e.nq.gz
│   ├── c910b66ff93a8bd06ba5898aeaa596f4830c3b8e.nq.gz
│   ├── d7bc42d6ec3e2fed744461ee429c1de55a458f6f.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 018d6a3dd9a343c0b1f1408b71ef4dd1d4d7a7fc.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[aio-libs/aiohttp-benchmarks](https://github.com/aio-libs/aiohttp-benchmarks)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
