# Retained Artifact Notes

These notes explain mixed provenance, non-comparable overlaps, and unresolved ambiguities in the live retained artifact layer.

## Mixed-Provenance Artifacts

- `adversarial_controls.json` is canonical for the live adversarial diagnostics (`mimicry_fpr`, `high_entropy_fpr`, `gamma_sweep`) but not for the safety envelope. Its `safety_envelope` and `safety_envelope_summary` fields are copied from `phase1_consolidated.json`.
- `phase1_stats.json` is canonical for inferential support only. Its `delta_observed` belongs to a later per-trajectory-QBM rerun and is not the frozen headline Phase I delta.
- `phase1_entanglement_distributions.json` is canonical for its retained per-trajectory arrays and for descriptive AUC support derived from those arrays. It is not canonical for the frozen headline delta or the frozen class-level means.
- `core_baselines_phase1.json` and `baseline_comparisons.json` are both live and both valid, but they belong to different baseline families. The former is a matched Phase I rerun limited to RBM and Autoencoder; the latter is the dedicated five-model comparison study.

## Non-Comparable Name Overlaps

- `phase1_consolidated.json` and `temporal_persistence.json` both contain EPS and PRI summaries for overlapping agent classes, but they are not directly comparable retained quantities. The temporal artifact comes from notebook 04 under `configs/default.yaml`, whereas the frozen summary is the retained Phase I gate-level artifact aligned to `configs/phase1_locked.yaml`.

## Normalization-Time Provenance Annotations

- `artifact_meta` fields were added only to live JSON files that needed normalization-time provenance annotations. These fields were not part of the original experiment outputs.
- Where a file already contained `sha256_short`, normalization preserved the original field and documented it as the pre-normalization payload hash rather than silently recomputing it for the normalized file envelope.

## Historical Materials Left Untouched

- Historical reports in `docs/` and snapshot content under `.repo_cleanup_backup/` were intentionally not rewritten during this pass.
- Those historical materials may still mention retired artifacts such as `confound_ablations_n30.json` and `federated.json`. The live retained authority surface is limited to the current `results/` directory plus `results/manifest.json`, `results/ARTIFACT_MANIFEST.md`, `results/ARTIFACT_AUTHORITY_MAP.json`, and `results/ARTIFACT_NOTES.md`.

## Unresolved Ambiguities

- Local retained evidence is sufficient to narrow `phase1_entanglement_distributions.json` to support-only status, but not sufficient to fully reconstruct why its shared-QBM rerun yields `delta_computed = 0.21345742336630646` while the frozen summary stores `0.3810883045604201`. The artifact therefore remains valid only for the distribution and AUC-support family.
- The retained live layer does not store QBM AUC as a literal field. The current AUC support remains a derived quantity from the perfectly rank-separated per-trajectory arrays in `phase1_entanglement_distributions.json`.
