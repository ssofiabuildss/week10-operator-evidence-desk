# IMPLEMENTATION PROMPT — WEEK 10 OPERATOR (derived from pre-code Packet)

Act as a coding agent. Use `docs/PACKET.md` as immutable source of truth for product scope, and the approved Week 10 Team 1 Blueprint's five conditions as invariants. Make small testable increments; do not add commerce/recommendation features.

## Increment I — shell + deterministic engine
- Files: `index.html`, `src/main.js`, `src/style.css`, `src/engine.js`, `tests/engine.test.js`.
- Acceptance: fiction disclosure visible; explicit student constraints (RAM/OS/fictional price); three outcomes; unknown never gets compatible; no inferred budget or purchase recommendation.
- Commit `feat: implement deterministic evidence checker`.

## Increment II — evidence corrections and audit
- Use bounded source labels, mandatory reasons, version changes, local persistence of fiction-only data, readout of revisions.
- Acceptance: correcting synthetic RAM recomputes result, reason and previous/new version present; invalid inputs rejected; reset/export available.
- Commit `feat: add evidence corrections and audit log`.

## Increment III — measured manual comparison
- User records two observations for same case: method, time, errors and support burden. Do not auto-fill invented measurements. Comparison is descriptive, not effectiveness proof.
- Acceptance: totals separated by method; bad numeric values rejected; exported log complete.
- Commit `feat: add manual checklist time ledger`.

## Increment IV — bounded LLM explanation + external price dataset dimension
- Fixed fictional price field already stored in each demo row, evaluated only against user-supplied ceiling. `/api/explain` accepts only precomputed status, bounded reasons, source, scope; calls provider using Vercel environment variable; returns `kind:ai` or explicit fallback.
- Acceptance: API key never sent to browser or committed; LLM response marked AI-generated; unavailable API returns truthful non-AI fallback; LLM never sets compatible/incompatible.
- Commit `feat: add bounded optional explanation`.
- **Deploy 1** after local mechanical smoke tests.

## Increment V — mechanical bug, fix, redeploy
- Run full suite, manually explore UI, and document an actually observed defect (do not manufacture one). Fix it, add regression test, repeat verification.
- Acceptance: `npm test` green, actual issue evidence and resolution in `docs/DECISIONS.md`.
- Commit `fix: correct observed mechanical defect`.

## Increment VI — persona worst-confusion fix
- NEW chat with synthetic persona based on Week 10 USER brief; show actual screenshots sequentially; record all hesitations and one worst confusion; do ONE minimal correction; update decisions.
- Acceptance: before/after copy or UX change and rationale documented; no fictional claims about user study.
- Commit `fix: clarify worst persona confusion`.
- **Deploy 2** after final test.

## Schemas
`EvidenceRow {id:string,name:string,ram:number|null,os:string[]|null,price:number|null,source:string,reviewed:YYYY-MM-DD,note:string,version:number}`. All synthetic.
`Constraints {ram:integer[1,128],os:'Windows'|'macOS'|'Linux',price:number[1,1000000]}`.
`Assessment {id,status:'COMPATIBLE'|'INCOMPATIBLE'|'UNRESOLVED',mismatches:string[],unknown:string[],source:string,scope:string}`.
`Correction {model,reason[8,240],previousVersion,newVersion,at}`.
`WorkLog {label[1,70],method:'manual'|'checker',minutes:[0,240],errors:integer[0,100],support:[0,240],at}`.

## State transitions
- Any explicitly failed constraint -> INCOMPATIBLE (but show missing evidence too).
- No failed constraints + any missing required source field -> UNRESOLVED.
- No failures and no missing fields -> COMPATIBLE **only within declared fictional constraints**.
- Change to evidence -> validate -> log version -> persist -> recompute; no automatic AI edits.
- User's constraints only change from inputs; sponsor cannot influence output.

## Security/fallback
- No personal data; synthetic records only. Validate form and API input size and types; escape dynamic HTML. No secrets in repo. No auth/database needed for synthetic local-only dataset. If real user data later introduced: auth and RLS first.
- AI errors -> deterministic explanatory fallback, never invent verification.
- Unavailable sources -> unresolved; don't lie.
- Mobile: form stacks into one column, buttons remain accessible.

## Acceptance test mapping
T01–T12 listed in Packet §11. At least 5 actual commits and 2 actual deploys required in Git/GitHub/Vercel. A successful unit test is not a substitute for live mechanical bug evidence, persona test, or deployed URLs.
