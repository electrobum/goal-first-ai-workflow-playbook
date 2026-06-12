# Next Continue Exactly From Here

## Status

- Current owner: `goal-thread-regression-fix`
- Current phase: `repair`
- Current target: `fix the cached-session expiry regression`

## What just completed

- Reproduced the bug in `tests/session/cache-regression.test.ts`.
- Confirmed the timestamp comparison in `src/session/cache.ts` uses the wrong boundary.

## Exact next action

- Open: `src/session/cache.ts`
- Do: patch the timestamp comparison, rerun the focused regression test, and then rerun the related session suite
- Write to: `notes/regression-fix-audit.md`
- Stop only if: the focused test still fails after the boundary patch and the root cause assumption is no longer credible

## Validation

- Validator or hard gate to run next: `session-regression-hard-gate`
- Honest success signal: the focused regression test passes and no related session tests regress

## Risks or blockers

- Another session expiry path may also be affected if the boundary logic was duplicated elsewhere.

## Notes for the next worker

- The failure reproduces only when the refresh timestamp equals the cached expiry timestamp exactly.
