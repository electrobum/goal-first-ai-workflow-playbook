# FAQ

## Is this a framework or a methodology?

It is closer to a methodology and a set of control templates than to a software framework.

The point is to improve how an AI workflow is run, resumed, and validated, not to force one implementation stack.

## Why "one primary execution thread"?

Because long-running workflows often waste budget by turning support lanes into pseudo-workers.

One clearly owned main path is usually easier to trust and easier to recover.

## Does this mean multi-agent systems are bad?

No.

It means multi-agent systems should justify their complexity.

Extra lanes are worth keeping only when they solve a real coordination or recovery problem.

## What is a truth surface?

A truth surface is the smallest set of files that lets a fresh worker understand the real state quickly.

It should summarize the workflow honestly without replacing the real outputs.

## What is a hard gate?

A hard gate is a validator that can fail on fake progress.

It should check whether the workflow produced meaningful outputs, not merely whether activity occurred.

## Why not just use memory or chat history?

Because long-running workflows eventually outgrow conversational memory.

File-backed continuation is slower to fake and easier to inspect.

## Is this only for coding workflows?

No.

The examples include coding and documentation patterns, but the playbook applies to many forms of AI-assisted knowledge work and automation.

## What should I implement first?

Start with:

- a truth surface;
- an exact next-step note;
- a validator that fails on empty or fake outputs.

Those three pieces alone already improve many workflows.
