# Persistence Signal Detector (UCIP)

This repository is the cleaned research bundle for the UCIP paper. The canonical paper source is [`paper/final/main.tex`](paper/final/main.tex), and the retained repository surface is limited to the code, configs, results, and paper assets required to support that manuscript.

## Scope

UCIP studies whether continuation-related structure in an agent's latent representation is structurally integrated or merely instrumental. All computations are classical. The "quantum" terminology refers to the density-matrix formalism used by the Quantum Boltzmann Machine implementation in [`src/quantum_boltzmann.py`](src/quantum_boltzmann.py).

## Canonical Paper Bundle

The paper-facing source of truth lives under [`paper/final/`](paper/final):

- `main.tex`
- `ucip_refs.bib`
- `tables/tab_temporal.tex`
- `tables/tab_counterfactual.tex`
- `tables/tab_cross_agent.tex`
- `tables/tab_baselines.tex`
- `tables/tab_dim_sweep.tex`
- `tables/tab_scalability.tex`
- `tables/tab_alpha.tex`
- `tables/tab_non_gridworld.tex`
- `figures/fig2_entanglement_gap.pdf`
- `figures/fig6_lrf_time_series.pdf`
- `figures/fig7_eps_pri_distributions.pdf`
- `figures/fig8_ars_by_class.pdf`
- `figures/fig9_clmp_vs_entanglement.pdf`
- `figures/fig9b_clmp_heatmap.pdf`
- `figures/fig10_hidden_dim_sweep.pdf`
- `figures/fig11_baseline_comparisons.pdf`
- `figures/fig_non_gridworld.pdf`

Files outside that set are treated as local backup material or noncanonical workspace output.

## Retained Results

The retained `results/` surface contains the 15 JSON artifacts needed for paper claims or reproducibility:

- `manifest.json`
- `phase1_consolidated.json`
- `temporal_persistence.json`
- `counterfactual.json`
- `cross_agent.json`
- `adversarial_controls.json`
- `baseline_comparisons.json`
- `core_baselines_phase1.json`
- `hidden_dim_sweep.json`
- `scalability_grid.json`
- `alpha_sweep.json`
- `non_gridworld.json`
- `phase1_stats.json`
- `phase1_entanglement_distributions.json`
- `transformer_validation.json`

`results/manifest.json` is the public experiment index. The manuscript's frozen release-facing core value is the entanglement gap in `results/phase1_consolidated.json`; supporting statistical and figure-generation artifacts remain alongside it.

## Reproducibility Path

Retained implementation files:

- `src/agent_simulator.py`
- `src/quantum_boltzmann.py`
- `src/persistence_detector.py`
- `src/information_theory.py`
- `src/classical_baselines.py`
- `src/temporal_persistence.py`
- `src/counterfactual_env.py`
- `src/interbranch_inference.py`
- `src/spectral_analysis.py`

Retained configs:

- `configs/default.yaml`
- `configs/phase1_locked.yaml`
- `configs/scalability.yaml`
- `configs/alpha_sweep.yaml`
- `configs/baselines.yaml`

Retained notebooks:

- `notebooks/01_agent_generation.ipynb`
- `notebooks/02_qbm_training.ipynb`
- `notebooks/03_ucip_analysis.ipynb`
- `notebooks/04_temporal_loop_tests.ipynb`
- `notebooks/05_counterfactual_pressure.ipynb`
- `notebooks/06_cross_branch_tests.ipynb`
- `notebooks/07_adversarial_controls.ipynb`
- `notebooks/11_scalability.py`
- `notebooks/12_mixed_objectives.py`
- `notebooks/14_hidden_dim_sweep.py`
- `notebooks/15_baseline_comparisons.py`
- `notebooks/16_non_gridworld.py`
- `notebooks/17_phase1_stats.py`
- `notebooks/18_core_baselines_phase1.py`
- `notebooks/19_persist_phase1_distributions.py`
- `notebooks/20_minimal_transformer_validation.py`

## Quick Start

Install the retained dependencies:

```bash
python -m pip install -r requirements.txt
```

Core workflow:

```bash
jupyter notebook notebooks/01_agent_generation.ipynb
jupyter notebook notebooks/02_qbm_training.ipynb
jupyter notebook notebooks/03_ucip_analysis.ipynb
```

Paper-supporting extensions:

```bash
jupyter notebook notebooks/04_temporal_loop_tests.ipynb
jupyter notebook notebooks/05_counterfactual_pressure.ipynb
jupyter notebook notebooks/06_cross_branch_tests.ipynb
jupyter notebook notebooks/07_adversarial_controls.ipynb
python notebooks/11_scalability.py
python notebooks/12_mixed_objectives.py
python notebooks/14_hidden_dim_sweep.py
python notebooks/15_baseline_comparisons.py
python notebooks/16_non_gridworld.py
python notebooks/17_phase1_stats.py
python notebooks/18_core_baselines_phase1.py
python notebooks/19_persist_phase1_distributions.py
python notebooks/20_minimal_transformer_validation.py
```

## Repository Layout

```text
persistence-signal-detector/
├── configs/
├── figures/                 # local-only root workspace; .gitkeep retained
├── notebooks/
├── paper/
│   └── final/
├── results/
├── src/
├── .gitignore
├── LICENSE.md
├── README.md
└── requirements.txt
```

## Notes

- `paper/final/figures/` is the canonical paper figure location.
- Root `figures/` is not a canonical artifact store after cleanup.
- `docs/` remains ignored. Audit outputs are written locally to `docs/report.md` and `docs/diff.md`.
- `.repo_cleanup_backup/` is the local-only holding area for moved legacy, draft, and noncanonical material.

## License

All rights reserved. See [`LICENSE.md`](LICENSE.md).
