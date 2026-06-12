# Final Architecture

## Core principle

One active primary thread should be the primary worker.

Everything else should either support that worker or stay quiet.

## Primary lane

The primary thread should:

1. Read the compact truth surface.
2. Choose one bounded task that matters.
3. Open real source assets or factual ledgers.
4. Write source-backed outputs.
5. Run a focused validator or hard gate.
6. Update compact continuation files.
7. Continue directly when the next bounded task is already clear.

## Fallback lane

Detached automation is useful only for recovery cases such as:

- stale-frontier recovery;
- broken ownership recovery;
- compact audit refresh;
- mature repetitive work that already has a safe method and validator.

The default state for fallback automation should be paused.

## Minimal truthful file surface

A small reusable truth surface is usually enough:

- `AUTONOMY_TRUTH_SURFACE.json`
- `NEXT_CONTINUE_EXACTLY_FROM_HERE.md`
- `JUDGE_AUDIT.md`
- `METHOD_LEARNING.md`
- `HARD_GATE_STATE.json`

Optional surfaces such as leases or runtime traces should exist only when they solve a real coordination problem.

## Required properties

### Source-level progress

A round counts as substantive only if it touches at least one of:

- source files;
- extracted source text;
- structured factual ledgers;
- repair rows;
- validator-backed outputs built from those assets.

### Exact continuation

The handoff note should name:

- the exact next file, row, queue item, or source;
- the exact files to open next;
- the blocker if work cannot continue.

### Monotonic next-step logic

The next-step pointer should not drift backward casually. If it changes direction, the reason should be written down.

### Compact but meaningful validation

Validators should answer:

- did we write real outputs;
- did required states close;
- did the real gap shrink;
- did the system only look busy.

## Recommended loop

### Step A: short read first

Read the compact surfaces first. Do not start every turn by re-reading the entire repository.

### Step B: bounded work item

Pick one task that is:

- narrow enough to finish honestly;
- important enough to matter;
- local enough to verify.

### Step C: source opening

Open the actual assets. This is where many fake systems fail because they never leave the control plane.

### Step D: evidence outputs

Prefer:

- structured rows;
- repair rows;
- closure rows;
- uncertainty rows;
- negative-result rows;
- trace data;
- explicit failure rows.

### Step E: validator run

Run a small truthful validator, not a ceremonial one.

### Step F: writeback

Update:

- the hard gate;
- the audit note;
- the method-learning note;
- the exact continuation note.

## When to wake automation

Automation is justified only if at least one of these is true:

- the primary thread is stale;
- the ownership surface is broken;
- a mature repetitive path can run safely with low supervision;
- the active worker is unavailable and recovery should continue.

If none of those are true, automation should exit quickly.
