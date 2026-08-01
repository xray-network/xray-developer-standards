# Target implementation status

Status-Template-Version: v1

Every `xray-updates/implementations/<target>/STATUS.md` uses this schema and is the only lifecycle and
decision-proof ledger for that target.

```markdown
# <Target> implementation status

Status-Version: v1
Target: <target>

This is the only lifecycle and decision-proof ledger for <target> implementation records.

## Implementation ledger

| ID | Instruction | State | Result | Evidence mode | Decision proof |
| --- | --- | --- | --- | --- | --- |
| `0001` | [Instruction](./0001-IMPL-INSTR.md) | `PLANNED` | — | `LOCAL` | Awaiting implementation. |
```

The section and table header are required even when there are no rows. Put
`No implementation records.` after an empty table header.

Rules:

- IDs are four digits, unique per target, and ordered ascending.
- Each row links one matching instruction and, once required, its result.
- Evidence mode matches the instruction.
- States are `PLANNED`, `REVIEW`, `ACCEPTED`, `REJECTED`, or `CANCELLED`.
- `REVIEW`, `ACCEPTED`, and `REJECTED` require a result link.
- `PLANNED` and `CANCELLED` may use `—` for Result.
- Decision proof gives the exact reason for the current state.
- Provider inventories, global plans, and other targets' availability do not belong here.
