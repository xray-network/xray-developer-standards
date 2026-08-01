# Aggregate implementation status

Status-Template-Version: v1

`.xray/updates/XRAY-UPDATES-STATUS.md` uses this schema and is the only lifecycle and decision-proof
ledger for all targets. Repeat the target section once for every implementation target.

```markdown
# XRAY Updates status

Status-Version: v1

This is the only lifecycle and decision-proof ledger for all implementation records.

## <Target> implementation status

Target: <target>

### Implementation ledger

| ID | Instruction | State | Result | Evidence mode | Decision proof |
| --- | --- | --- | --- | --- | --- |
| `0001` | [Instruction](./implementations/<target>/0001-IMPL-INSTR.md) | `PLANNED` | — | `LOCAL` | Awaiting implementation. |
```

Every inferred target has exactly one section. Its table header is required even when there are no
rows. Put `No implementation records.` after an empty table header. If there are no inferred
targets, put `No implementation targets.` after the introductory paragraph.

Rules:

- Target sections are unique and ordered by target slug.
- IDs are four digits, unique per target, and ordered ascending within their target section.
- Each row links one matching instruction and, once required, its result.
- Evidence mode matches the instruction.
- States are `PLANNED`, `REVIEW`, `ACCEPTED`, `REJECTED`, or `CANCELLED`.
- `REVIEW`, `ACCEPTED`, and `REJECTED` require a result link.
- `PLANNED` and `CANCELLED` may use `—` for Result.
- Decision proof gives the exact reason for the current state.
- Provider inventories and global plans do not belong here.
