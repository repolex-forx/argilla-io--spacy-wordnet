# Repolex Knowledge Graph of argilla-io/spacy-wordnet

RDF knowledge graph data for [argilla-io/spacy-wordnet](https://github.com/argilla-io/spacy-wordnet), parsed by [repolex](https://repolex.ai).

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
rlex download argilla-io/spacy-wordnet
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fddfb6f1f3cdf86e5fbac16f650dba5f2cd01055
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fddfb6f1f3cdf86e5fbac16f650dba5f2cd01055
│           └── chunk-001.nq.gz
├── blob
│   ├── 0353919948fef671ab56674df41153a2c515cf3f.nq.gz
│   ├── 1c52195338c0ba9487b2ffc1ecf1e165aab79349.nq.gz
│   ├── 215bd885f69471b9b74ab45fe69ae0f7c5a13d4a.nq.gz
│   ├── 226e6f59313909fc91249cb261f86ee5fa25daa5.nq.gz
│   ├── 2633141cc0d06a8f82f3a9cc4b3325893f693e4a.nq.gz
│   ├── 2683bb0d49a3f6553966b6f6cc228a7c61307aa2.nq.gz
│   ├── 3989c5130411f77da5198a165361ea1b8b2fc1de.nq.gz
│   ├── 398cc10ccfb0aa5ebeae2aebaf87e1b03f637d02.nq.gz
│   ├── 39f890f7f214ffe47e898013cb319abc143bfdca.nq.gz
│   ├── 3c963632027b176c1146e6cca3b2d1aab781d766.nq.gz
│   ├── 4179ad7e296edfc00d0aaeb9f0b988f673f0926e.nq.gz
│   ├── 44c1a13c34ce4cd36e45230d8e1b9c573c587c66.nq.gz
│   ├── 5a3f5e148f23c122054e251d381de1b28707e1fc.nq.gz
│   ├── 5cfb9efc0c81bc28a79ff18f9e2dae1c0be23025.nq.gz
│   ├── 828ef2ba0a7eb7ed354b8603abbb5e4aec7a1055.nq.gz
│   ├── 871950df3f80fa9315dcec169c6af0a0a000f62e.nq.gz
│   ├── 91d63cd1fef6eaf55706be2eff6e96e3882bc061.nq.gz
│   ├── 9c1e06caee4a89fe979f98c16103587a9c2b4eb9.nq.gz
│   ├── 9e44b5a284c9c258550f9ea713de7c5f5c02d440.nq.gz
│   ├── 9fa27b4bda3a25b9ddb48fe1546e284efc43f6ad.nq.gz
│   ├── a9b359606522fef07a757612f9b6dca0ba468b99.nq.gz
│   ├── c0c48084003391b60a5283322fb50cf631d05dd8.nq.gz
│   ├── cd8e0913a8fa9ba3a03696eb3f0a03730d14a485.nq.gz
│   ├── db4bde2fa5455a9ea1c781f932df07fe4581a34b.nq.gz
│   ├── dda9a2f67cd45b1e83e38c9a27bbb22f30966e47.nq.gz
│   ├── f7ba63503dacf4df6691ae626bdd0f933c6983e4.nq.gz
│   └── fb33e1dc3d48f50b8a482ec746d2a5c8d0271018.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fddfb6f1f3cdf86e5fbac16f650dba5f2cd01055.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[argilla-io/spacy-wordnet](https://github.com/argilla-io/spacy-wordnet)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
