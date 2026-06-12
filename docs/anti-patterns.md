# Anti-Patterns

This repository is designed around a small set of failure modes that repeatedly show up in long-running AI systems.

## Governance theater

Symptoms:

- lots of coordination;
- lots of fresh notes;
- little source opening;
- few evidence rows.

Why it is dangerous:

The system spends budget managing itself instead of moving the real target forward.

## Memory-first operation

Symptoms:

- summaries are trusted more than ledgers or source locators;
- recent notes are treated like ground truth;
- continuation depends on recollection rather than files.

Why it is dangerous:

Recovery degrades and subtle mistakes get amplified.

## Multi-agent status loops

Symptoms:

- many threads re-affirming each other;
- duplicate audits;
- high liveness with low evidence.

Why it is dangerous:

The control layer becomes the main product.

## Thin closure

Symptoms:

- one complex task becomes one placeholder row;
- one rich artifact becomes one headline metric;
- one label replaces a whole process chain;
- incomplete work is promoted because revisiting feels expensive.

Why it is dangerous:

The system appears efficient while silently losing obligation depth.

## Candidate inflation

Symptoms:

- early signals get counted as solved evidence;
- hints become closure;
- early seeds get presented as if they were validated outputs.

Why it is dangerous:

Coverage looks better than it really is, and downstream analysis starts from a distorted base.

## Freshness-only health claims

Symptoms:

- health is inferred from timestamps alone;
- leases and heartbeats are treated as success;
- status churn is mistaken for real motion.

Why it is dangerous:

Freshness says a process ran. It does not prove a problem got solved.
