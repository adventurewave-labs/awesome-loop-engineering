# Awesome Loop Engineering [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Prompt engineering → context engineering → harness engineering → **loop engineering**.

A curated list of resources for designing autonomous AI agent loops — the discipline of running coding agents in self-feeding cycles (Ralph and beyond): loop patterns, runners, orchestrators, memory strategies, stop conditions, and safety.

*"I don't prompt Claude anymore. I have loops running that prompt Claude and figure out what to do. My job is to write loops."* — Boris Cherny, creator of Claude Code

## Contents

- [The Canon](#the-canon)
- [Patterns & Techniques](#patterns--techniques)
- [Loop Runners & Orchestrators](#loop-runners--orchestrators)
- [Multi-Agent Loop Systems](#multi-agent-loop-systems)
- [Harnesses & SDKs](#harnesses--sdks)
- [Articles & Deep Dives](#articles--deep-dives)
- [Related Lists](#related-lists)

## The Canon

- [everything is a ralph loop](https://ghuntley.com/loop/) - Geoffrey Huntley's foundational essay. The bash loop that started it: allocate specs, set a goal, loop the goal.
- [how-to-ralph-wiggum](https://github.com/ghuntley/how-to-ralph-wiggum) - Huntley's reference repo for the Ralph Wiggum Technique.
- [Inventing the Ralph Wiggum Loop](https://devinterrupted.substack.com/p/inventing-the-ralph-wiggum-loop-creator) - Dev Interrupted interview with Huntley on how dumb loops + deterministic context allocation change the unit economics of code. ([podcast episode](https://linearb.io/dev-interrupted/podcast/inventing-the-ralph-wiggum-loop))
- [ralph-wiggum.ai](https://ralph-wiggum.ai/) - The viral loop, simplified for teams.
- [Loop Engineering](https://addyosmani.com/blog/loop-engineering/) - Addy Osmani's essay that named the discipline and gave it an anatomy: automations, worktrees, skills, connectors, sub-agents, and durable external state.
- [Stop prompting, design loops](https://x.com/steipete/status/2063697162748260627) - Peter Steinberger's one-line reframe (creator of OpenClaw): you shouldn't be prompting coding agents anymore — you should be designing loops that prompt them.
- [How the agent loop works](https://code.claude.com/docs/en/agent-sdk/agent-loop) - Anthropic's official docs on the inner loop: evaluate → tool call → result → repeat.

## Patterns & Techniques

- [The Ralph Wiggum Loop: Autonomous Code Generation with Fresh Context](https://www.codecentric.de/en/knowledge-hub/blog/the-ralph-wiggum-loop-autonomous-code-generation-with-a-fresh-context) - Why fresh context every iteration is the point, not a side effect: filesystem as memory, one task per iteration, exit for a clean window.
- [Agentic Engineering Protocols: The Ralph Wiggum Loop](https://dwmkerr.com/ralph-wiggum-loop/) - Loop as protocol: spec comparison, IMPLEMENTATION_PLAN.md as prioritized queue, commit-per-iteration.
- [Ralph Wiggum pattern](https://path.kilo.ai/introduction/patterns/ralph-wiggum/) - Pattern-catalog treatment: when to reach for a loop vs a single session.
- [The Ralph Loop: How Recursive AI Agents Actually Work](https://thomas-wiegold.com/blog/ralph-loop-how-recursive-ai-agents-work/) - Mechanics of recursion via restart: plan files, DONE sentinels, retry-with-fresh-context.
- [Ralph Wiggum Loop notes](https://prg.sh/notes/Ralph-Wiggum-Loop) - Condensed field notes on the loop lifecycle.
- [Agentic Coding Framework: Build the Agent Loop](https://www.buildmvpfast.com/blog/harness-engineering-agent-loop-agentic-coding-framework-2026) - The progression from harness engineering to loop engineering: the harness on a timer, spawning helpers, feeding itself.

## Loop Runners & Orchestrators

- [loopgen-rs](https://github.com/adventurewave-labs/loopgen-rs) - Agentic loop runner for Claude Code, in Rust. *(ours)*
- [ralph-orchestrator](https://github.com/mikeyobrien/ralph-orchestrator) - Production-minded Ralph implementation: safety limits, monitoring, cost controls, multiple backends. ([docs](https://mikeyobrien.github.io/ralph-orchestrator/))
- [ralphex](https://github.com/umputun/ralphex) - Standalone CLI that orchestrates Claude Code or Codex through implementation plans from your repo root — no IDE plugins, no cloud.
- [ralph-loop-agent](https://github.com/vercel-labs/ralph-loop-agent) - Vercel Labs' "Continuous Autonomy for the AI SDK."
- [continuous-claude](https://github.com/AnandChowdhary/continuous-claude) - Ralph loop with PRs: create PR → wait for checks → merge → repeat. CI/CD-shaped autonomy.
- [ralph](https://github.com/snarktank/ralph) - Loop until every PRD item is complete.
- [ralph-loop](https://github.com/PageAI-Pro/ralph-loop) - Long-running task-list loop; AI coding for days at a time.
- [autoloop](https://github.com/yaoshengzhe/autoloop) - Autonomous-iteration plugin for agentic tools: keeps running until the task is done.
- [agentic-loop](https://github.com/allierays/agentic-loop) - RALPH + PRD-driven development toolkit; `npx agentic-loop run`.
- [loop-maker](https://github.com/EricTechPro/loop-maker) - Interviews you, then scaffolds a self-running loop with verifier, state file, and human gate. Cross-harness (Claude Code / Codex / Hermes / OpenClaw).

## Multi-Agent Loop Systems

- [gastown](https://github.com/gastownhall/gastown) - Gas Town, via Steve Yegge: if Ralph is one agent looping, Gas Town is a community of them — a workspace manager coordinating fleets of coding agents across tasks.
- [turbo-flow](https://github.com/marcuspat/turbo-flow) - Agentic dev environment running 60+ subagents with SPARC methodology; loop-native by design. *(ours)*

## Harnesses & SDKs

- [Claude Agent SDK agent loop](https://code.claude.com/docs/en/agent-sdk/agent-loop) - Embed the Claude Code loop in your own applications: programmatic control over tools, permissions, cost limits.
- [Top Agent Harnesses](https://aimultiple.com/agent-harness) - Survey of the harness layer your loop runs inside.

## Articles & Deep Dives

- [Claude Code Loop Engineering: Stop Prompting, Start Designing Autonomous Agent Workflows](https://www.techtimes.com/articles/318828/20260622/claude-code-loop-engineering-stop-prompting-start-designing-autonomous-agent-workflows.htm) - The case for loop engineering as its own discipline.
- [What is Ralph Loop? A New Era of Autonomous Coding](https://medium.com/@tentenco/what-is-ralph-loop-a-new-era-of-autonomous-coding-96a4bb3e2ac8) - Accessible introduction.
- [Ralph Wiggum CLI](https://deepakness.com/raw/ralph-cli/) - Notes on Huntley's CLI packaging of the technique.

## Related Lists

- [awesome-ralph](https://github.com/snwfdhmp/awesome-ralph) - Ralph-specific resources. Loop engineering is the superset; start here for Ralph depth.
- [awesome-harness-engineering](https://github.com/ai-boost/awesome-harness-engineering) - The layer below the loop: tools, evals, memory, MCP, permissions, observability.
- [awesome-agentic-patterns](https://github.com/nibzard/awesome-agentic-patterns) - Catalogue of production agentic patterns — the mini-architectures loops are assembled from.
- [awesome-cli-coding-agents](https://github.com/bradAGI/awesome-cli-coding-agents) - Terminal-native coding agents and the harnesses / parallel runners that drive autonomous loops.
- [awesome-agentic-engineering](https://github.com/jordimas/awesome-agentic-engineering) - Broader practical agentic-engineering reading; loop design sits inside it.
- [autonomous-coding topic](https://github.com/topics/autonomous-coding) - GitHub's live index.

## Contributing

PRs welcome — one link per PR, with a one-line description of *why it matters for loops* (not just "AI tool"). Dead links and marketing pages get pruned. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

Maintained by [Adventure Wave Labs](https://github.com/adventurewave-labs) — we also build [loopgen-rs](https://github.com/adventurewave-labs/loopgen-rs).

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)
