# Repolex Knowledge Graph of graphql-python/gql-next

RDF knowledge graph data for [graphql-python/gql-next](https://github.com/graphql-python/gql-next), parsed by [repolex](https://repolex.ai).

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
rlex download graphql-python/gql-next
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1e583a203d8b2f2a18692a273bd7ba0b3dba3c69
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1e583a203d8b2f2a18692a273bd7ba0b3dba3c69
│           └── chunk-001.nq.gz
├── blob
│   ├── 004ff84366a6377451310a9acc7470a818312030.nq.gz
│   ├── 01aa4b79dc6d77f667e65fde47430e2f43bbd88f.nq.gz
│   ├── 0e187118ebda14e0499f91ddbb7c94ed37c4ffaf.nq.gz
│   ├── 23d4a9147438442a6fdcc2ce7834837a187d0f91.nq.gz
│   ├── 246c98c56e7a6c7c85a788ed70e0ff0aa5ce2c2e.nq.gz
│   ├── 291be97b8d1b6189352f4ba69c7b5a910de476b5.nq.gz
│   ├── 31332eb7b0d4d77b42a6c7ebaa1538f829f23a35.nq.gz
│   ├── 3737e12b2645e0c21d84eac569f6ab765c8ec565.nq.gz
│   ├── 4bead1660611942e92d87c3a73e051d743fa844d.nq.gz
│   ├── 526c111f90c52876f3ef3d220ed585a0cffbeaba.nq.gz
│   ├── 60ce2f81d23d1bdfc1b8f6d29ebf046eb7d2dd08.nq.gz
│   ├── 6a4efd6ef1e9f5b5c853744e26d7b0fccc697cb1.nq.gz
│   ├── 788aa3adf32553959f7abbf21e55eb41677d725a.nq.gz
│   ├── 7b1d9a51c9d5e8d010ff8338d819958b1cbc97d3.nq.gz
│   ├── 7de0d31b385a8a2ad21877bb67a16c3b3638cb25.nq.gz
│   ├── 8084cb8591e0848b3898811d2ce381101ecfc996.nq.gz
│   ├── 814cb1d2cda917d091c4b3bacd07473b6132e48b.nq.gz
│   ├── 9ccf61b14587b60fb7dc5587af58ef4f9f591108.nq.gz
│   ├── 9f8e3e25b9aee1f09d361237280a36e47ac324ad.nq.gz
│   ├── a73b3260ec5845efc7f62380f6853156363fbfc5.nq.gz
│   ├── a7ed6acd3b154b951a7d54151e2e839e8d7a63d0.nq.gz
│   ├── a804d9a614229aca41152bba7f9471e16bf4d382.nq.gz
│   ├── bcac95b5620fe84a81c4a6b3caf55995778a4b0e.nq.gz
│   ├── bdcd6c97ac116600116af5f63076cc8eaae5f575.nq.gz
│   └── d36befe2c68854edb4c4c6d1275e5e39c1c205e7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1e583a203d8b2f2a18692a273bd7ba0b3dba3c69.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[graphql-python/gql-next](https://github.com/graphql-python/gql-next)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
