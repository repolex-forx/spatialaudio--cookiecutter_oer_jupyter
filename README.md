# Repolex Knowledge Graph of spatialaudio/cookiecutter_oer_jupyter

RDF knowledge graph data for [spatialaudio/cookiecutter_oer_jupyter](https://github.com/spatialaudio/cookiecutter_oer_jupyter), parsed by [repolex](https://repolex.ai).

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
rlex download spatialaudio/cookiecutter_oer_jupyter
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4a808575cc77e8ef77a79206728d6412d50cc593
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4a808575cc77e8ef77a79206728d6412d50cc593
│           └── chunk-001.nq.gz
├── blob
│   ├── 04912a05b4f3247649ad7288af697cb619a609e6.nq.gz
│   ├── 1f33a9df6459613007aee7f5cfa335bd30f1f723.nq.gz
│   ├── 38034e3dbf9dca831f7a45e093b5dec0a9a72d9e.nq.gz
│   ├── 48bc119d435cf5e0935ef20276365a6c68a401c6.nq.gz
│   ├── 54a085160d5e50c0a1a672d7d73eb9e96edb7065.nq.gz
│   ├── 7bc1eaaac614dd66235f8e8fa6d2da131a9ac8fd.nq.gz
│   ├── 80be1fde30049d1383083f519f2bf2737093b8e7.nq.gz
│   ├── 83d373cffce41fef1ca8b1cb2434e7ec007692aa.nq.gz
│   ├── 977cd53582cc15d32599e7aadb8ae3ccb9ca1336.nq.gz
│   ├── 9f1f668e87a0cc9e18469e583416c56e069faa5d.nq.gz
│   ├── a7b966ec285848cf020a639d5a8e9d51d8f1082c.nq.gz
│   ├── bacfda451d148d8d807ced5975e1301052a77830.nq.gz
│   ├── bb0498a414c9a1df18440ec2f5719f85fd303812.nq.gz
│   ├── be0ceb9a08713e8473dfaf3478ba5d38f22a52d6.nq.gz
│   ├── c06872ae1c383fce4b7da610f088b6063b38ccf4.nq.gz
│   ├── c2088ff9b712f0cdac73ada3c75315f10abfb35a.nq.gz
│   ├── ca03d69f2eeb26562dcf81eb6a8048225be46e1e.nq.gz
│   ├── ccde6fad8769c63eff5fee9bcfa8b7853db6d6d8.nq.gz
│   ├── dc833dd4befe4d013346e1b2418e3fe91406a7a8.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ff5670115a96a669641650eb8fe54c1ae1843da6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4a808575cc77e8ef77a79206728d6412d50cc593.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 27 files
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

[spatialaudio/cookiecutter_oer_jupyter](https://github.com/spatialaudio/cookiecutter_oer_jupyter)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
