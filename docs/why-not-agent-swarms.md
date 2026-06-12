# Why Not Agent Swarms By Default

This repository is not anti-agent.

It is anti-unjustified orchestration.

## The short answer

Extra agents are worth having only when they solve a real problem that a simpler loop cannot solve.

In long-running workflows, more agents often create:

- more notes;
- more coordination;
- more implied progress;
- more token spend;
- more opportunities for liveness to masquerade as usefulness.

## The main risk

The biggest risk is not that a workflow stops.

It is that a workflow keeps moving in ways that look sophisticated while the real task advances slowly.

This is why the repository defaults to:

- one primary execution thread;
- compact file-backed state;
- small validators;
- recovery-only fallback automation.

## When more agents do make sense

More lanes can be useful when:

- ownership really can go stale;
- a mature repetitive path needs recovery;
- audit or triage can happen cheaply and safely;
- one agent is not enough to keep a workflow recoverable.

The burden of proof should stay on complexity.

## The design stance

This project prefers:

- fewer active control lanes;
- stronger truth surfaces;
- exact handoffs;
- validators that fail on fake progress.

That is why the project reads more like a control plane than a swarm framework.
