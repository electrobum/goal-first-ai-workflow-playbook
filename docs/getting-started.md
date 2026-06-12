# Getting Started

This guide is the fastest path from "interesting idea" to "usable workflow."

## The goal

You do not need to adopt every file in this repository at once.

You only need enough structure to answer four questions reliably:

1. What is the workflow trying to do right now?
2. What real output changed last?
3. What exact task comes next?
4. How do we know the workflow is making real progress instead of staying busy?

## The minimum setup

Start with these files:

- `AUTONOMY_TRUTH_SURFACE.json`
- `NEXT_CONTINUE_EXACTLY_FROM_HERE.md`
- `HARD_GATE_STATE.json`

Then add:

- `JUDGE_AUDIT.md`
- `METHOD_LEARNING.md`

Use the versions in [templates/](../templates) as your starting point.

## The minimum loop

Use this loop first before adding anything fancier:

1. Read the truth surface.
2. Pick one bounded task.
3. Open the real assets.
4. Produce a real output.
5. Run a validator.
6. Update the continuation note.

If you cannot point to the real output, the round probably did not count.

## The first validator you should write

Your first validator should fail on fake progress.

Good early checks:

- output files exist and are not empty;
- required fields are closed explicitly;
- the next step is exact rather than vague;
- the workflow touched real assets rather than only notes.

## When to add more structure

Add `JUDGE_AUDIT.md` when:

- a workflow looks active but quality is drifting;
- you want short truth-oriented review notes;
- multiple people need to trust the workflow state quickly.

Add `METHOD_LEARNING.md` when:

- the workflow includes repeated experimentation;
- the same mistakes keep recurring;
- method choices matter and need to be recorded.

## When to add automation

Do not start with lots of automation.

Start with one primary execution thread and a compact control surface.

Add fallback automation only when:

- the main workflow can go stale;
- recovery has to happen unattended;
- a repetitive path is mature enough to be safe.

## A practical first use case

If you want a simple starting point:

1. choose one existing workflow with repeated interruptions;
2. copy the templates into that project;
3. make the next-step note exact;
4. make the validator fail on empty or fake outputs;
5. run that loop for a week before adding more orchestration.

That alone is often enough to expose the biggest quality problems.
