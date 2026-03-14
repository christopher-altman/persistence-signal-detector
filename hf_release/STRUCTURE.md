# Release Structure

This release is a bounded Phase I reproducibility layer aligned to the current paper-facing submission state associated with `arXiv:2603.11382`.

## Folders

- `configs/`
  - Frozen and paper-aligned YAML configurations used by the retained experiments.
  - Includes the locked Phase I config and paper-aligned sweep/baseline configs.

- `thresholds/`
  - Extracted frozen Phase I threshold values derived from `configs/phase1_locked.yaml`.
  - Included to make the gate thresholds easy to inspect without implying a separate raw-data layer.

- `results/`
  - The normalized retained artifact surface copied from the live repo.
  - Includes:
    - retained JSON result artifacts
    - `manifest.json` as the experiment index
    - `ARTIFACT_MANIFEST.md`, `ARTIFACT_AUTHORITY_MAP.json`, and `ARTIFACT_NOTES.md` as the authority layer
    - retained manuscript-aligned tables under `results/tables/`
  - The authority layer distinguishes frozen headline artifacts from inferential support, distribution support, diagnostics, matched baselines, and exploratory comparison families.

- `figures/`
  - Canonical retained paper figure exports.
  - These are included as paper-aligned outputs. Their inclusion does not imply that every figure is exactly regenerable from the public JSON layer alone.

- `manifests/`
  - Additional release-facing provenance files, including source-revision metadata and the figure-export summary used to explain figure-retention semantics.

- `notebooks/`
  - Reproducibility entrypoints referenced by the live experiment index.
  - These notebooks and scripts depend on the canonical UCIP codebase and are not a standalone execution environment by themselves.

## Intentional exclusions

- No standalone raw trajectories are included.
- No standalone label files are included.
- No standalone train/validation/test split files are included.
- No historical snapshots under `.repo_cleanup_backup/` are included.
- No paper build auxiliaries or staging preview PNGs are included.
- No full repo export is included.

## Relation to the paper-facing state

This bundle tracks the current corrected paper-facing state associated with `arXiv:2603.11382` without assuming that a new public arXiv version is already live.

The paper-facing repo now explicitly points readers to the artifact authority manifest. This bundle preserves that same front-door interpretation layer so future readers can distinguish frozen Phase I headline quantities from support, diagnostic, comparison, and exploratory retained artifacts.
