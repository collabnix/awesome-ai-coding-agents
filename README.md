# Awesome AI Coding Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![Stars](https://img.shields.io/github/stars/ajeetraina/awesome-ai-coding-agents?style=social)](https://github.com/ajeetraina/awesome-ai-coding-agents/stargazers)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
[![Discord](https://img.shields.io/badge/Discord-Collabnix-5865F2?logo=discord&logoColor=white)](https://launchpass.com/collabnix)
[![Last updated](https://img.shields.io/badge/updated-2026--10--31-informational)](#)

> A curated list of **AI coding agents** - the tools that read, write, run, test and ship code with you or for you. Terminal CLIs, IDE copilots, autonomous cloud engineers, agent frameworks and the harnesses that keep them safe.

An *AI coding agent* is more than autocomplete: it plans a task, edits files across a repo, runs commands, reads the results and iterates - often behind a review step or inside a sandbox. This list sorts the fast-moving field into categories, states plainly what each tool is, and flags how it runs (local, cloud, or sandboxed).

- 🖥️ **Terminal CLIs** - agents that live in your shell
- 🧩 **IDE & editor agents** - copilots embedded in VS Code, JetBrains, Zed and beyond
- ☁️ **Autonomous & cloud agents** - fire-and-forget software engineers that work async on a VM
- 🛠️ **Frameworks & SDKs** - build your own coding agent
- 🔒 **Sandboxes & harnesses** - run untrusted agents without handing over the keys

> **Legend** - `OSS` open source · `$` paid/commercial · `freemium` free tier + paid · `local` runs on your machine · `cloud` runs on a hosted VM

---

## Contents

- [Terminal / CLI Agents](#terminal--cli-agents)
- [IDE & Editor Agents](#ide--editor-agents)
- [Autonomous & Cloud Agents](#autonomous--cloud-agents)
- [Code Review & PR Agents](#code-review--pr-agents)
- [Agent Frameworks & SDKs](#agent-frameworks--sdks)
- [Sandboxes & Runtime Harnesses](#sandboxes--runtime-harnesses)
- [Self-Hosted & Open Models](#self-hosted--open-models)
- [The Docker Agent that curates this list](#the-docker-agent-that-curates-this-list)
- [Recently discovered (auto-added, unreviewed)](#recently-discovered-auto-added-unreviewed)
- [Contributing](#contributing)
- [License](#license)

---

## Terminal / CLI Agents

Agents that run in your terminal, edit files in place, and execute commands in your working directory.

- [**Claude Code**](https://github.com/anthropics/claude-code) - Anthropic's agentic CLI (also in VS Code/JetBrains and the web). Plans multi-step tasks, edits across a repo, runs tools, and supports hooks, subagents, MCP servers and skills. `$` `freemium` `local`
- [**OpenAI Codex CLI**](https://github.com/openai/codex) - OpenAI's open-source coding agent for the terminal, with default-on sandboxing (Seatbelt on macOS, Landlock + seccomp on Linux). Pairs with the Codex cloud agent. `OSS` `$` `local`
- [**Gemini CLI**](https://github.com/google-gemini/gemini-cli) - Google's open-source terminal agent backed by Gemini, with a large context window, MCP support, and Seatbelt/Docker/Podman sandbox modes. `OSS` `freemium` `local`
- [**Aider**](https://github.com/Aider-AI/aider) - Pair-programming in your terminal with git-aware edits and automatic commits. Model-agnostic (Claude, GPT, DeepSeek, local). A long-standing favourite. `OSS` `local`
- [**OpenCode**](https://github.com/sst/opencode) - Provider-agnostic terminal agent from the SST team, with a polished TUI and a client/server architecture. `OSS` `local`
- [**Goose**](https://github.com/block/goose) - Block's open-source, on-machine agent (CLI + desktop) built around MCP extensions; works with any LLM. `OSS` `local`
- [**Amazon Q Developer CLI**](https://github.com/aws/amazon-q-developer-cli) - AWS's agentic CLI for the terminal, with inline completions, `/` commands and AWS-aware context. `freemium` `local`
- [**Qwen Code**](https://github.com/QwenLM/qwen-code) - A Gemini-CLI fork tuned for Alibaba's Qwen3-Coder models; strong on agentic, long-context repo tasks. `OSS` `local`
- [**Crush**](https://github.com/charmbracelet/crush) - Charm's glamorous terminal coding agent; multi-model, MCP-capable, LSP-aware. `OSS` `local`
- [**Plandex**](https://github.com/plandex-ai/plandex) - Terminal agent built for large, multi-file tasks with a persistent plan and diff-review sandbox before changes land. `OSS` `local`
- [**Mentat**](https://github.com/AbanteAI/mentat) - CLI assistant that coordinates edits across multiple files and locations from a single prompt. `OSS` `local`

## IDE & Editor Agents

Copilots and agents embedded directly in an editor.

- [**Cursor**](https://cursor.com) - The VS Code fork built around agentic editing; Agent mode, background agents, `.cursorrules` and a composer that spans your codebase. `$` `freemium` `local`
- [**GitHub Copilot**](https://github.com/features/copilot) - The original in-editor copilot, now with agent mode, chat, and a cloud coding agent that opens PRs. Works in VS Code, JetBrains, Neovim and more. `$` `freemium` `local` `cloud`
- [**Windsurf**](https://windsurf.com) - Formerly Codeium; an agentic IDE whose "Cascade" agent reasons over your whole workspace and runs commands. `$` `freemium` `local`
- [**Cline**](https://github.com/cline/cline) - Open-source autonomous agent for VS Code that plans, edits, runs terminal commands and uses MCP tools, with human-in-the-loop approval. `OSS` `local`
- [**Roo Code**](https://github.com/RooCodeInc/Roo-Code) - A feature-rich VS Code agent (a Cline fork) with customizable modes, multi-model support and MCP. `OSS` `local`
- [**Kilo Code**](https://github.com/Kilo-Org/kilocode) - Open-source VS Code agent that merges ideas from Cline and Roo; orchestrator modes and a built-in marketplace. `OSS` `local`
- [**Continue**](https://github.com/continuedev/continue) - Open-source IDE extension (VS Code + JetBrains) for building and running custom AI code assistants and agents. `OSS` `local`
- [**Zed**](https://github.com/zed-industries/zed) - High-performance Rust editor with a native agent panel, edit prediction and MCP support. `OSS` `local`
- [**JetBrains Junie**](https://www.jetbrains.com/junie/) - JetBrains' autonomous coding agent across IntelliJ, PyCharm and the rest of the IDE family. `$` `freemium` `local`
- [**Augment Code**](https://www.augmentcode.com) - Agent focused on large codebases, with a context engine that indexes big monorepos. `$` `local`
- [**Trae**](https://www.trae.ai) - ByteDance's AI IDE with a builder agent and multi-model backend. `freemium` `local`
- [**Tabnine**](https://www.tabnine.com) - Privacy-first completion and chat with an agent mode; supports self-hosting and air-gapped deployment. `$` `freemium` `local`
- [**Pythagora**](https://github.com/Pythagora-io/gpt-pilot) - (GPT Pilot) builds apps feature-by-feature with a human reviewing each step; also a VS Code extension. `OSS` `local`

## Autonomous & Cloud Agents

Fire-and-forget engineers that pick up a task (often a GitHub issue) and work asynchronously on a hosted VM, returning a PR.

- [**Devin**](https://devin.ai) - Cognition's autonomous software engineer; runs on its own cloud VM with a browser, shell and editor, and tackles tickets end-to-end. `$` `cloud`
- [**OpenAI Codex (cloud)**](https://openai.com/index/introducing-codex/) - Cloud agent that works in parallel sandboxes, reads your repo and opens PRs; the counterpart to the Codex CLI. `$` `cloud`
- [**GitHub Copilot coding agent**](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) - Assign an issue to Copilot and it spins up an ephemeral Actions-backed VM, works the task, and opens a PR for review. `$` `cloud`
- [**Google Jules**](https://jules.google) - Async coding agent that clones your repo into a Google Cloud VM, plans, and proposes PRs; backed by Gemini. `freemium` `cloud`
- [**Replit Agent**](https://replit.com/ai) - Builds and deploys full apps from a prompt entirely inside Replit's cloud workspace. `freemium` `cloud`
- [**Factory (Droids)**](https://factory.ai) - "Droids" that run across terminal, IDE and cloud for agent-driven software development at team scale. `$` `cloud` `local`
- [**Lovable**](https://lovable.dev) - Prompt-to-app builder that generates and deploys full-stack web apps from natural language. `freemium` `cloud`
- [**Bolt.new**](https://bolt.new) - StackBlitz's in-browser full-stack agent that builds, runs and deploys apps in a WebContainer. `freemium` `cloud`
- [**v0**](https://v0.dev) - Vercel's generative UI and app agent; prompt to React/Next.js components and deployable apps. `freemium` `cloud`
- [**Sweep**](https://github.com/sweepai/sweep) - Turns GitHub issues into PRs; started as an OSS bot, now also a JetBrains assistant. `cloud`
- [**Devlo / Codegen**](https://codegen.com) - Cloud SWE agents that act on issues, Slack and Linear and return reviewed PRs. `$` `cloud`
- [**Tembo (formerly Solver)**](https://www.tembo.io) - Autonomous agent that investigates and fixes issues across a codebase. `$` `cloud`
- [**Orbi**](https://github.com/orbi-build/orbi) - Self-hostable GitHub-issue agent with isolated worktrees, independent acceptance review, gated PR merges, and releases on request. [Website](https://orbi.build/?ref=dir-collabnix-awesome-agents). `OSS` `local`

## Code Review & PR Agents

Agents specialised in reviewing diffs, not writing features.

- [**CodeRabbit**](https://www.coderabbit.ai) - AI PR reviewer that posts line-by-line feedback, summaries and suggested fixes on every pull request. `$` `freemium` `cloud`
- [**Greptile**](https://www.greptile.com) - Codebase-aware PR review that reasons over the full graph of your repo. `$` `cloud`
- [**Qodo (formerly Codium)**](https://www.qodo.ai) - PR-Agent plus test generation and review; has a popular open-source PR-Agent. `OSS` `freemium` `cloud`
- [**Ellipsis**](https://www.ellipsis.dev) - Reviews PRs and can also fix the issues it finds by pushing commits. `$` `cloud`
- [**Bito**](https://bito.ai) - AI code review agent and IDE assistant with security and standards checks. `freemium` `cloud` `local`

## Agent Frameworks & SDKs

Build your own coding agent, or embed one in your product.

- [**Claude Agent SDK**](https://github.com/anthropics/claude-agent-sdk-python) - The toolkit behind Claude Code, exposed for building custom agents (Python & TypeScript) with tools, MCP, subagents and permissions. `OSS`
- [**OpenAI Agents SDK**](https://github.com/openai/openai-agents-python) - Lightweight framework for multi-agent workflows, handoffs and tool use. `OSS`
- [**LangGraph**](https://github.com/langchain-ai/langgraph) - Graph-based orchestration for stateful, long-running agents from the LangChain team. `OSS`
- [**Microsoft AutoGen**](https://github.com/microsoft/autogen) - Multi-agent conversation framework for building collaborating LLM agents. `OSS`
- [**CrewAI**](https://github.com/crewAIInc/crewAI) - Role-playing multi-agent framework for orchestrating teams of agents. `OSS`
- [**SWE-agent**](https://github.com/SWE-agent/SWE-agent) - Princeton's research agent that autonomously resolves GitHub issues; the reference implementation for SWE-bench. `OSS`
- [**OpenHands**](https://github.com/All-Hands-AI/OpenHands) - (formerly OpenDevin) a full open-source platform for agents that write code, run commands and browse the web. `OSS` `local` `cloud`
- [**GPT Engineer / gpt-engineer**](https://github.com/gpt-engineer-org/gpt-engineer) - Specify an app in natural language and have it generated; one of the original codegen agents. `OSS` `local`
- [**MetaGPT**](https://github.com/FoundationAgents/MetaGPT) - Multi-agent framework that assigns software-company roles (PM, architect, engineer) to LLMs. `OSS`
- [**Smol Developer**](https://github.com/smol-ai/developer) - A minimal "junior developer" agent you embed to scaffold whole codebases. `OSS`

## Sandboxes & Runtime Harnesses

Infrastructure to run coding agents safely - isolated kernels, network policy and credential brokering, so an autonomous agent can't wander off with your secrets.

- [**Docker Sandboxes (sbx)**](https://github.com/ajeetraina/awesome-docker-sbx) - Standalone CLI (`sbx`) that runs Claude Code, Codex, Gemini CLI and others inside isolated microVMs, each with its own kernel, Docker daemon, filesystem and network. See the companion [awesome-docker-sbx](https://github.com/ajeetraina/awesome-docker-sbx) and [awesome-sbx-kits](https://github.com/ajeetraina) lists. `OSS` `local`
- [**E2B**](https://github.com/e2b-dev/e2b) - Open-source cloud sandboxes (Firecracker microVMs) purpose-built for running AI-generated code and agents. `OSS` `cloud`
- [**Daytona**](https://github.com/daytonaio/daytona) - Secure, elastic infrastructure for running AI-generated code with sub-second sandbox startup. `OSS` `cloud`
- [**Modal Sandboxes**](https://modal.com) - Serverless containers for executing untrusted agent code with a Python-first API. `$` `cloud`
- [**Microsandbox**](https://github.com/microsandbox/microsandbox) - Self-hostable microVM sandboxes for running untrusted AI/user code locally. `OSS` `local`
- [**Northflank**](https://northflank.com) - Secure, scalable sandboxes and runtime for deploying AI agents and the apps they build. `$` `cloud`

## Self-Hosted & Open Models

Agents and completion servers you can run entirely on your own hardware.

- [**Tabby**](https://github.com/TabbyML/tabby) - Self-hosted, open-source coding assistant; a privacy-preserving Copilot alternative with no external dependencies. `OSS` `local`
- [**Ollama**](https://github.com/ollama/ollama) - Run open coding models (Qwen Coder, DeepSeek-Coder, Code Llama, etc.) locally; the backend many of the agents above can point at. `OSS` `local`
- [**Twinny**](https://github.com/twinnydotcom/twinny) - Free, private, fully local VS Code completion and chat extension that pairs with Ollama/llama.cpp. `OSS` `local`
- [**Refact.ai**](https://github.com/smallcloudai/refact) - Self-hostable AI agent and completion engine for the enterprise. `OSS` `local`

---

## The Docker Agent that curates this list

This repository is partly maintained by an autonomous **Docker Agent** - the same `docker agent run` pattern used in [awesome-docker-sbx](https://github.com/ajeetraina/awesome-docker-sbx). A scheduled GitHub Action installs the Docker Agent CLI plugin, then runs a curator agent that:

1. Searches GitHub and the web for newly released AI coding agents, tools and posts.
2. Judges each candidate for relevance, maturity and how it handles credentials.
3. Opens a tracking **issue** per find (label `agent-bot`).
4. Appends accepted entries to the **[Recently discovered](#recently-discovered-auto-added-unreviewed)** section via a single auto-merged **PR** - never touching the hand-curated sections above and never pushing to `main` directly.

A human then promotes the good finds into the curated sections. The agent definition lives in [`workflow/auto-curator-agent/curator.yaml`](./workflow/auto-curator-agent/curator.yaml) and the schedule in [`.github/workflows/agent-auto-curator.yml`](./.github/workflows/agent-auto-curator.yml).

**Credentials.** The curator's primary model is OpenAI's `gpt` provider, authenticated from the `OPENAI_API_KEY` repository secret. A free NVIDIA-hosted Nemotron model is wired as a documented fallback. All GitHub work (search, labels, issues, PR, merge) runs on the workflow's built-in `GITHUB_TOKEN` - no personal access token required.

| Secret | Used for |
| --- | --- |
| `OPENAI_API_KEY` | **Required.** Primary model (platform.openai.com key with billing) |
| `NVIDIA_API_KEY` | Optional free fallback model (build.nvidia.com) |
| `ANTHROPIC_API_KEY` | Optional, if you switch the agent to a Claude model |

The only repo setting needed is **Settings → Actions → General → Workflow permissions → "Read and write permissions"** plus **"Allow GitHub Actions to create and approve pull requests"** (the workflow also declares `contents`, `issues` and `pull-requests: write` explicitly).

Run it locally with:

```bash
docker agent run --yolo ./workflow/auto-curator-agent/curator.yaml \
  "Scan GitHub and the web for new AI coding agents from the last 7 days."
```

---

## Recently discovered (auto-added, unreviewed)

> Entries below are added automatically by the Docker curator agent and have **not** been human-reviewed. Promote the good ones into the curated sections above via a PR.

_None yet - the curator will populate this on its first scheduled run._

---

## Contributing

Contributions are very welcome! Please:

1. Keep entries **factual and neutral** - this is a reference, not marketing.
2. Use the format: `- [**Name**](url) - one-line description of what it is. tags`
3. Put each tool in the category that best matches how it runs.
4. Note how an agent handles code execution and credentials where relevant (local, sandboxed, cloud).
5. One entry per PR for new tools; dedupe by URL.

Open a PR or an issue. See [the Awesome manifesto](https://github.com/sindresorhus/awesome/blob/main/awesome.md) for guidance on what belongs on an awesome list.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work. See [LICENSE](./LICENSE).
