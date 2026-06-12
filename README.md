# Goal-First AI Workflow Playbook

Design patterns for long-running AI workflows that keep making real progress.

This repository is a compact, publish-ready playbook for building AI workflows that stay useful over time. It focuses on a simple but hard problem: how to keep an AI system moving across long tasks without letting it drift into summaries, heartbeats, and busy-looking automation that produces little real value.

The central idea is straightforward:

use one primary execution thread for real work, keep continuation state on disk, and enforce hard gates that measure outputs instead of activity.

## Why this exists

Most long-running AI systems do not fail because they stop immediately.

They fail because they keep looking active while real progress slows down.

Common symptoms:

- fresh notes keep appearing;
- multiple threads look alive;
- status files keep updating;
- handoff text keeps growing;
- but the actual task barely moves.

This repo distills a more durable alternative:

- one primary execution thread does the real work;
- compact files carry continuation truth across interruptions;
- hard gates measure outputs instead of freshness;
- fallback automations exist for recovery, not as the main work engine.

The result is a workflow that is easier to resume, easier to audit, and much harder to fake.

## Why it is useful

You can use this playbook if you are building:

- agentic coding workflows;
- document-processing pipelines;
- multi-step analysis systems;
- long-running assistants for operations or knowledge work;
- any AI loop where continuity matters more than one-shot prompting.

It is especially useful when you want:

- fewer orchestration layers;
- clearer handoffs;
- lower token waste;
- better recovery after interruption;
- stricter separation between activity and progress.

## What is included

- [docs/evolution.md](docs/evolution.md): how the operating model evolved from single-thread execution to automation-heavy orchestration and back to a leaner design.
- [docs/final-architecture.md](docs/final-architecture.md): the recommended architecture, loop, and wake conditions for automation.
- [docs/anti-patterns.md](docs/anti-patterns.md): common failure modes such as governance theater, candidate inflation, and memory-first drift.
- [docs/design-rules.md](docs/design-rules.md): publication-ready rules for start gates, closure states, validation, and anti-simplification.
- [docs/repository-positioning.md](docs/repository-positioning.md): recommended GitHub name, subtitle, topics, and framing.
- [principles/](principles): short standalone principles that can be linked or reused independently.
- [templates/](templates): reusable truth surfaces, handoff notes, audit notes, and hard-gate templates.
- [examples/](examples): two small examples showing how the templates work in practice.

## Core model

The recommended architecture is:

1. Read a compact truth surface first.
2. Pick one bounded real task.
3. Open actual source assets or factual ledgers.
4. Write evidence rows or other source-backed outputs.
5. Run a focused validator or hard gate.
6. Write an exact continuation note.
7. Only wake automation if the primary worker is stale, unavailable, or the control surface needs recovery.

This approach is intentionally conservative about what counts as progress.

Fresh timestamps are not progress.
More notes are not progress.
More agents are not progress.

Real progress means the system changed something that matters and left enough evidence for the next worker to continue correctly.

## Quick start

1. Read [docs/final-architecture.md](docs/final-architecture.md).
2. Copy the files in [templates/](templates) into your own project.
3. Fill in a real `AUTONOMY_TRUTH_SURFACE.json`, `HARD_GATE_STATE.json`, and `NEXT_CONTINUE_EXACTLY_FROM_HERE.md`.
4. Keep your validator tied to real outputs, not heartbeat freshness.
5. Use the examples as small reference implementations for your own workflow.

## What this repo does not claim

This project is intentionally anti-hype. It does not claim:

- universal autonomy;
- fully self-driving work with no oversight;
- guaranteed correctness;
- a magic multi-agent controller;
- a domain-independent replacement for real validation.

It is a practical system design playbook for making AI workflows more durable, inspectable, and useful.

## Suggested GitHub settings

Recommended repository names:

- `goal-first-ai-workflow-playbook`
- `goal-first-autonomy`
- `ai-workflow-continuity-playbook`

Suggested GitHub topics:

- `ai-autonomy`
- `workflow-design`
- `agentic-systems`
- `prompt-engineering`
- `human-in-the-loop`
- `operations`
- `ai-workflows`
- `knowledge-work`
- `automation`
- `playbook`

## License

[MIT](LICENSE)
