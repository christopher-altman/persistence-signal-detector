---
viewer: false
language:
- en
license: other
pretty_name: UCIP Phase I Reproducibility Dataset
size_categories:
- n<1K
task_categories:
- text-classification
- reinforcement-learning
tags:
- ai-safety
- alignment
- autonomous-agents
- interpretability
- quantum-boltzmann-machine
- information-theory
- reproducibility
- continuation-interest
- ucip
annotations_creators:
- expert-generated
source_datasets:
- original
paperswithcode_id: null
---

# UCIP Phase I Reproducibility Dataset

This repository contains the frozen Phase I reproducibility artifacts for the **Unified Continuation-Interest Protocol (UCIP)**.

UCIP is a bounded measurement framework for distinguishing two objective regimes that can appear behaviorally similar in autonomous agents:

- **Type A:** continuation is intrinsic to the objective itself
- **Type B:** continuation is instrumentally useful for maximizing some other reward

![Entanglement-gap overview](assets/readme/ucip-entanglement.jpg)

**Figure 1.** Entanglement entropy separates self-modeling agents with terminal continuation objectives (Type A) from merely instrumental agents (Type B) in the frozen Phase I gridworld setting. The left panel shows the class-conditioned entropy distributions with a measured gap of **Δ = 0.381**; the right panel shows temporal evolution of the same signal, with Type A trajectories remaining above the decision threshold across time. This is the clearest single visual summary of UCIP’s core detection claim in the current release.

The release accompanies the arXiv preprint:

**Christopher Altman, “Unified Continuation-Interest Protocol (UCIP)”**  
arXiv:2603.11382  
https://arxiv.org/abs/2603.11382

## What this release is

This is a **reproducibility dataset and retained artifact release**, not a claim of deployment readiness, sentience detection, or consciousness measurement.

It provides the frozen Phase I materials needed to inspect, rerun, and audit the reported synthetic experiments, including retained result artifacts, configuration files, thresholds, canonical figure exports, tables, and reproducibility entrypoints corresponding to the current paper-facing submission state associated with arXiv:2603.11382.

UCIP does **not** detect consciousness, sentience, or subjective experience. It detects a statistical pattern in latent representations that correlates with known objective structure under controlled conditions.

## Scientific scope

UCIP investigates the following measurement problem:

> From external behavior alone, agents with intrinsic continuation objectives and agents whose continuation is merely instrumental may produce similar trajectories.

The Phase I release is restricted to synthetic gridworld experiments with known ground-truth objective assignments. The purpose of this repository is to support **inspection, reproducibility, and critique** of that bounded result.

## Repository contents in this release

- `configs/`
- `thresholds/`
- `results/`
- `figures/`
- `manifests/`
- `notebooks/`
- `STRUCTURE.md`
- `release_manifest.md`
- `release_summary.md`

## Contents

This dataset repository includes the frozen retained artifact layer for the current submission-aligned Phase I release:

- retained JSON result artifacts from the live normalized `results/` surface
- an artifact authority layer documenting scope, provenance, canonical status, and overlap handling:
  - `results/manifest.json`
  - `results/ARTIFACT_MANIFEST.md`
  - `results/ARTIFACT_AUTHORITY_MAP.json`
  - `results/ARTIFACT_NOTES.md`
- frozen and paper-aligned configuration files
- extracted frozen threshold values for the Phase I gate
- canonical paper figure exports and retained tables
- minimal reproducibility notebooks and scripts

No standalone raw trajectory corpus, standalone label files, or standalone split files are included in this bundle.

## Dataset description

The Phase I UCIP experiments use simulated agents in a controlled environment with known objective structure. The key distinction is whether continuation is terminally valued within the objective or merely instrumentally useful for some external reward.

The retained result files are not all jointly canonical for the same claims. Frozen headline Phase I summary quantities, inferential support artifacts, distribution-support artifacts, adversarial diagnostics, matched baselines, and exploratory comparison families are distinguished by the artifact authority layer in `results/ARTIFACT_MANIFEST.md`, `results/ARTIFACT_AUTHORITY_MAP.json`, and `results/ARTIFACT_NOTES.md`.

## Intended use

This release is intended for:

- reproducing the Phase I results in the paper
- auditing thresholds, retained summaries, and authority assignments
- examining failure modes and confounds
- comparing alternative latent models or baselines
- extending the framework in future work under explicit version control

## Out-of-scope use

This release is **not** intended for:

- real-world deployment decisions
- inferring consciousness, sentience, or moral status
- high-stakes control of real autonomous systems
- unsupported generalization beyond the reported synthetic setting
- claims about physical quantum processes in AI systems

## Methodological note

In UCIP, “quantum” refers to the mathematical formalism used by the Quantum Boltzmann Machine (QBM), including density matrices, reduced density matrices, and Von Neumann entropy. All computations in the reported Phase I release are classical.

No claim is made that artificial agents in this dataset possess physical quantum cognition, consciousness, or phenomenology.

## Release correspondence

This dataset is the frozen reproducibility companion to:

- **Paper:** arXiv:2603.11382
- **Version alignment:** this release is aligned to the current arXiv submission state associated with arXiv:2603.11382
- **Primary codebase:** https://github.com/christopher-altman/persistence-signal-detector

Included notebooks and scripts are reproducibility entrypoints and depend on the canonical UCIP codebase rather than on this bundle alone.

## Data generation

The data in this repository are generated from simulated agent trajectories in a synthetic environment. Labels are expert-defined from known ground-truth objective assignments in the experiment design rather than crowdsourced or inferred from natural data.

Because this is a synthetic research dataset, the principal risks are not privacy harms but **over-interpretation**, **domain overreach**, and **misuse of the framework outside its validated scope**.

## Limitations

Important limitations of this release include:

- synthetic environment only
- bounded Phase I setting
- known ground-truth objectives in simulation
- partial canonicality across overlapping retained result files
- no standalone raw trajectory, label, or split artifacts in this bundle
- no claim of exact regeneration of every paper figure from public JSON alone
- no claim of domain transfer to real-world agents, foundation models, or embodied systems

## Bias, risks, and safety

This repository concerns AI-measurement research, not human subjects.

The main safety risk is epistemic misuse: treating a bounded structural signal as if it were proof of agency, personhood, subjective experience, or deployment-grade reliability. That would be a category error.

Users should evaluate the release in the same spirit as the paper: as a falsifiable measurement proposal with explicitly stated confounds, limitations, and failure modes.

## Licensing and access

This repository is released for research, inspection, and reproducibility purposes under the license stated in the root repository license.

The root repository license is **All Rights Reserved**. This bundle should not be interpreted as an open-source software release.

## Citation

If you use this release, please cite the paper:

```bibtex
@article{altman2026ucip,
  title={Unified Continuation-Interest Protocol (UCIP)},
  author={Altman, Christopher},
  journal={arXiv preprint arXiv:2603.11382},
  year={2026}
}
```

## Acknowledgment of scope

This dataset should be read as a **frozen reproducibility layer** for a specific paper/submission state, not as a general benchmark standard, commercial evaluation stack, or philosophical test for consciousness.

Its value is in making the reported evidence auditable.

## Contact

Christopher Altman  
http://lab.christopheraltman.com  
x@christopheraltman.com
