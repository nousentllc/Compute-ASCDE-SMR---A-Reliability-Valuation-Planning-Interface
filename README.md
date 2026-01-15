# Nous Enterprises — UEVF / Compute-ASCDE

This repository hosts the working research stack behind **UEVF** and **Compute-ASCDE**: a reliability-complete valuation and planner interface for AI campuses, interconnection decisions, and grid-constrained power procurement.

The core thesis is simple: **MW-block planning fails for modern compute**. What matters is the joint geometry of (i) **goodput conversion** (useful tokens per facility joule), (ii) **workload stiffness** (cost + reliability penalty of interruption), and (iii) **temporal densification / sprinting**, because these primitives determine **seasonal tail coincidence** with scarcity hours and therefore the **reliability externality** imposed on the grid.

## What’s inside
- **Compute-ASCDE (AI)**: present value of total system cost divided by present value of survival-weighted reliable intelligence delivered.
- **Tranche control model**: explicit decomposition into stiff vs flexible compute with auditable controls and contract mapping.
- **Reliability translation layer**: MRV / eMRV shadow pricing via EUE (and seasonal tail event conditioning), suitable for insertion into fractional programs (e.g., Dinkelbach form).
- **Grid interface operators**: deliverability treated as an **active constraint geometry** (PTDF/interface binding sets), not a scalar factor.
- **SMR coupling interface (optional)**: SMR as boundary-condition state that restricts feasible control trajectories (minimum generation, ramp, availability, islanding, heat rejection, governance constraints).

## Why this matters
For hyperscale compute, the dominant planning risk is not “average energy cost”—it is **tail alignment**:
- queue delay vs silicon time,
- sprint coincidence with scarcity regimes,
- and feasibility constraints that turn “cheap” power into **non-deliverable** or **non-dispatchable** value.

This stack is intended to be **planner-usable**: it prioritizes explicit state, admissible control sets, and auditable assumptions over black-box claims.

## Status
Active research and tooling. The goal is a clean, reproducible interface suitable for:
- scenario sweeps,
- Monte Carlo evaluation,
- and decision support under ISO/RTO deliverability and reliability constraints.

## Quick navigation (typical)
- `papers/` — LaTeX sources and compiled PDFs (Compute-ASCDE variants, SMR coupling notes)
- `appendices/` — derivations, proofs, calibration protocols, verification kernels
- `data/` — (optional) anonymized/synthetic traces + schema notes
- `code/` — calibration scripts, Monte Carlo drivers, plotting utilities

(Directory names may evolve; treat this README as the intent-level map.)

## Citation / attribution
If you use this framework in analysis, benchmarking, or planning work, cite the relevant manuscript(s) in `papers/` and reference this repository as the implementation/workbench.

## Contact
Justin Candler — Nous Enterprises LLC  
Email: nousentllc@gmail.com
