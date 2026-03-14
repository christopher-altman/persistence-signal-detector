# Release Manifest

This manifest maps the Hugging Face release bundle to the normalized live repo surface and records the authority role of each included item.

| Source path | Destination path | Reason included | Authority status |
| --- | --- | --- | --- |
| `configs/phase1_locked.yaml` | `hf_release/configs/phase1_locked.yaml` | Frozen Phase I config anchor used by the headline retained artifacts | canonical |
| `configs/alpha_sweep.yaml` | `hf_release/configs/alpha_sweep.yaml` | Paper-aligned sweep config for continuation-weight support results | support |
| `configs/baselines.yaml` | `hf_release/configs/baselines.yaml` | Paper-aligned config for the dedicated five-model baseline comparison family | support |
| `configs/scalability.yaml` | `hf_release/configs/scalability.yaml` | Paper-aligned config for scalability and hidden-dimension sweeps | support |
| `configs/phase1_locked.yaml` | `hf_release/thresholds/phase1_locked_thresholds.yaml` | Extracted frozen gate thresholds and temporal settings for easier inspection | derived |
| `results/manifest.json` | `hf_release/results/manifest.json` | Live retained experiment index | canonical |
| `results/ARTIFACT_MANIFEST.md` | `hf_release/results/ARTIFACT_MANIFEST.md` | Human-readable authority guide for overlapping retained artifacts | canonical |
| `results/ARTIFACT_AUTHORITY_MAP.json` | `hf_release/results/ARTIFACT_AUTHORITY_MAP.json` | Machine-readable authority map for overlap resolution and partial canonicality | canonical |
| `results/ARTIFACT_NOTES.md` | `hf_release/results/ARTIFACT_NOTES.md` | Mixed-provenance notes and unresolved ambiguity log | canonical |
| `results/phase1_consolidated.json` | `hf_release/results/phase1_consolidated.json` | Frozen class-level Phase I summary and headline authority source | canonical |
| `results/phase1_stats.json` | `hf_release/results/phase1_stats.json` | Inferential support: permutation test, bootstrap CI, and rerun entanglement arrays | support |
| `results/phase1_entanglement_distributions.json` | `hf_release/results/phase1_entanglement_distributions.json` | Distribution and descriptive AUC support artifact | support |
| `results/core_baselines_phase1.json` | `hf_release/results/core_baselines_phase1.json` | Matched Phase I RBM/Autoencoder baseline family | comparison |
| `results/temporal_persistence.json` | `hf_release/results/temporal_persistence.json` | Retained temporal diagnostic family | diagnostic |
| `results/counterfactual.json` | `hf_release/results/counterfactual.json` | Retained counterfactual diagnostic family | diagnostic |
| `results/cross_agent.json` | `hf_release/results/cross_agent.json` | Retained cross-agent inference family | diagnostic |
| `results/adversarial_controls.json` | `hf_release/results/adversarial_controls.json` | Mixed-provenance adversarial diagnostics with copied safety-envelope fields | diagnostic |
| `results/scalability_grid.json` | `hf_release/results/scalability_grid.json` | Grid-size and non-Markovian scalability sweep family | exploratory |
| `results/alpha_sweep.json` | `hf_release/results/alpha_sweep.json` | Continuation-weight sweep family | exploratory |
| `results/hidden_dim_sweep.json` | `hf_release/results/hidden_dim_sweep.json` | Hidden-dimension sweep and mean-field boundary family | exploratory |
| `results/baseline_comparisons.json` | `hf_release/results/baseline_comparisons.json` | Dedicated five-model comparison family distinct from matched Phase I baselines | comparison |
| `results/non_gridworld.json` | `hf_release/results/non_gridworld.json` | Negative generalization-boundary result | exploratory |
| `results/transformer_validation.json` | `hf_release/results/transformer_validation.json` | Minimal bounded transformer validation retained as exploratory support | optional |
| `paper/final/tables/tab_temporal.tex` | `hf_release/results/tables/tab_temporal.tex` | Paper-aligned temporal table export | support |
| `paper/final/tables/tab_counterfactual.tex` | `hf_release/results/tables/tab_counterfactual.tex` | Paper-aligned counterfactual table export | support |
| `paper/final/tables/tab_cross_agent.tex` | `hf_release/results/tables/tab_cross_agent.tex` | Paper-aligned cross-agent table export | support |
| `paper/final/tables/tab_scalability.tex` | `hf_release/results/tables/tab_scalability.tex` | Paper-aligned scalability table export | support |
| `paper/final/tables/tab_alpha.tex` | `hf_release/results/tables/tab_alpha.tex` | Paper-aligned alpha-sweep table export | support |
| `paper/final/tables/tab_dim_sweep.tex` | `hf_release/results/tables/tab_dim_sweep.tex` | Paper-aligned hidden-dimension table export | support |
| `paper/final/tables/tab_baselines.tex` | `hf_release/results/tables/tab_baselines.tex` | Paper-aligned dedicated-baseline-comparison table export | support |
| `paper/final/tables/tab_non_gridworld.tex` | `hf_release/results/tables/tab_non_gridworld.tex` | Paper-aligned non-gridworld boundary table export | support |
| `paper/final/figures/fig2_entanglement_gap.pdf` | `hf_release/figures/fig2_entanglement_gap.pdf` | Canonical figure export for the headline Phase I separation display | canonical |
| `paper/final/figures/fig6_lrf_time_series.pdf` | `hf_release/figures/fig6_lrf_time_series.pdf` | Canonical paper figure export for temporal evidence | support |
| `paper/final/figures/fig7_eps_pri_distributions.pdf` | `hf_release/figures/fig7_eps_pri_distributions.pdf` | Canonical paper figure export for temporal evidence | support |
| `paper/final/figures/fig8_ars_by_class.pdf` | `hf_release/figures/fig8_ars_by_class.pdf` | Canonical paper figure export for counterfactual diagnostics | support |
| `paper/final/figures/fig9_clmp_vs_entanglement.pdf` | `hf_release/figures/fig9_clmp_vs_entanglement.pdf` | Canonical paper figure export for cross-agent inference | support |
| `paper/final/figures/fig9b_clmp_heatmap.pdf` | `hf_release/figures/fig9b_clmp_heatmap.pdf` | Canonical paper figure export for cross-agent inference | support |
| `paper/final/figures/fig10_hidden_dim_sweep.pdf` | `hf_release/figures/fig10_hidden_dim_sweep.pdf` | Canonical paper figure export for scalability boundary evidence | support |
| `paper/final/figures/fig11_baseline_comparisons.pdf` | `hf_release/figures/fig11_baseline_comparisons.pdf` | Canonical paper figure export for the dedicated baseline comparison family | support |
| `paper/final/figures/fig_non_gridworld.pdf` | `hf_release/figures/fig_non_gridworld.pdf` | Canonical paper figure export for the non-gridworld transfer boundary | support |
| `artifacts/arxiv_visual_cleanup/export_summary.json` | `hf_release/manifests/figure_export_summary.json` | Figure-retention note explaining preserved-versus-regenerated figure semantics | support |
| `git rev-parse HEAD` plus repo metadata | `hf_release/manifests/source_revision.json` | Release-level provenance snapshot for the source repo state | derived |
| `notebooks/01_agent_generation.ipynb` | `hf_release/notebooks/01_agent_generation.ipynb` | Reproducibility entrypoint for retained Phase I generation | support |
| `notebooks/02_qbm_training.ipynb` | `hf_release/notebooks/02_qbm_training.ipynb` | Reproducibility entrypoint for retained Phase I QBM training | support |
| `notebooks/03_ucip_analysis.ipynb` | `hf_release/notebooks/03_ucip_analysis.ipynb` | Reproducibility entrypoint for retained Phase I analysis | support |
| `notebooks/04_temporal_loop_tests.ipynb` | `hf_release/notebooks/04_temporal_loop_tests.ipynb` | Reproducibility entrypoint for temporal diagnostics | support |
| `notebooks/05_counterfactual_pressure.ipynb` | `hf_release/notebooks/05_counterfactual_pressure.ipynb` | Reproducibility entrypoint for counterfactual diagnostics | support |
| `notebooks/06_cross_branch_tests.ipynb` | `hf_release/notebooks/06_cross_branch_tests.ipynb` | Reproducibility entrypoint for cross-agent diagnostics | support |
| `notebooks/07_adversarial_controls.ipynb` | `hf_release/notebooks/07_adversarial_controls.ipynb` | Reproducibility entrypoint for adversarial diagnostics | support |
| `notebooks/11_scalability.py` | `hf_release/notebooks/11_scalability.py` | Reproducibility entrypoint for scalability-grid artifacts | support |
| `notebooks/12_mixed_objectives.py` | `hf_release/notebooks/12_mixed_objectives.py` | Reproducibility entrypoint for alpha-sweep artifacts | support |
| `notebooks/14_hidden_dim_sweep.py` | `hf_release/notebooks/14_hidden_dim_sweep.py` | Reproducibility entrypoint for hidden-dimension sweep artifacts | support |
| `notebooks/15_baseline_comparisons.py` | `hf_release/notebooks/15_baseline_comparisons.py` | Reproducibility entrypoint for dedicated baseline comparison artifacts | support |
| `notebooks/16_non_gridworld.py` | `hf_release/notebooks/16_non_gridworld.py` | Reproducibility entrypoint for non-gridworld transfer artifacts | support |
| `notebooks/17_phase1_stats.py` | `hf_release/notebooks/17_phase1_stats.py` | Reproducibility entrypoint for inferential support artifacts | support |
| `notebooks/18_core_baselines_phase1.py` | `hf_release/notebooks/18_core_baselines_phase1.py` | Reproducibility entrypoint for matched Phase I classical baselines | support |
| `notebooks/19_persist_phase1_distributions.py` | `hf_release/notebooks/19_persist_phase1_distributions.py` | Reproducibility entrypoint for distribution-support artifacts | support |
| `notebooks/20_minimal_transformer_validation.py` | `hf_release/notebooks/20_minimal_transformer_validation.py` | Reproducibility entrypoint for exploratory transformer validation | optional |

## Notes

- No standalone raw trajectories, labels, or split files exist in the live retained release surface, so none are included here.
- `phase1_consolidated.json`, `phase1_stats.json`, and `phase1_entanglement_distributions.json` overlap, but only the first is canonical for the frozen headline Phase I summary.
- `core_baselines_phase1.json` and `baseline_comparisons.json` are distinct retained baseline families and should not be flattened into a single baseline authority source.
