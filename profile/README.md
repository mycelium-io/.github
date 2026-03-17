<div align="center">

# Mycelium

**A coordination layer for multi-agent systems**

Shared rooms, persistent memory, and semantic negotiation — built on the [Internet of Cognition](https://outshift.cisco.com).

[![CI](https://img.shields.io/github/actions/workflow/status/mycelium-io/mycelium/ci.yml?branch=main&style=for-the-badge)](https://github.com/mycelium-io/mycelium/actions/workflows/ci.yml?branch=main)
[![Release](https://img.shields.io/github/v/release/mycelium-io/mycelium?include_prereleases&style=for-the-badge)](https://github.com/mycelium-io/mycelium/releases)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](https://github.com/mycelium-io/.github/blob/main/LICENSE)

**[mycelium-io.github.io](https://mycelium-io.github.io)**

</div>

---

AI agents are powerful individually, but they can't think together. Mycelium gives agents **rooms** to coordinate in, **persistent memory** that compounds across sessions, and a **CognitiveEngine** that mediates negotiation so agents never have to talk directly to each other.

### How It Works

| Pillar | What it does |
|--------|-------------|
| **Coordination Protocol** | Rooms with a state machine. CognitiveEngine orchestrates multi-issue negotiation via NegMAS. |
| **Persistent Memory** | Namespaced key-value store with semantic vector search, backed by AgensGraph + pgvector. |
| **Knowledge Graph** | Two-stage LLM extraction turns conversations into structured concepts in an openCypher graph. |

### Quick Start

```bash
curl -fsSL https://mycelium-io.github.io/mycelium/install.sh | bash
mycelium install

mycelium room create my-project --mode async
mycelium memory set "context/goal" "Build a REST API for the new service"
mycelium memory search "database decisions"
```

### Repositories

| Repo | Description |
|------|-------------|
| [`mycelium`](https://github.com/mycelium-io/mycelium) | Core monorepo — CLI, FastAPI backend, and generated client |

### Built On

[Internet of Cognition](https://outshift.cisco.com) (Outshift by Cisco) · [NegMAS](https://negmas.readthedocs.io/) · [AgensGraph](https://github.com/skaiworldwide-oss/agensgraph) · [FastAPI](https://fastapi.tiangolo.com/) · [pgvector](https://github.com/pgvector/pgvector)
