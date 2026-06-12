# Evolution

This playbook came from repeated long-haul AI work where continuity mattered, but token waste mattered too.

## Stage 1: one long working thread

The earliest useful setup was one long conversation doing real work directly.

Why it helped:

- low orchestration overhead;
- continuity by default;
- strong pressure toward source-level work;
- easy ownership.

Why it eventually broke:

- context became too large;
- too much state lived in conversation memory;
- recovery after interruption became fragile.

## Stage 2: detached automation expansion

The next move was to add more roles:

- planner;
- executor;
- watchdog;
- status sync;
- current-thread audit;
- heartbeat and health checks.

This improved survivability, but it also introduced a hidden cost. Support lanes could keep producing notes, leases, and status refreshes without matching evidence growth.

That is the dangerous failure mode:

- the system looks alive;
- timestamps stay fresh;
- multiple threads keep moving;
- but source-backed progress per token declines.

## Stage 3: hard-gated control

The next improvement was not more orchestration. It was stronger truth constraints:

- hard gates tied to outputs;
- anti-simplification rules;
- explicit start gates before execution;
- method notes before method-sensitive work;
- required closure states instead of accidental blanks.

This forced the system to distinguish:

- freshness from progress;
- candidate seeds from completed evidence;
- output existence from output content.

## Stage 4: primary-thread execution

The stable form turned out to be simpler:

- keep the file-backed continuity surfaces;
- keep the validators and hard gates;
- keep exact handoff notes;
- pause detached automations by default;
- let one active primary thread own the main path.

That design preserves continuity and recoverability while removing most orchestration theater.

## The key lesson

Long-haul autonomy does not just fail by stopping.

It also fails by looking continuously active while yielding poor evidence per token.

A durable architecture must optimize for both:

- continuity;
- anti-theater progress control.
