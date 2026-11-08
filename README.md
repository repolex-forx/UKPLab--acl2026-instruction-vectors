# Repolex Knowledge Graph of UKPLab/acl2026-instruction-vectors

RDF knowledge graph data for [UKPLab/acl2026-instruction-vectors](https://github.com/UKPLab/acl2026-instruction-vectors), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/acl2026-instruction-vectors
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fd390c7b8b9e8677da071fe197b73e2f22da53b9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fd390c7b8b9e8677da071fe197b73e2f22da53b9
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cc0bfab9e1370bb6d05422bb6db41f85049779a.nq.gz
│   ├── 0f215d3fd17cb6ee07fce3ae1718db049b78aed7.nq.gz
│   ├── 24af4d5f9b497905a143dd97131afc4f9d8e198e.nq.gz
│   ├── 299f2eb069cd8958f2bbb41a9ddf88df5731e30e.nq.gz
│   ├── 2b3dfbf7bc381956b2759366f541c5c6ea52dc25.nq.gz
│   ├── 2b6901e926da7b0d6bbd32af20982475f759307e.nq.gz
│   ├── 37e9e91f3029318d576da4a739ba9e3180e18464.nq.gz
│   ├── 39460c44ee45754c931a26f2e09e6cb741ed6a8f.nq.gz
│   ├── 3c03fa1785c067b11a689642af4dabf69cb15b84.nq.gz
│   ├── 438b6eddc04608fa0de45a9916d5b8ca204f1b0f.nq.gz
│   ├── 4494992e95a890d760734ccf84e8f96ba53b132e.nq.gz
│   ├── 4efb08faa618a58f379e81c1a1c43c5a4596efd5.nq.gz
│   ├── 5b67f1b9dd3a818cd877077a0f6b0b3d37ebb9ce.nq.gz
│   ├── 5e8d20793ff178ae98c47af5f4f68c14172085b3.nq.gz
│   ├── 5eac1356291adb7ff38701f0a7cfc9b230a417ab.nq.gz
│   ├── 63a4f098a39c859feb8c5e2514bfc429679824b4.nq.gz
│   ├── 7cb2805d18b3c07484bb66b6cf90763065c5a11c.nq.gz
│   ├── 7e98db5ff4665a4d0f6057b61de02e43053523a5.nq.gz
│   ├── 83d960379ead9e07713b49efaa804156bd9a4f1f.nq.gz
│   ├── 87a0a1ab6d8360d30b463ff4dbac4d52129b0cfb.nq.gz
│   ├── 91031a0499874910c3d5b131f5d0dde59a489390.nq.gz
│   ├── 921792fdfa7fb72467f5758cf510f17a345f2d96.nq.gz
│   ├── 94d8e9cbd75d9936a623b7294334d2cb2e4fe3c3.nq.gz
│   ├── 95b21d365649abfee1308555209c574027e8f069.nq.gz
│   ├── 97900b5a3e93ab94fb7d147f1bd020735f6991c3.nq.gz
│   ├── 9c404e33ced1fcc47ea6f364c0d884329c38066f.nq.gz
│   ├── a0052944e156121b4c35eb9f5e468169c32eecaa.nq.gz
│   ├── a5b468e620d55353a2a743c01b929dc922f612a8.nq.gz
│   ├── a97c619a42132ad7edd30b962defb617af3f6d79.nq.gz
│   ├── ccf2b0f0f63607e4b47e648b918f70e4945656cc.nq.gz
│   ├── cd3924211119831f77f6299c8cc1dc43edf0571c.nq.gz
│   ├── d1b10eeeb6d8db2a5dc567976771c49b6e2d83ca.nq.gz
│   ├── dec587aea6ae5c0e0ff0d2cb4215f81bf82946cd.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e995f3cefdc1ec5397dd707462626b5f9296a595.nq.gz
│   ├── ea6d05ea8f9d193059c6b06318dbcc5229e7b33a.nq.gz
│   ├── ee35b8b61b07b931029117ac388d527ce6e66c3a.nq.gz
│   ├── ef2095b48db7a5bba7328470995a59bed821af08.nq.gz
│   └── f0751bbf51defcf36e120ae8588647543720fcf8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fd390c7b8b9e8677da071fe197b73e2f22da53b9.nq.gz
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

[UKPLab/acl2026-instruction-vectors](https://github.com/UKPLab/acl2026-instruction-vectors)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
