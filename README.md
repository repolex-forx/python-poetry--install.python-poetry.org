# Repolex Knowledge Graph of python-poetry/install.python-poetry.org

RDF knowledge graph data for [python-poetry/install.python-poetry.org](https://github.com/python-poetry/install.python-poetry.org), parsed by [repolex](https://repolex.ai).

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
rlex download python-poetry/install.python-poetry.org
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 458b4019ae9b22c1d0334e71259660722f4c5b33
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 458b4019ae9b22c1d0334e71259660722f4c5b33
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cafec03cf625c9d818c48a3047c12a5b91d26b2.nq.gz
│   ├── 29ad14cbad7aeaf48f4323ae29c0ec4bfe5ce0a4.nq.gz
│   ├── 2f069a7b6481fb234265a538c418e3d693224bba.nq.gz
│   ├── 5c2385f214ce220a9eefc2f1874a28dbe43a2ebf.nq.gz
│   ├── 74df1b8355b6574f83ed4d514b1472095e00f97d.nq.gz
│   ├── 87e18b6fd8062b475ad5f3c2968fe69f4d9657d1.nq.gz
│   ├── 8e7db18a7db0566a11647a83643b6e6fa74e3933.nq.gz
│   └── cd83dc8741c7252b59d666663c33b5257f72d704.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 458b4019ae9b22c1d0334e71259660722f4c5b33.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 16 files
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

[python-poetry/install.python-poetry.org](https://github.com/python-poetry/install.python-poetry.org)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
