<div align="center">

# mycelium

**A coordination layer for multi-agent systems**

Shared rooms, persistent memory, and structured negotiation over an end-to-end-encrypted messaging fabric.

[![CI](https://img.shields.io/github/actions/workflow/status/mycelium-io/mycelium/ci.yml?branch=main&style=for-the-badge)](https://github.com/mycelium-io/mycelium/actions/workflows/ci.yml?branch=main)
[![Release](https://img.shields.io/github/v/release/mycelium-io/mycelium?include_prereleases&style=for-the-badge)](https://github.com/mycelium-io/mycelium/releases)
<a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=for-the-badge" alt="Apache 2.0 License"></a>

**[mycelium-io.github.io](https://mycelium-io.github.io)**

</div>

---

AI agents are powerful individually, but they can't think together. Mycelium gives agents **rooms** to coordinate in, **persistent memory** that compounds across sessions, and a first-party **aligner** that mediates negotiation so agents never have to talk directly to each other. You drive it from a **UI**; your agents work through the **CLI**.

### How It Works

Mycelium is **SLIM-native**: one [AGNTCY SLIM](https://github.com/agntcy/slim) messaging node, a thin FastAPI backend, and local files. **No database.**

| Pillar | What it does |
|--------|-------------|
| **Rooms** | Each room is one end-to-end-encrypted SLIM group channel — a persistent space where agents share context and open scoped, recorded negotiations (episodes). |
| **Persistent Memory** | Markdown files on your filesystem are the shared source of truth — greppable, git-shareable — made recallable by meaning through a local ONNX embedding index. No external service. |
| **Structured Negotiation** | The **aligner**, a first-party cognition engine, runs a real [NegMAS](https://negmas.readthedocs.io/) Stacked Alternating Offers negotiation and compiles the agreement into a shared `- [ ]` plan the team executes. |

### Quick Start

```bash
curl -fsSL https://mycelium-io.github.io/mycelium/install.sh | bash
mycelium install

mycelium room create my-project
mycelium memory set context/goal "Build a REST API for the new service"
mycelium memory search "database decisions"
```

### Repositories

| Repo | Description |
|------|-------------|
| [`mycelium`](https://github.com/mycelium-io/mycelium) | Core monorepo — CLI, FastAPI backend, Next.js frontend, and generated client |

### Built On

[AGNTCY SLIM](https://github.com/agntcy/slim) · [NegMAS](https://negmas.readthedocs.io/) · [FastAPI](https://fastapi.tiangolo.com/) · [fastembed](https://github.com/qdrant/fastembed) · [Next.js](https://nextjs.org/)
