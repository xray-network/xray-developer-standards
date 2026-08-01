# Aggregate implementation status

Status-Template-Version: v1

`.xray/updates/XRAY-UPDATES-STATUS.md` uses this schema and is the only lifecycle and decision-proof
ledger for all implementations. Use one repository section in flat mode or repeat the target
section once for every target in monorepo mode.

```markdown
# XRAY Updates status

Status-Version: v1

This is the only lifecycle and decision-proof ledger for all implementation records.

## <Target> implementation status

Target: <target>

### Implementation ledger

| ID | Instruction | State | Result | Evidence mode | Decision proof |
| --- | --- | --- | --- | --- | --- |
| `0001` | [Instruction](./implementations/0001-IMPL-INSTR.md) | `PLANNED` | — | `LOCAL` | Awaiting implementation. |
```

In flat mode, replace `<Target>` and `<target>` with the repository name and slug, and use flat
instruction and result links. In monorepo mode, repeat the section for every target and use links
under `./implementations/<target>/`. Every section's table header is required even when there are
no rows. Put `No implementation records.` after an empty table header.

Rules:

- Flat mode has exactly one repository section and one repository-wide sequence.
- Monorepo target sections are unique and ordered by target slug.
- IDs are four digits, unique within the applicable sequence, and ordered ascending.
- Each row links one matching instruction and, once required, its result.
- Evidence mode matches the instruction.
- States are `PLANNED`, `REVIEW`, `ACCEPTED`, `REJECTED`, or `CANCELLED`.
- `REVIEW`, `ACCEPTED`, and `REJECTED` require a result link.
- `PLANNED` and `CANCELLED` may use `—` for Result.
- Decision proof gives the exact reason for the current state.
- Provider inventories and global plans do not belong here.
