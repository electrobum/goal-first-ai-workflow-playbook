# One Primary Execution Thread

One active primary thread should be the main worker.

That worker should own the real path:

- read the compact truth surface;
- choose one bounded task;
- open sources;
- write evidence;
- run validation;
- leave an exact handoff.

Fallback automation exists for recovery, not as the ordinary engine.

This principle removes a large class of token waste by preventing many support lanes from behaving like pseudo-workers.
