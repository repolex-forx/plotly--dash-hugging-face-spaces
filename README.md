# Repolex Knowledge Graph of plotly/dash-hugging-face-spaces

RDF knowledge graph data for [plotly/dash-hugging-face-spaces](https://github.com/plotly/dash-hugging-face-spaces), parsed by [repolex](https://repolex.ai).

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
rlex download plotly/dash-hugging-face-spaces
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dddd5a69c742cab48bdbbb6e7a809fe4a3ec64dd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dddd5a69c742cab48bdbbb6e7a809fe4a3ec64dd
│           └── chunk-001.nq.gz
├── blob
│   ├── 11f3126b4f83a2417a87f9b74214420379084806.nq.gz
│   ├── 347fe43c99e89ae13ae2ff22e9983b9c505bcc10.nq.gz
│   ├── 7542adf8e2ca5bcd6dc509ef964da96adf3d7a3b.nq.gz
│   ├── 8ba84ed309e10231c75aa3811911c82e2477f996.nq.gz
│   ├── 9d9cee49461b2b05906b7d58f74934a2bd5e641f.nq.gz
│   ├── a27d29a29f56cdbc579fcc896da9caebfc0fa2f2.nq.gz
│   └── e7c5878bba6a97fcdee17d6f972a5a5d57c65c7e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dddd5a69c742cab48bdbbb6e7a809fe4a3ec64dd.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 13 files
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

[plotly/dash-hugging-face-spaces](https://github.com/plotly/dash-hugging-face-spaces)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
