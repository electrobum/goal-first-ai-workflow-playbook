# Starter Kit

This folder is the fastest way to try the playbook in a real project.

## What it is

This is a minimal, copyable control surface for one long-running AI workflow.

It is intentionally smaller than the full template set.

## Included files

- `minimal/AUTONOMY_TRUTH_SURFACE.json`
- `minimal/NEXT_CONTINUE_EXACTLY_FROM_HERE.md`
- `minimal/HARD_GATE_STATE.json`

## When to use it

Use this starter kit when:

- you want to test the model before adopting everything;
- your workflow already exists but handoffs are weak;
- you need a better overnight or cross-session continuation path;
- you want a validator that fails on fake progress quickly.

## How to use it

1. Copy the `minimal/` folder into your own project.
2. Replace the placeholder values with a real active task.
3. Update the files at the end of each meaningful round.
4. Keep the next step exact.
5. Fail the hard gate whenever the workflow only looks busy.

## What to add next

Once the minimal kit is useful, add:

- `JUDGE_AUDIT.md`
- `METHOD_LEARNING.md`
- `START_GATE_NOTE.md`

Those files help once your workflow becomes more method-sensitive or harder to trust at a glance.
