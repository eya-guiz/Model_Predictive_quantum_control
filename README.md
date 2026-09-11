This repository contains the reproducibility code used to generate the
numerical results for *Model Predictive Quantum Control: A Modular Approach
for Efficient and Robust Quantum Optimal Control*.

## Implemented control schemes

- Basic MPQC
- Terminal-equality-constrained MPQC (TEC-MPQC)
- Artificial-setpoint MPQC
- Full-horizon open-loop quantum optimal control (QOC)

All direct MPQC–QOC comparisons use matched physical models, discretization,
objective functions, input bounds, initializations, and CasADi/IPOPT solver
settings unless stated otherwise.

## Numerical studies

- Basic MPQC solver benchmark over an equatorial family of single-qubit target
  states: CasADi/IPOPT versus analytic-gradient GRAPE/L-BFGS-B.
- Theorem-consistent TEC-MPQC stabilization for a single qubit, including
  terminal-residual, recursive-feasibility, and Lyapunov-decrease diagnostics.
- Comparison of TEC-MPQC and artificial-setpoint MPQC over random single-qubit
  targets, including the minimum feasible prediction horizon.
- Multi-qubit GHZ-state preparation: runtime–accuracy Pareto comparison of
  Basic MPQC and full-horizon QOC, together with an appendix sweep over the
  full horizon length.
- Closed-loop two-qubit Bell-state preparation with finite-shot Pauli
  tomography, quantifying the measurement-resource versus final-accuracy
  trade-off.

## Reproducibility

Each run writes a timestamped result directory containing the exact JSON
configuration, machine-readable CSV summaries, per-update diagnostics, and
generated figures. The supplied scripts and configurations reproduce the
reported numerical studies.

This repository is research code intended for reproducibility of the paper
results. It is not presented as a production-ready control-software package.
