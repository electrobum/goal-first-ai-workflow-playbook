# Use Cases

This playbook is generic on purpose. It is meant to adapt to different long-running AI workflows without being tied to one domain.

## 1. Agentic coding workflows

Use it when:

- one task spans many files or many sessions;
- regressions need focused validation;
- code changes are easy to make but easy to overclaim.

Why it helps:

- exact handoffs reduce restart time;
- validators can stay tied to tests, builds, or real outputs;
- multiple helper loops are less likely to drift into status theater.

## 2. Documentation and knowledge workflows

Use it when:

- documentation gets updated over multiple sessions;
- review and accuracy matter more than speed alone;
- stale summaries create confusion.

Why it helps:

- the truth surface keeps the current target visible;
- the handoff note points to the exact next file;
- the hard gate can require verified examples, not just rewritten prose.

## 3. Operations and internal automation

Use it when:

- workflows need to run for days or weeks;
- interruptions are common;
- ownership needs to stay clear.

Why it helps:

- compact files keep continuity durable;
- one primary thread reduces duplicated work;
- fallback automation can focus on recovery instead of pretending to be the main engine.

## 4. Review and evaluation loops

Use it when:

- the workflow repeatedly checks quality, compliance, or completion;
- progress tends to be over-reported;
- teams need better evidence of closure.

Why it helps:

- validators can stay narrow and honest;
- candidate inflation becomes easier to detect;
- fake-complete states become harder to maintain.

## 5. Long-lived assistants

Use it when:

- an assistant has to continue work across many sessions;
- context windows are not enough to hold reliable state;
- memory notes alone are no longer trustworthy.

Why it helps:

- file-backed continuation becomes the real source of truth;
- the next step remains exact even after interruptions;
- method learning accumulates outside the conversation itself.

## Where not to overuse it

This playbook is probably too much for:

- one-shot prompting tasks;
- tiny scripts with no real continuation need;
- purely disposable experiments;
- workflows with no meaningful validation step.

It is most valuable when the cost of confusion, drift, or restart is already visible.
