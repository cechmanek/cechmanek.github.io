# Justin Cechmanek

Personal website for **Justin Cechmanek** — Senior Applied AI Engineer at Redis, building [RedisVL](https://github.com/redis/redis-vl) (the Redis Vector Library) for LLM and agentic-AI workloads: semantic caching, contextual chat history, semantic routing, and AI agents.

Live site: <https://cechmanek.github.io/>

## About

Justin is an AI engineer focused on computer vision, robotics, and real-time data infrastructure for AI. He works on the open-source tooling that turns Redis into a real-time context engine for agents — vector search for RAG, in-memory short-term memory, and semantic caching.

- **GitHub:** [@justin-cechmanek](https://github.com/justin-cechmanek)
- **LinkedIn:** [in/justin-cechmanek](https://linkedin.com/in/justin-cechmanek)
- **Hugging Face:** [@cechmanek](https://huggingface.co/cechmanek)
- **Redis blog:** [Author profile](https://redis.io/blog/author/justin-cechmanek/)

## Technical work

- **RedisVL** — High-level Python abstractions for vector search, semantic caching (`SemanticCache`), semantic routing (`SemanticRouter`), and conversational/agent memory on Redis.
- **Semantic caching for LLMs** — Research and tooling on reducing LLM cost and latency via embedding-based response reuse; co-author of *Advancing Semantic Caching for LLMs with Domain-Specific Embeddings and Synthetic Data* (2025, arXiv:2504.02268).
- **Agent memory** — Contributor to Redis Agent Memory Server and integrations with agent frameworks (LangChain, LangGraph, LlamaIndex, and a proposed NVIDIA NeMo Agent Toolkit memory backend).
- **Previously:** Venmo (ML engineering lead — graph learning for search & recommendations), Piaggio Fast Forward (computer vision for the Gita robot), Dephy (controls & ML for wearable robotics).

## Site

Built with the [Hugo](https://gohugo.io/) static site generator using the [Ananke](https://github.com/theNewDynamic/gohugo-theme-ananke) theme. Deployed to GitHub Pages via the workflow in `.github/workflows/hugo.yaml`.

```bash
# install Hugo (extended), then:
hugo server -D   # local preview
hugo             # build to ./public (git-ignored)
```

`public/` and `resources/_gen/` are build artifacts and are excluded from version control.
