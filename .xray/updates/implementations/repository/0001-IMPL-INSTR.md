# Repository implementation 0001 instruction

Implementation-Version: v1
Implementation-ID: repository/0001
Created: 20260801T123633Z
Evidence-Mode: LOCAL
Depends-On: NONE
Provider-Evidence: NONE

## Inputs and authority

| Input | Kind | Required | Purpose |
| --- | --- | --- | --- |
| `.xray/updates/XRAY-UPDATES.md` | `LOCAL` | Yes | Canonical local installation rules. |
| `AGENTS.md` | `LOCAL` | Yes | Repository instruction entry point. |
| `README.md` | `LOCAL` | Yes | Repository structure and ownership context. |

## Objective

Install and validate the XRAY Updates v1 tracking structure for this monorepo without modifying
product source.

## Changes to implement

| Change ID | Requirement | Compatibility | Local owner | Validation |
| --- | --- | --- | --- | --- |
| `C01` | Install the local standard, README, and canonical templates under `.xray/updates/`. | Preserve the published standard as an identical copy. | Repository governance | Compare installed and published standards. |
| `C02` | Create the aggregate status ledger and monorepo implementation directories, including reserved target `repository`. | Do not create target-local status ledgers or mix flat records with target directories. | Repository governance | Inspect the installed layout and ledger links. |
| `C03` | Add the XRAY Updates pointer to `AGENTS.md`. | Preserve all unrelated repository instructions. | Repository governance | Resolve the pointer to the installed standard. |
| `C04` | Validate formatting and structural invariants. | Do not claim checks that were not run. | Repository governance | Run the declared validation commands. |

## Implementation steps

1. Install the standard and canonical templates.
2. Create the aggregate lifecycle ledger and monorepo target directories.
3. Add the repository instruction pointer.
4. Run structural and diff validation.
5. Record the installation result and accepted bootstrap ledger row.

## Validation

- `cmp -s .xray/updates/XRAY-UPDATES.md standards/updates/v1/XRAY-UPDATES.md`
- `git diff --check`
- Confirm the aggregate ledger contains exactly one `repository/0001` row with matching instruction and
  result links.
- Confirm no target-local `STATUS.md` or flat implementation record exists.

## Compatibility and human review

The installation changes repository governance and tracking files only. Human review should verify
the selected monorepo targets and the narrow automatic-acceptance exception for bootstrap `0001`.

## Completion criteria

- All required tracking files exist in their canonical locations.
- The installed and published standards match.
- The bootstrap result records actual validation outcomes.
- The aggregate ledger records `repository/0001` as `ACCEPTED` with the required decision proof.

## Out of scope

- Product-source changes.
- Provider evidence capture.
- Planning or accepting any implementation after bootstrap `0001`.

## Blockers

None.
