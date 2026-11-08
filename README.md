# Repolex Knowledge Graph of canonical/sdcore-webui-operator

RDF knowledge graph data for [canonical/sdcore-webui-operator](https://github.com/canonical/sdcore-webui-operator), parsed by [repolex](https://repolex.ai).

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
rlex download canonical/sdcore-webui-operator
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 46a734935a9410bebb75a262f01f7fc8cb793388
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 46a734935a9410bebb75a262f01f7fc8cb793388
│           └── chunk-001.nq.gz
├── blob
│   ├── 07e10a08514124ce2ce63de2bd3fccecb89797e1.nq.gz
│   ├── 13af703428e23ce7d56cf7a1bc7061b64a8f6a18.nq.gz
│   ├── 1b28b7fbe3ec5002ab0dfa436847990093849423.nq.gz
│   ├── 1b62fd8e5d5673909bc2f74a5e03bdba1e34d377.nq.gz
│   ├── 1d0a543f9b43b352b852bb1ebb8e7115f49d958d.nq.gz
│   ├── 2e6a68c6a56dc628a7b847cdd0d1a4641eb4f9ed.nq.gz
│   ├── 3a277b3488023cb70d152bef071e817039bb0f7c.nq.gz
│   ├── 3bcd8a9f726c1e7ff32172d0ed5d95ab6436a34c.nq.gz
│   ├── 44d26118a5f2063dff74d85eee6f76d6428dfb32.nq.gz
│   ├── 4d394c33b8ea132a10ef09db97c9509d10e14fd1.nq.gz
│   ├── 534f791388dd80ddccda3fefc5b241835898f7c9.nq.gz
│   ├── 5d358339a92d6bcc5b1b5bc8be29ea2eb30d2344.nq.gz
│   ├── 7170c4d9d3e2f77e3bb132d4bf23b2a49470248a.nq.gz
│   ├── 74c76f4df18e9df8854ec47f117a0f77130d260d.nq.gz
│   ├── 88178a039b4aba2815b8cb92d55326116a1b2885.nq.gz
│   ├── 8d771e187ba4b2ced1b643c804548e5c014bab70.nq.gz
│   ├── 9523adcc0e8cc148e287c44110ff7a778e14def8.nq.gz
│   ├── 96bebd3208c0758cefa1a977776cb23ad2425874.nq.gz
│   ├── a7fd57504931d9d27188e78ee4bf0e6ebca2bf9e.nq.gz
│   ├── aaed2e528a296cfc4b6c9e53924186de79fbef7c.nq.gz
│   ├── b1a8f03a40d69e8a8cf5402612c28727e00b0793.nq.gz
│   ├── b1d6cc2490b2359486e0ad60c509d2ff782d12d9.nq.gz
│   ├── b24588f615ca151f6a0cdc4c67975329eae076dd.nq.gz
│   ├── b8366f2ace0640e25d8f5fa1143ccdb2171a5f66.nq.gz
│   ├── bbda50f7b27139850dafd5b2865768ab817b1ccd.nq.gz
│   ├── bbe77cb69558e274639017d0079c3ebd6bc948a5.nq.gz
│   ├── c0b34d8879b121d763efc7e0b710cbae2bd9096f.nq.gz
│   ├── c0cb49fa607f671dffb9e0d0c8bb275df0ed21ba.nq.gz
│   ├── c33c25229079110ad25ea2de778f3a760db43941.nq.gz
│   ├── c60eeac2b09941ff10f8bb58e58a7642c4fc0caa.nq.gz
│   ├── d75cb7e1995609944fb1aecee8db0a5df8bf1061.nq.gz
│   └── ed67d9f62e5efc1621f0c0e8ae8ee293fdde7856.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 46a734935a9410bebb75a262f01f7fc8cb793388.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[canonical/sdcore-webui-operator](https://github.com/canonical/sdcore-webui-operator)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
