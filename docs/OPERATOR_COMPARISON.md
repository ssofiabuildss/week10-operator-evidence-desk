# Week 10 — Team 1 — OPERATOR comparison

## Test and direct observations (2026-10-15)
Evidence Desk is a fictional classroom demo. For Campus C, buyer-declared minimum RAM was 16 GB, required OS Windows, and fictional price ceiling MX$18,000. The fictional Campus C evidence showed 8 GB RAM, Windows, and MX$13,900.

| Method | Operator-reported actual duration | Outcome |
| --- | --- | --- |
| Manual checklist | 15 seconds (0.25 min) | INCOMPATIBLE |
| Evidence Desk deterministic checker | 24 seconds (0.40 min) | INCOMPATIBLE |

The checker took 9 seconds (0.15 minutes) longer, or 60% more time relative to the manual checklist, for **this one case**. Both methods correctly identified the 8 GB versus 16 GB RAM mismatch. These are operator-reported timings, not repeated or independently controlled trials. No time savings, 10:1 benefit, generalized accuracy gain, or financial value has been demonstrated.

## Recording discrepancy: original export remains unchanged
The operator saved the original JSON export on the Mac Desktop, filename `week10-operator-fictional-evidence (1).json`, also supplied in the Build Chat. The export contains **two recorded checker entries**, each 0.40 minutes, with IDs `s-1792106918667-404` and `s-1792106947033-962`. It contains **no manual entry**. Both recorded checker entries are an accidental logging duplication/misclassification, not two separately observed checker runs. **Exclude these entries from method-level aggregates.** The application's visible figure `2 run(s) · 0.8 min` is not a valid comparison. We intentionally did not edit localStorage or reset the demo.

The same export preserves the Campus B synthetic evidence correction from version 1 to version 2, timestamp `2026-10-15T23:08:02.086Z`, reason: “Simulated source update: missing RAM specification corrected during evidence review.” Retain this audit evidence; do not alter or fabricate timestamps.

## OPERATOR finding and limitations
- This simple case favored the manual checklist (15 s vs. 24 s). One case cannot establish a long-run winner.
- Campus B's versioned correction and the export illustrate maintainability features, but time to review, fix, recheck, and support were **not measured**.
- The JSON fields `errors: 0` and `support: 0` belong to the misrecorded entries and do not establish measured zero errors/support cost across the service.
- Actual recurring work, wage rates, hosting/API expense, corrections, support demand, and payer evidence are **unknown**. Do not invent totals or savings.
- Under Blueprint Condition 4, further technology must justify its incremental operational value against an identical-evidence manual checklist. If it does not, prefer the simpler checklist.

## Five locked Team 1 conditions
1. Traceable and correctable evidence, without invented claims or confidence scores.
2. **SHADOW — buyer autonomy** over requirements, budgets and final decision; no automatic purchase or inferred priorities.
3. Visible compatible/incompatible/unresolved outcomes, unknowns, and catalog coverage limitations.
4. Meaningful incremental operational value relative to identical-evidence manual process must be measured.
5. Independent governance: no affiliate incentives, unnecessary personal data retention or unvalidated commercial claims.

No substantive Blueprint decision is changed.
