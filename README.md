# R-CoMET-Proof-of-Concept
Geometric Regularization and Causal Validation of EEG Foundation Models (R-CoMET). Enhancing BCI robustness against representational drift using Riemannian Geometry and TMS-EEG.
# R-CoMET: Riemannian-Regularized EEG Foundation Models

This repository contains the **Proof-of-Concept (PoC)** and preliminary stability analysis for the **R-CoMET** framework, proposed as part of a doctoral research project at **KU Leuven**.

## Overview
Modern neural decoding faces a major challenge: **Representational Drift**. Traditional EEG foundation models are often "geometry-blind," optimizing for Euclidean correlations that fail to capture the intrinsic non-linear manifold of brain dynamics. 

**R-CoMET** introduces a paradigm shift by:
1. **Geometric Regularization:** Integrating Riemannian Manifolds (SPD matrices) into the Transformer backbone.
2. **Causal Validation:** Utilizing concurrent TMS-EEG to quantify the Causal Alignment Index (CAI).
3. **Ecological Robustness:** Ensuring stability in high-noise environments (VR/Clinical).

## Preliminary Results (Proof of Concept)
We conducted a representational stability analysis on the **BNCI2014001** real-world EEG dataset. The results demonstrate that mapping neural signals to a Riemannian manifold significantly enhances class separability compared to standard Euclidean latent spaces.



* **Left (Euclidean):** Shows significant "Manifold Collapse" where different cognitive tasks (Hand, Feet, Tongue imagery) overlap heavily.
* **Right (Riemannian):** Shows distinct, stable clusters, proving that geodesic distance preserves the intrinsic geometry of the neural signal and mitigates drift.

## 🛠️ Requirements & Installation
This analysis is implemented in Python using the following libraries:
- `mne`: For EEG data management.
- `pyriemann`: For Riemannian geometry and covariance estimation.
- `moabb`: For benchmarking on real-world datasets.
- `scikit-learn`: For MDS and manifold visualization.

To run the analysis:
```bash
pip install mne pyriemann moabb scikit-learn matplotlib
