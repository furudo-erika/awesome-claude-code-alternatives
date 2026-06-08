# Awesome Open Source Claude Code Alternatives

A practical guide to open-source alternatives to Claude Code for developers who
want a terminal agent, editor agent, local workflow agent, or self-hosted coding
agent platform.

Claude Code set the shape of the modern agentic coding workflow: open a repo,
ask for a change, let the agent inspect files, edit code, run shell commands,
read failures, and iterate. This list covers tools with a similar workflow and
agent code that developers can inspect, fork, extend, or self-host.

Last checked: June 2026.

> Building AI apps with Claude Code, Codex, or your favorite API client?
>
> Try **[Blackmagic AI](https://blackmagic.engineering/?utm_source=github&utm_medium=awesome-list&utm_campaign=claude-code-alternatives&utm_content=cta-text)**, an OpenAI-compatible gateway and cheaper OpenRouter alternative. Use one API key, prepaid credits, and top models while cutting AI model costs by up to 50%.
>
> **[Compare model pricing](https://blackmagic.engineering/models?utm_source=github&utm_medium=awesome-list&utm_campaign=claude-code-alternatives&utm_content=cta-pricing)**

[<img width="1490" height="915" alt="Blackmagic AI OpenAI-compatible gateway dashboard" src="https://github.com/user-attachments/assets/af41beba-3fe0-4409-bfd6-03c6617a6ab1" />](https://blackmagic.engineering/?utm_source=github&utm_medium=awesome-list&utm_campaign=claude-code-alternatives&utm_content=cta-image)

## What Counts As A Claude Code Alternative?

This is not a generic list of autocomplete plugins. A Claude Code alternative
should understand repository context, plan a change, edit files, run commands
or tests, respond to errors, and keep the human in control of risky operations.
The best projects also support model choice, local execution, custom rules, MCP
tools, sandboxing, and auditable logs.

This list favors tools that are open source, documented, and useful for real
software work. Some are terminal-first. Some live in editors or desktop apps.
Some are better for research or internal platforms than daily pair programming.

## Quick Comparison

| Project | Surface | Best For |
| --- | --- | --- |
| [OpenAI Codex CLI](https://github.com/openai/codex) | Terminal, IDE, desktop app | A polished terminal coding agent with an Apache-2.0 client and OpenAI model path |
| [OpenCode](https://opencode.ai/) | Terminal, IDE, desktop app | Provider-flexible Claude Code-like workflows with sessions, LSP context, and local privacy |
| [Aider](https://github.com/aider-ai/aider) | Terminal | Git-native pair programming, reliable diffs, repo maps, commits, linting, and tests |
| [Cline](https://github.com/cline/cline) | VS Code, JetBrains, CLI, SDK | Human-approved autonomous edits, Plan/Act workflow, tools, MCP, and multi-agent work |
| [Kilo Code](https://kilo.ai/docs/getting-started) | IDE, terminal, browser, cloud | Multi-surface open-source coding with many model providers and team workflows |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli) | Terminal, GitHub Actions, IDE companion | A Google-backed open-source terminal agent with Gemini auth and MCP support |
| [Qwen Code](https://github.com/QwenLM/qwen-code) | Terminal, IDE integrations | Qwen-optimized terminal agent with multi-provider auth and Claude Code-like skills |
| [Continue](https://github.com/continuedev/continue) | CLI, IDE, CI checks | Source-controlled AI checks, PR automation, and open-source coding infrastructure |
| [Goose](https://github.com/aaif-goose/goose) | Desktop, CLI, API | Local workflow automation across code, tools, APIs, MCP extensions, and many models |
| [OpenHands](https://www.openhands.dev/) | Self-hosted/cloud platform | Cloud coding agents, Docker or Kubernetes isolation, team governance, and auditability |
| [mini-SWE-agent](https://mini-swe-agent.com/) | CLI, Python framework | Minimal, hackable issue-solving agent for research, benchmarks, and command-line tasks |

## Terminal-First Agents

### OpenAI Codex CLI

[Codex CLI](https://github.com/openai/codex) is OpenAI's open-source coding
agent that runs locally in the terminal. It is a close alternative to Claude
Code when you want a single command-line loop that can read code, edit files,
run commands, and work inside the repo you already have checked out. The client
is Apache-2.0 licensed, installs through npm, Homebrew, shell scripts, or
release binaries, and can use ChatGPT sign-in or API-key setup.

Choose Codex CLI if your team is comfortable with OpenAI models and wants a
well-maintained terminal agent with a predictable local execution model. It is
less model-agnostic than some community tools, but it is one of the strongest
open-source clients for developers who want a Claude Code-style shell workflow.

### OpenCode

[OpenCode](https://opencode.ai/) is one of the most direct open-source Claude
Code alternatives. It runs in the terminal, has IDE and desktop surfaces, and
supports many providers rather than forcing one model vendor. Its public site
highlights multi-session workflows, LSP-aware repository context, free included
models, existing ChatGPT or GitHub Copilot login paths, and local or hosted
model support.

Choose OpenCode if you want the closest open-source, terminal-native feeling to
Claude Code while keeping provider choice. It is especially useful when you run
multiple agents side by side, work across many repos, or want a coding agent
that can follow your shell habits instead of replacing them with a new IDE.

### Aider

[Aider](https://github.com/aider-ai/aider) is a terminal pair programmer rather
than a full autonomous teammate. That is a strength. It maps your codebase,
edits files, commits changes, works across many programming languages, can use
cloud or local models, and can run linters and tests after edits.

Use Aider when you want disciplined, git-friendly collaboration. It is less
flashy than some autonomous agents, but it is easy to reason about: you select
the files, describe the change, inspect the diff, and keep normal Git tooling in
charge. For many production repos, that lower autonomy is exactly the right
tradeoff.

### Gemini CLI

[Gemini CLI](https://github.com/google-gemini/gemini-cli) is Google's
open-source terminal agent. It brings Gemini into an interactive command-line
environment with file operations, shell commands, web fetching, MCP support,
custom context files, checkpointing, headless mode, GitHub Actions integration,
and Apache-2.0 licensing.

Choose Gemini CLI if your organization already uses Google Cloud, Gemini Code
Assist, or Gemini API keys. It is not model-neutral in the same way as OpenCode
or Aider, but it is a serious open-source option for teams that want a supported
Gemini-native agent.

### Qwen Code

[Qwen Code](https://github.com/QwenLM/qwen-code) is an open-source terminal
agent optimized for Qwen models. It has a Claude Code-like workflow, built-in
skills and subagents, optional IDE integrations, and support for OpenAI,
Anthropic, Gemini-compatible APIs, OpenRouter, Fireworks, Alibaba Cloud, or
bring-your-own API keys.

The current caveat is authentication: the Qwen OAuth free tier was discontinued
on April 15, 2026, so new users should expect to configure a paid plan, router,
or provider key. Choose Qwen Code when you specifically want to evaluate Qwen
models in an agentic shell.

## Editor And Multi-Surface Agents

### Cline

[Cline](https://github.com/cline/cline) is an open-source coding agent in your
IDE and terminal. It supports VS Code, a CLI, an SDK, a Kanban-style multi-agent
task board, and a JetBrains experience. The agent can create files, edit across
the project, run commands, browse the web, use MCP servers, and ask for approval
before changing code or executing commands.

Choose Cline if you want Claude Code-like autonomy with stronger visual review.
Its Plan and Act workflow is useful for teams that want the agent to inspect
first, propose a strategy, and only then start editing. Also note the nuance:
the main project is open source, but the repository currently says the
JetBrains plugin is not open-sourced.

### Kilo Code

[Kilo Code](https://kilo.ai/docs/getting-started) is an open-source coding
assistant that works across IDE, terminal, browser, and cloud surfaces. Its docs
position it as an inspectable, forkable assistant that can generate code,
automate reviews, debug issues, and understand a codebase. The current platform
also emphasizes access to hundreds of models through its gateway.

Choose Kilo Code if you want a broad, productized open-source platform rather
than a single terminal binary. It makes the most sense for users who want one
agent workflow across VS Code, JetBrains, CLI, browser, cloud sessions, review,
and team automation.

### Continue

[Continue](https://github.com/continuedev/continue) has evolved from an
open-source IDE assistant into a broader AI engineering platform. Current docs
emphasize source-controlled AI checks on pull requests, with an open-source CLI
powering enforceable GitHub status checks.

Choose Continue when your main pain is code review, policy checks, CI feedback,
and repeatable AI rules rather than an interactive Claude Code clone.

## Workflow And Platform Agents

### Goose

[Goose](https://github.com/aaif-goose/goose) is a local open-source agent now
under the Agentic AI Foundation. It offers desktop, CLI, and API surfaces for
code, workflows, research, data analysis, and automation. It supports many model
providers and connects to MCP extensions for tools such as GitHub, databases,
and internal APIs.

Choose Goose when coding is only part of the job. It is useful for developers
who want a local agent that can operate across the repo, terminal, docs, tickets,
and external services while keeping the agent runtime inspectable.

### OpenHands

[OpenHands](https://www.openhands.dev/) is an open platform for cloud coding
agents. It targets platform teams that want isolated Docker or Kubernetes
environments, access control, auditability, and integrations with GitHub,
GitLab, CI/CD, Slack, ticketing systems, and preferred model providers.

Choose OpenHands when you want an internal agent platform rather than an
individual developer tool. It is heavier than Claude Code, but it offers a more
appropriate shape for organizations that need governance, scale, and repeatable
agent environments.

### mini-SWE-agent

[mini-SWE-agent](https://mini-swe-agent.com/) is a minimal agent from the team
behind SWE-agent and SWE-bench. It is designed to solve GitHub issues or help in
the command line with radically simple control flow, broad model compatibility
through providers such as LiteLLM and OpenRouter, and support for local or
sandboxed environments.

Choose mini-SWE-agent if you are building, studying, or benchmarking coding
agents. It is not the most polished daily pair programmer, but it is excellent
for understanding what an agent scaffold actually needs.

## Choosing The Right Tool

Pick OpenCode, Codex CLI, Gemini CLI, or Qwen Code for terminal-first work.
Pick Cline or Kilo Code for editor review and multi-surface workflows. Pick
Aider for conservative git-native pair programming. Pick Continue for AI checks
encoded in the repo. Pick Goose, OpenHands, or mini-SWE-agent for broader agent
infrastructure, workflow automation, or research harnesses.

The best open-source Claude Code alternative is not always the most autonomous
one. For production work, the key questions are simpler: can you inspect what it
will do, restrict what it can touch, choose the model, capture logs, run tests,
undo changes, and keep your repository rules as the source of truth?

## Contributing

Add projects that are active, documented, and open enough for developers to
inspect or fork. Include the license, supported surfaces, model support, install
path, safety model, and caveats around hosted services, telemetry, pricing,
provider lock-in, or sunset status.
