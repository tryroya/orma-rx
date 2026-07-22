# Orma Rx — test build (demo)

Mobile-first demo of a $50 CPAP-prescription service: patient with an existing sleep study →
intake + front-camera tongue photo → physician-facing AI pre-review (green/red, every check shows its
basis) → physician signs a specimen Rx. Built for CMO feedback. Deployed via GitHub Pages.

- **Demo only:** no backend — entries stay in the visitor's browser (localStorage); fake checkout; specimen watermark. Restart demo from the footer.
- **Claims posture (F41-reviewed 2026-07-22):** physician-service framing only — no diagnosis/screening/monitoring claims, no device references. Do not add any.
- **F9 conditions:** the pre-review is physician-facing CDS; the tongue photo is displayed to the physician and must never be machine-analyzed.
- Source of record: `sites/orma-rx/` in the orma-wiki repo — edit there, re-upload via the contents API.
- Criteria ruleset v0.1 (draft for CMO correction): `brain/clinical/orma-rx-criteria.md`.
