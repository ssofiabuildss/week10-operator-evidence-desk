# Week 10 — Team 1 — Evidence and verification register

## Confirmed repository history as checked on 2026-10-15
- Repository: https://github.com/ssofiabuildss/week10-operator-evidence-desk
- Original commit `b8bfd9da7d16e06310cd6efe51e64af3463f5bbb` — `chore: initialize Week 10 Operator Evidence Desk`.
- Mechanical defect fix commit `aecac569e60401942d140afbcee8046a6d4224fb` — `fix: clear stale correction success message`.
- Bug: previous successful evidence-correction message remained after an invalid correction submission. Fix clears stale message on correction form input/change/invalid events. Browser reproduction/retest reported in the project DECISIONS log and prior Build Chat; do not construe as a fresh browser retest in this handoff.

## Reverified mechanical tests
- Supplied ZIP's `tests/engine.test.js` executed locally with `node --test tests/engine.test.js` on 2026-10-15.
- **10 tests passed; 0 failed**. Covered RAM/OS/price mismatches, missing evidence, compatible result, correction version, invalid inputs, export structure, precedence rules.
- This fresh run was on the uploaded project ZIP, which predates the fix; the earlier documented regression run after the fix reported 10/10 passing. The browser stale-message correction is not one of the 10 tests, so never characterize this automated run as a direct automated regression test of that UI bug.
- Browser display screenshots showed Campus B v2 COMPATIBLE, Campus C INCOMPATIBLE, Campus D UNRESOLVED and Campus A COMPATIBLE under declared constraints.

## Vercel deployments independently verified (READY / production)
1. `dpl_3QE6GQZMXMMjNbFojozYtLJguqKa` — https://week10-operator-evidence-desk-nmolh9n4k-ssofia1.vercel.app — commit `b8bfd9d` — READY.
2. `dpl_37bAkTsa8F41vuvq5J7cvTE3qo65` — https://week10-operator-evidence-desk-jx791r5i1-ssofia1.vercel.app — commit `aecac56` — READY.
- Current production alias https://week10-operator-evidence-desk.vercel.app maps to deployment 2 as verified via Vercel project metadata.
- Further Git documentation commits do not, by themselves, prove another Vercel deployment.

## Unverified or incomplete checks
- No actual monetary support/maintenance cost data; manual-versus-checker comparison limited to one case and flawed stored ledger; see `docs/OPERATOR_COMPARISON.md`.
- Mobile UI, exported JSON reimport, and live AI explanation/fallback were not independently exercised in this handoff. Automated export structure check passed; do not overstate coverage.
- Independent Persona Test must occur in **a separate chat** and follow actual screenshots. No persona responses or persona-fix commit yet.
- Build Chat transcript, Persona transcript and final demo-video evidence depend on their actual production; do not mark complete until produced.

## Operator decision
Do not claim product validation or a 10:1 result. Preserve the evidence trail and the Team 1 Blueprint's five conditions.
