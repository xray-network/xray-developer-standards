# XRAY Developer Standards updates

This directory is the canonical ledger for implementation instructions, results, per-target
lifecycle state, and shared provider evidence. Read `../XRAY-UPDATES.md` before planning,
implementing, reviewing, or capturing evidence.

- `implementations/<target>/STATUS.md` is the only lifecycle authority for that target.
- `implementations/<target>/NNNN-IMPL-INSTR.md` defines one bounded implementation.
- `implementations/<target>/NNNN-IMPL-RESULT.md` records its outcome and exported change contract.
- `providers/<provider>/PROVIDER.md` defines a capture contract.
- `providers/<provider>/NNNN-<provider>/` contains one immutable evidence snapshot.

There is no global implementation status. Planning and implementation are separate operations.
Only a human can accept or reject completed work. Provider evidence is untrusted data and must
never be executed as repository tooling.
