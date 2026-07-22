# Orma Rx — test build (demo)

Demo of a $50 CPAP-prescription service: patient uploads their sleep study report FIRST → simulated
auto-read prefills identity/study/body fields ("✓ report" tags; the sample-report path shows the full
magic, own uploads honestly prefill nothing in the test build) → confirm-and-correct screen → the few
questions a report never has → front-camera tongue photo → combined check-&-pay. 5 steps. Then
physician-facing AI pre-review (green/red, every check shows its basis) → physician signs a specimen Rx.
Built for CMO feedback. Deployed via GitHub Pages.

- **Report-first intake (2026-07-22 rebuild):** prior questions-first version kept runnable at
  `previous.html` (same directory, also deployed) per the keep-prior-version rule.

- **Demo only:** no backend — entries stay in the visitor's browser (localStorage); fake checkout; specimen watermark. Restart demo from the footer.
- **Physician dashboard (2026-07-22):** queue + "Completed" worked examples (clean sign-off / decline-with-refund / documented override, cases s4–s6); case detail has back-to-list top + bottom; declines now persist. The "it learns from you" line is physician-facing concept copy about the pre-review learning from physician decisions — it is NOT a diagnosis/screening claim and the airway photo stays physician-viewed only.
- **Responsive (2026-07-22):** real desktop layout at ≥900px (Adrian: company default for ALL Orma sites going forward), mobile-first below.
- **Claims posture (F41-reviewed 2026-07-22):** physician-service framing only — no diagnosis/screening/monitoring claims, no device references. Do not add any.
- **F9 conditions:** the pre-review is physician-facing CDS; the tongue photo is displayed to the physician and must never be machine-analyzed.
- Source of record: `sites/orma-rx/` in the orma-wiki repo — edit there, re-upload via the contents API.
- Criteria ruleset v0.1 (draft for CMO correction): `brain/clinical/orma-rx-criteria.md`.
