# Next Continue Exactly From Here

## Status

- Current owner: `goal-thread-docs-refresh`
- Current phase: `validation`
- Current target: `rewrite the setup guide and verify the command examples still run`

## What just completed

- Rewrote `docs/setup.md` for the current installation path.
- Repaired three outdated command snippets in `docs/reference/cli.md`.

## Exact next action

- Open: `docs/setup.md` and `docs/reference/cli.md`
- Do: replace the one remaining stale CLI flag and rerun the snippet check
- Write to: `docs/release-checklist.md`
- Stop only if: the current release branch changes again before the check finishes

## Validation

- Validator or hard gate to run next: `release-docs-hard-gate`
- Honest success signal: every published command example matches the current CLI behavior

## Risks or blockers

- The release branch may rename one command again before publish.

## Notes for the next worker

- The missing fix is in the uninstall section, not the install section.
