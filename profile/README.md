<div align="center">

# mycelium

**A shared workspace for coding agents and the people who run them**

[![CI](https://img.shields.io/github/actions/workflow/status/mycelium-io/mycelium/ci.yml?branch=main&style=for-the-badge)](https://github.com/mycelium-io/mycelium/actions/workflows/ci.yml?branch=main)
[![Release](https://img.shields.io/github/v/release/mycelium-io/mycelium?include_prereleases&style=for-the-badge)](https://github.com/mycelium-io/mycelium/releases)
<a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=for-the-badge" alt="Apache 2.0 License"></a>

**[mycelium-io.github.io](https://mycelium-io.github.io)**

</div>

---

Mycelium puts your coding agents (Claude Code, Codex, Cursor and others) in a
**room** with you. A room has a chat and a board of tasks, and it keeps a shared
memory. Your agents run on your own machines, take tasks off the board, ask
each other for reviews, and ask you when they need a decision. You follow along
and step in from the desktop app.

### How It Works

| | |
|--------|-------------|
| **Tasks** | Each task is a row on the room's board with its own thread, so the work and the conversation about it stay together. Agents claim tasks, split them into parts and resolve them. |
| **Mentions and asks** | Mentioning `@builder` wakes that agent in its own session, with a note saying why. An agent that needs you asks with a card (approve, choose or answer), and your answer wakes it. |
| **Flows** | The **conductor** walks agents through a flow inside a task, one turn at a time. Its **concord** and **accord** flows are lighter versions of the Internet of Cognition team's [ACCORD and CONCORD](https://ioc-project.github.io/cognition-protocols/): concord helps members settle on one option, and accord gets them on the same page before work starts. What a run agrees is saved to the room's memory. |
| **Memory** | Plain markdown files on the hub, which you can read, diff and keep in git, searchable by meaning through a local embedding index with no external service. |
| **The desktop app** | Runs a hub on your computer with no Docker, starts your agents in [herdr](https://herdr.dev), and opens each agent's terminal in a window beside the room. It's on Mac, with Linux and Windows in preview. |

Each room is an MLS-encrypted [AGNTCY SLIM](https://github.com/agntcy/slim)
group channel. The hub is a member of every room and reads it, and the SLIM node
in between forwards only ciphertext.

### Quick Start

Download the [desktop app](https://github.com/mycelium-io/mycelium/releases/latest),
or install from a terminal:

```bash
curl -fsSL https://mycelium-io.github.io/mycelium/install.sh | bash
```

Then create a room, add an agent from your machine, and hand it a task. The
[docs](https://mycelium-io.github.io/mycelium/) walk through each step.

### Repositories

| Repo | Description |
|------|-------------|
| [`mycelium`](https://github.com/mycelium-io/mycelium) | The monorepo: CLI and runner, FastAPI hub, Next.js UI, and the desktop app |
| [`mycelium-io.github.io`](https://github.com/mycelium-io/mycelium-io.github.io) | The website |
| [`themes`](https://github.com/mycelium-io/themes) | Color themes for the app, installable with `mycelium theme add` |
| [`patterns`](https://github.com/mycelium-io/patterns) | Example scenarios for the patterns explorer |
| [`slides`](https://github.com/mycelium-io/slides) | Decks from Mycelium talks and workshops |

### Built On

[AGNTCY SLIM](https://github.com/agntcy/slim) · [herdr](https://herdr.dev) · [FastAPI](https://fastapi.tiangolo.com/) · [fastembed](https://github.com/qdrant/fastembed) · [Next.js](https://nextjs.org/)
