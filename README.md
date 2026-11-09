# ML-Assisted Hybrid Optimization of a 6G Lower FR3 FBAW Filter

### Physics-Constrained Optimization | Gaussian Process Regression | SciPy | Reproducible Numerical Evaluation

## Overview

This research investigates ML-assisted hybrid optimization of a wideband Lower FR3 4Rx4 FBAW filter, comparing a conventional SLSQP baseline (V1.6) with a GPR-assisted hybrid optimization candidate (V0.6).

The study emphasizes reproducible numerical evaluation, robust multi-condition performance, transparent acceptance criteria, and rigorous analysis of optimization limitations.

## Optimization and Verification Workflow

- **V1.6:** Conventional SciPy SLSQP baseline. The retained design originated from an earlier checkpoint after unsuccessful SLSQP optimization attempts.
- **GPR stage:** Gaussian Process Regression models used in the broader candidate-generation workflow.
- **V0.6:** SciPy Powell optimization applied to previously verified candidate seeds.
- **V0.7:** Independent fixed-parameter numerical verification without additional optimization or ML retraining.

## Key Results

At 0.05 MHz frequency resolution:

| Condition | V1.6 Ripple (dB) | V0.6 Ripple (dB) | Limit (dB) |
|---|---:|---:|---:|
| Nominal | 0.498534 | 0.494399 | 0.50 |
| Q80 | 0.712867 | 0.699244 | 0.70 |
| Q60 | 0.860680 | 0.842217 | 0.85 |

The V0.6 candidate satisfies all specified ripple, bandwidth, and far-rejection constraints across the three operating conditions.

## Reproducible Evaluation

- 24 fixed-design evaluations.
- Four frequency-grid resolutions: 0.5, 0.25, 0.1, and 0.05 MHz.
- Three operating conditions: Nominal, Q80, and Q60.
- Consistent pass/fail conclusions across all four grids.
- Explicit reporting of numerical margins and insertion-loss tradeoffs.

## Limitations

The minimum Q80 ripple margin is only 0.000756 dB. Numerical grid convergence does not establish manufacturing tolerance or model-parameter robustness.

The upstream GPR candidate-generation provenance is incomplete in the reviewed package. The results therefore do not establish the independent causal superiority of GPR.

## Technical Report

[Read the V0.7 Technical Research Report](reports/Lower_FR3_ML_Hybrid_V0_7_Technical_Report.pdf)

## Research Areas

Machine Learning-Assisted Optimization · Scientific Computing · Gaussian Process Regression · Numerical Verification · RF Filter Design · Reproducible Engineering Evaluation

## Author

**Xian Ji, Ph.D. (George X. Ji)**

Electronics and Communications Engineering

GitHub: [gxji-2026](https://github.com/gxji-2026)
