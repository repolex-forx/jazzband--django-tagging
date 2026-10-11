# Repolex Knowledge Graph of jazzband/django-tagging

RDF knowledge graph data for [jazzband/django-tagging](https://github.com/jazzband/django-tagging), parsed by [repolex](https://repolex.ai).

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
rlex download jazzband/django-tagging
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 79cb321b1e4c464d39ed96ddbef02617ab0c692e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 79cb321b1e4c464d39ed96ddbef02617ab0c692e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cddc85a338fae0df86f6138135fd198fbeb258a.nq.gz
│   ├── 10dc930458865254d826fb70fb77c4644c998d37.nq.gz
│   ├── 137eb55e2d1d2e0cbbedd1359cdd236965a052b8.nq.gz
│   ├── 1bfb9fe3ec8904acb20535ff15930e0445f9c1ff.nq.gz
│   ├── 1e5cdf58915cea58c555123c7370d1b1a80afea7.nq.gz
│   ├── 32a08b62e5fa6d08a6bf6695cd92940915b62bf6.nq.gz
│   ├── 374101e3d198ca3d30ec535dce4b4cfb59ab03bb.nq.gz
│   ├── 50995c8d3efbd76c06cd2bc4d31e1a403f48d850.nq.gz
│   ├── 558349c79e305eef186eeae9bc2a738ea4382ab9.nq.gz
│   ├── 59f77e757eea3a36bb5f5d9916311eda69e31b93.nq.gz
│   ├── 5dd2582e15818cc0e637187b542d87e0cd288cb4.nq.gz
│   ├── 63a0143a851c6b4bcbf906b2df3c7ec4c94adec5.nq.gz
│   ├── 66bbbff892fd512c8a5a7cf013697c3079003e38.nq.gz
│   ├── 68bc17f9ff2104a9d7b6777058bb4c343ca72609.nq.gz
│   ├── 759e2aadc6044a06c14d01cbc03adfcdc897f219.nq.gz
│   ├── 770e928b7564a58e123107e0b34d2fec4eb310ca.nq.gz
│   ├── 7910b1165a54d61720c3ade42f0146af72b8e0dc.nq.gz
│   ├── 7db3e7e1204c983008ab006a963155dd90f30ada.nq.gz
│   ├── 7f11455db78763946b18451d7f1fe4401822b46f.nq.gz
│   ├── 805bae9720c89205aa5f95d8df4cf37f2f384dcb.nq.gz
│   ├── 847593a97b9bf328e80dcc55d6828dc623b2d6ad.nq.gz
│   ├── 85434112f4c5f4675d110e45d914c4caf1ad6d8b.nq.gz
│   ├── 96557995353a2cd3cebbe8d6e182a5acae9c1f8f.nq.gz
│   ├── a52e1dbe1c98bd12da9aac31a5309cb37807bc3d.nq.gz
│   ├── ab524e269350a64f1baf4e3a849a83c9be0b6dac.nq.gz
│   ├── aeb41f51ec2cc27a5bde319d9ab9164454889dae.nq.gz
│   ├── b3233966cfd49007d197c8f5ff692a7306a5ada3.nq.gz
│   ├── b7f0596000b10d8065c2ff1e09e777432e75a851.nq.gz
│   ├── c2890170595d91f07f70f94b20187fbe950dad00.nq.gz
│   ├── cc2d69692cd8f458c7257e12819a829000cd6a3e.nq.gz
│   ├── cc9ce001a780e53df099fbbaa7c88cab217a4877.nq.gz
│   ├── d01e27cc7b7503ccaecf36403a09d0a0d15b6b7b.nq.gz
│   ├── da2480e7f36ae04b8421388a5d290c01caca44b3.nq.gz
│   ├── de2890dc9c710e4be4e93d08b7cc931875f4783c.nq.gz
│   ├── ea6498370f44db9e62fe343d6ceea65c18af8e15.nq.gz
│   ├── ea96daad6b646bd312bdde511d03e08d7bb79da9.nq.gz
│   ├── ef4e18086772515057fab328412af8b1a74d6936.nq.gz
│   ├── f0203780174b299adf7fe7d11fffaba76b9bb418.nq.gz
│   └── f04b202a4acf4ceb2da65e8d84ee363484fed222.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 79cb321b1e4c464d39ed96ddbef02617ab0c692e.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 46 files
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

[jazzband/django-tagging](https://github.com/jazzband/django-tagging)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
