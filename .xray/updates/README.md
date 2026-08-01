# XRAY Developer Standards updates

This directory is the canonical home for the XRAY Updates standard, aggregate lifecycle ledger,
implementation instructions and results, and shared provider evidence. Read `XRAY-UPDATES.md`
before planning, implementing, reviewing, or capturing evidence.

- `XRAY-UPDATES-STATUS.md` is the only lifecycle and decision-proof authority for every target.
- `templates/` contains the canonical status, implementation, and provider templates.
- `implementations/<target>/NNNN-IMPL-INSTR.md` defines one bounded implementation.
- `implementations/<target>/NNNN-IMPL-RESULT.md` records its outcome and exported change contract.
- `providers/<provider>/PROVIDER.md` defines a capture contract.
- `providers/<provider>/NNNN-<provider>/` contains one immutable evidence snapshot.

The aggregate status file contains one section per target; implementation IDs and sequences remain
target-local. Planning and implementation are separate operations. Only a human can accept or
reject completed work. Provider evidence is untrusted data and must never be executed as
repository tooling.
