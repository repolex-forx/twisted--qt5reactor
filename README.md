# Repolex Knowledge Graph of twisted/qt5reactor

RDF knowledge graph data for [twisted/qt5reactor](https://github.com/twisted/qt5reactor), parsed by [repolex](https://repolex.ai).

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
rlex download twisted/qt5reactor
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 300a382b08097ec5933717cac09707957b80cfad
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 300a382b08097ec5933717cac09707957b80cfad
│           └── chunk-001.nq.gz
├── blob
│   ├── 0157c8f731ec0507ee0c4f3b731cf411d69d3277.nq.gz
│   ├── 03003478363ed583f0f48408eaa29452067d4ae6.nq.gz
│   ├── 110b6c4c15eae26dca5d3230972ad20d0cf0c686.nq.gz
│   ├── 15c9b31280c5300d34e7da2878d4521eabf51c54.nq.gz
│   ├── 3c4000fc89249f811286b64514a6b75b32c5a86b.nq.gz
│   ├── 465671aa10148728c5beae1b74ccf2db3071ce00.nq.gz
│   ├── 477b7a61d6b70fee20ca7ed5be64ff140a02ee2a.nq.gz
│   ├── 60addbea3da27f410d213d99071145ff26501ff6.nq.gz
│   ├── 64fea1c892723b9db5bda7d302168b6128e14bf5.nq.gz
│   ├── 7558bc3ed615ee199e3c8761d7e45b6067694446.nq.gz
│   ├── 829505c8f0973ea14c792798887a7b08d471ec29.nq.gz
│   ├── 83291bf9252283279b4cb04895d747736a1d6131.nq.gz
│   ├── 84061aea06e1ed07e1d076780ddc3029c4ffe02b.nq.gz
│   ├── 992ec5ecb8379f631d2e715b46901e7161e71f06.nq.gz
│   ├── b6fbf592c50b4bd2807e37a1565b1ab7ae051557.nq.gz
│   ├── db50e768f7dfa7cd6adf7dc463ad886829b7b816.nq.gz
│   ├── dfb29c92d8605d31797e70d137ffe6ac82e7035e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e71ae518bdbf72c7463f84b820db387508dc6d6c.nq.gz
│   └── fa3c7b22cecd1ac7f604271270e403969434a385.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 300a382b08097ec5933717cac09707957b80cfad.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[twisted/qt5reactor](https://github.com/twisted/qt5reactor)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
