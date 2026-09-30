# REMORA evidence-sufficiency v1.2 — private repair check

2026-09-30. For maintainer factual correction; publication requires a separate agreement.

## Result

The three canonicalisation faults that survived v1.1 are now distinguished in the status/reason and runner-failures projections. They remain indistinguishable in the guidance projection, where the relevant outcomes are decisive and carry no guidance. This checks repair against known faults, not generalisation.

| Projection | Known killed / survived | Previously additional killed / survived |
|---|---:|---:|
| Status and reason | 80 / 0 | 6 / 0 |
| Guidance | 90 / 13 | 3 / 3 |
| Runner failures | 103 / 0 | 6 / 0 |

All six measurements completed. Positive controls were killed; inert controls changed nothing. No unproved mutant occurred. The two guidance rows exited 1 with only survivor declarations. Two known faults per row were unexpected-exit kills (the missing expected_state and observed_state guard halves), the same labels as in v1.1. No previously additional fault was killed by termination. These are not three different sets of bugs: the rows project the same selected faults differently and must not be added together.

Exactly three mutation labels change from survived to killed, each in the verdict and runner rows: case-folded strings, list-order erasure and mapping values ignored. Each moves one vector in the per-case verdict row. All other mutation verdicts match the retained original v1.1 reports. The original 13 known-set guidance survivors remain; their previously agreed projection limitation still applies. No denominator was reduced. The aliases retain the published overlap disclosures and are not fresh independent evidence.

## Fixed inputs and comparison

- REMORA source: `c1345b1f9e0f877454bf996b2160d533c5a9b16a`.
- CA 0.7.0: `5fa2ff587497b00ac684a767335b9068f7e520a6`.
- Tool content identity: `sha256:5258816bb0b8933466a34b42651467cde11845fbf36f5e7f18a9176839a5cd5e`; exact in every report.
- Python 3.14.3; platform recorded in RUN-PLAN-FROZEN.json.
- Original frozen plan SHA-256: `0a44f9e385a57cd18dc103d66a2afd545ffd58cb74b7e18ac106bb74da631990`.

The six manifests are byte-identical to the [published v1.1 package](https://github.com/corpus-adequacy/remora-es-v11-adequacy/tree/9f3851995bbe395e510dde9ce9a03ebb6f1f965a). Only adapter suite paths/identity and the appended E18–E20 vectors differ. The 50 old cases retain JSON values and order. The v1/v1.1 conformance trees equal those at `8772d85a3b2544045960910f3704d88f741e1545`; guidance and ladders are copied byte for byte. Rows ran sequentially, and the subject hash inventory was checked before execution and after every row.

The formerly additional set was selected with the v1.1 design and totals visible; it was never a blind sample. All its definitions were public before v1.2. E18–E20 were authored with the faults known. The measured change is therefore repair evidence only. It establishes neither checker correctness nor corpus completeness, security, production effectiveness or a generalisation rate. A surviving guidance row does not contradict the repaired verdict and runner projections.

## Evidence and review

The result files are derived delivery copies. Only the top-level local `manifest` path is replaced by a portable relative path; every other parsed value is unchanged. ORIGINAL-TO-DELIVERY.json binds original and delivery digests. Original bytes remain retained; this package alone cannot independently establish those original digests. Execution receipts are unchanged. The published v1.0 and v1.1 packages remain unchanged.

Preparation and retained-result interpretation were reviewed by a separate, non-building Codex subagent. It checked controls, counts, termination labels, tool/source hashes and the before/after verdict changes. This is a same-family review, not an independent rerun or cross-family validation. Delivery packaging is checked separately in DELIVERY-VERIFICATION.json.

Please flag factual corrections and whether the projection-specific interpretation matches your contract. Once that is settled, please say separately whether this package may be published unchanged, including these limitations. Until then it stays private.

Prepared with AI assistance; original result bytes retained.
