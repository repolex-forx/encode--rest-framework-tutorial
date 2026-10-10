# Repolex Knowledge Graph of encode/rest-framework-tutorial

RDF knowledge graph data for [encode/rest-framework-tutorial](https://github.com/encode/rest-framework-tutorial), parsed by [repolex](https://repolex.ai).

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
rlex download encode/rest-framework-tutorial
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c338449d616f613fdcbfa4ea368cdf163a0f183d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c338449d616f613fdcbfa4ea368cdf163a0f183d
│           └── chunk-001.nq.gz
├── blob
│   ├── 146f4b39a950f44529acc9e4c6e6767196510f54.nq.gz
│   ├── 1bf63d63259a3c2efc27c9b5abf3a4c506d2d6a8.nq.gz
│   ├── 24ee5b1be9961e38a503c8e764b7385dbb6ba124.nq.gz
│   ├── 33c9aa9a275f0ffbd44fdb61def045f522690400.nq.gz
│   ├── 3884b2bdd6ee53068cfbf613f8c321d99242cb1b.nq.gz
│   ├── 3a5330e09be07989b9df88e0d3aa003f7d297231.nq.gz
│   ├── 3ffd7afb40d27008aee7d8377bc1c5aafe62b620.nq.gz
│   ├── 5a754715db72b2aaad2e26fe6e3b5ede35dd9152.nq.gz
│   ├── 5ad33a1a0f8bf7d51b935daa39543faba7f0dd47.nq.gz
│   ├── 6e3564966b38af4a3923916d1dbd2842a7ff2770.nq.gz
│   ├── 7510b28062476752dc86268ffe62a659003e08df.nq.gz
│   ├── 82e5b9469c96458306622fa38bce90e35851a729.nq.gz
│   ├── 95717e567359fb60c204fbe3f5ccecec99019dd7.nq.gz
│   ├── 97f17bab5b0dfa059a8c65a0719d4e4b55ffb292.nq.gz
│   ├── 9bca2f81e5fbca21388a19642ac6b48802fb9ea0.nq.gz
│   ├── a1a766399f95805008f87adbd891607dad76d764.nq.gz
│   ├── af0cb04a933df1dd27195beec6f6a2c519aa85a2.nq.gz
│   ├── bc22ecb2461da93d069f2c75f6cfda44ee9e4076.nq.gz
│   ├── c598a6743862b69b64f808c1af54efec8252392d.nq.gz
│   ├── de291ac4c95e7762347781722a8d985f6196a3c4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec8a880699fa2d3701895ce604cbb3dadf4605f0.nq.gz
│   ├── f2ead5c98853327d3742816f58f7a7209f68de4d.nq.gz
│   ├── fc8365b25d1a28d17b784aa6a789b46999af0119.nq.gz
│   └── feb2a9c1f301d0f101499ce4accc6a7da43d6526.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c338449d616f613fdcbfa4ea368cdf163a0f183d.nq.gz
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

[encode/rest-framework-tutorial](https://github.com/encode/rest-framework-tutorial)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
