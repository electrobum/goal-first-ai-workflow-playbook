# Design Rules

## 1. No silent simplification

A richer live plan must not be quietly replaced by a thinner convenient subset.

Every obligation should end in one explicit state:

1. implemented now;
2. remapped into a richer newer surface;
3. explicitly replaced by a better rule;
4. explicitly retired with scope and reason.

Anything else is simplification drift.

## 2. No blank-by-accident fields

Required labels should close as one of:

- a source-backed value;
- `not_reported`;
- `not_applicable`;
- `blocked_missing_source`;
- `blocked_unreadable_source`;
- `blocked_ambiguous_mapping`.

Blank accidental states make recovery weak and ambiguous.

## 3. No header-only progress

Header-only tables do not count as output.

This applies especially to:

- artifact tables;
- curve tables;
- repair ledgers;
- closure ledgers;
- QA ledgers.

## 4. No freshness-only health claims

The system is not healthy merely because:

- timestamps are fresh;
- conversations are alive;
- leases are active;
- batch ids keep changing.

Health must connect to real outputs.

## 5. No method-sensitive execution without a method decision

Before method-sensitive work, record:

- search terms;
- options considered;
- selected method;
- expected outputs;
- validation plan;
- failure states.

## 6. Start gates before substantial work

Before a meaningful execution epoch:

- reread the live plan surface;
- write task-specific reasoning;
- define invalid shortcuts;
- define completion;
- record the method decision when the task is method-sensitive.

## 7. Focused validators over ceremonial validators

The validator should test whether:

- real outputs were produced;
- required links were repaired;
- required fields closed;
- the claimed gap actually shrank.

## 8. Exact handoff every round

Each round should leave one exact continuation pointer:

- exact next file;
- exact next row;
- exact next source;
- or exact blocker.

Broad intentions are not enough for reliable recovery.
