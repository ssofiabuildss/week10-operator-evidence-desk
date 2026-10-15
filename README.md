# Evidence Desk — Week 10 OPERATOR

Fictional Week 10 educational web app. Source-backed **synthetic** laptop compatibility; operator evidence correction & audit; manual checklist comparison; optional bounded LLM explanation. This is **not** a production consumer decision tool.

## Run locally
```bash
npm install
npm test
npm run dev
```
Visit the local URL printed by Vite. For a hosted URL, push this project to GitHub and import into Vercel. Set `OPENAI_API_KEY` in **Vercel environment variables** (not in the repo) to enable the optional AI explainer. Without a key, the deterministic app works and clearly labels a non-AI fallback. Do not claim Dragon Stack execution unless the live AI endpoint has actually been exercised.

## Key demonstration
1. Default RAM=16, OS=Windows, price=18,000. Click evidence check: A COMPATIBLE, B UNRESOLVED, C INCOMPATIBLE, D UNRESOLVED.
2. Evidence updates: select B, enter corrected RAM=16, price=16900, OS=Windows and Linux; enter synthetic source and reason. B changes to COMPATIBLE; audit history grows.
3. Record an actual timed manual checklist exercise and a checker exercise of the same scenario. Do not fabricate measurements.
4. Export local JSON; verify evidence and log available offline. Reset demo only after saving export.
5. Run AI explanation if the Vercel secret exists; otherwise safe fallback. The LLM never computes the verdict.

## Required evidence not automatic
- At least five actual Git commits and two actual Vercel deployments.
- A documented observed mechanical bug and retest after fixing. Tests passing alone are insufficient.
- A real fresh-chat synthetic persona run using actual UI screenshots; identify and fix its worst confusion.
- Full Buildchat transcript PDF, Persona transcript/log PDF, final Packet PDF, real demo video.

## Operator test ledger
Write observed durations and errors only. Compare identical requirement/scenario/evidence across checklist and checker; include maintenance and correction costs. If no meaningful net improvement exists, prefer the simpler checklist.

## Blueprint constraints
1 Traceable evidence and correctability; 2 Shadow buyer autonomy; 3 uncertainty; 4 measurable net operating value; 5 independence/privacy/funding. No shopping store, seller recommender, autofunding, or automatic purchases.
