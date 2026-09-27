# Repolex Knowledge Graph of asimov-protocol/asimov-map-widget

RDF knowledge graph data for [asimov-protocol/asimov-map-widget](https://github.com/asimov-protocol/asimov-map-widget), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-protocol/asimov-map-widget
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6b37ffff3ee15d9646232d44f9c0f90f57a34939
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 6b37ffff3ee15d9646232d44f9c0f90f57a34939.nq.gz
│   └── repolex
│       └── 6b37ffff3ee15d9646232d44f9c0f90f57a34939
│           └── chunk-001.nq.gz
├── blob
│   ├── 112920a8119f9cbd1cce15acaed3abc6cbd058fe.nq.gz
│   ├── 11f02fe2a0061d6e6e1f271b21da95423b448b32.nq.gz
│   ├── 1f577938800e9705a82fe1e5b90fc8cd5fed160b.nq.gz
│   ├── 2bd5a0a98a36cc08ada88b804d3be047e6aa5b8a.nq.gz
│   ├── 2ee0a8b599528d4558e0edbfbe66f5b55425a44a.nq.gz
│   ├── 382a8322a054f61a11451f169021f766e1589782.nq.gz
│   ├── 84c8a23a8633122859eb4c2fb8f874aa97571525.nq.gz
│   ├── 8a816f627618681fa523dd0f6c0216b9e6675243.nq.gz
│   ├── 978b02cd40a557837f13c747445664be30b295ee.nq.gz
│   ├── a547bf36d8d11a4f89c59c144f24795749086dd1.nq.gz
│   ├── a866ff51155f56cc7f6005b3d6d1b6ae5c65eb84.nq.gz
│   ├── b2b87dc3196692621b8087db69a14cf80a31a410.nq.gz
│   ├── b36cddc9fc2d8bd0f3217c20c8ba2c02d4b8ee81.nq.gz
│   ├── b821d359fc4b4063cfb58da9e19c9b3937f52916.nq.gz
│   ├── b89af522a94fabe59200380865bdeabcd56e9ba3.nq.gz
│   ├── c6f82135ad145c8153e79f74657271e90cc4d253.nq.gz
│   ├── d11224b762e0ee43a1e48e001d6e0a3f759d6390.nq.gz
│   ├── d296490915563f133e751430ed67fac5600ccac2.nq.gz
│   ├── db0becc8b033a4a78144f4a3bb852082fe91cd62.nq.gz
│   ├── e7564f71227f44ac1edbb32b28a6e6240b8be3cd.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── f251395fa84bcee87bd0d70099c7c66463facdb9.nq.gz
│   └── fab12190d83e8958ecb52ec814f532a886642a82.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 6b37ffff3ee15d9646232d44f9c0f90f57a34939.nq.gz
├── filetree
│   └── 6b37ffff3ee15d9646232d44f9c0f90f57a34939.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 32 files
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

[asimov-protocol/asimov-map-widget](https://github.com/asimov-protocol/asimov-map-widget)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
