# .github
Public README
# Project David

> David was the first entity. What began as a single GPT with a custom system prompt grew into a full AI orchestration platform.

Project David is an open source AI orchestration substrate — a platform for building, running, and coordinating intelligent agents at scale.

Built for engineers who won't trade data sovereignty for convenience.
Run open-weight models. Own your infrastructure. Orchestrate at scale.

## Ecosystem

| Repo | Description |
|---|---|
| [platform](https://github.com/project-david-ai/platform) | Core orchestration engine — supervisors, workers, streaming infrastructure |
| [projectdavid](https://github.com/project-david-ai/projectdavid) | Python SDK |
| [entities-common](https://github.com/project-david-ai/entities-common) | Shared utilities and validation |
| [david-core](https://github.com/project-david-ai/david-core) | Docker orchestration layer |
| [reference-backend](https://github.com/project-david-ai/reference-backend) | Flask reference implementation |
| [reference-frontend](https://github.com/project-david-ai/reference-frontend) | React reference implementation |

## Architecture

Project David is structured as a layered ecosystem. The **platform** is the core — a FastAPI orchestration engine that manages agents, tools, threads, and state. The **SDK** gives developers a clean Python interface to the platform without needing to interact with the REST API directly. **david-core** handles cloud deployment, TLS, and routing for the hosted instance.

The orchestration layer supports multi-agent deep research out of the box — a supervisor agent plans and delegates, workers execute in parallel, and a shared scratchpad provides observable, attributed state across the entire run.

### Stack

![Project David Stack](https://raw.githubusercontent.com/project-david-ai/projectdavid-platform/master/assets/svg/projectdavid-stack.svg)

```

## Documentation

Full documentation is available in the [docs](https://github.com/project-david-ai/docs) repository.

| Topic | Link |
|---|---|
| Platform Overview | [api-index.md](https://github.com/project-david-ai/projectdavid_docs/blob/master/src/pages/overview/api-index.md) |
| Quick Start | [sdk-quick-start.md](https://github.com/project-david-ai/projectdavid_docs/blob/master/src/pages/sdk/sdk-quick-start.md) |
| Assistants | [sdk-assistants.md](https://github.com/project-david-ai/projectdavid_docs/blob/master/src/pages/sdk/sdk-assistants.md) |
| Tools | [sdk-tools.md](https://github.com/project-david-ai/projectdavid_docs/blob/master/src/pages/sdk/sdk-tools.md) |
| Architecture | [sdk-architecture.md](https://github.com/project-david-ai/projectdavid_docs/tree/master/src/pages/architecture) |

> When the hosted docs site is live, all links above will be updated to `docs.projectdavid.co.uk`.

## Quick Start

Install the SDK:

```bash
pip install projectdavid
```

Run your first inference:

```python
from projectdavid import Entity

client = Entity(api_key="your_api_key")

assistant = client.assistants.create_assistant(
    name="my_assistant",
    instructions="You are a helpful AI assistant.",
)

thread = client.threads.create_thread()
```

See the [Quick Start guide](https://github.com/project-david-ai/projectdavid_docs/blob/master/src/pages/sdk/sdk-quick-start.md) for the full example.
