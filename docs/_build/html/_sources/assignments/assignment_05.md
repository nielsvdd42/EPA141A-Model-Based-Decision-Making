# Assignment 5 — Many-Objective Optimisation (Local Run)

**Key methods:** Borg MOEA · ε-NSGA-II · Platypus · Pareto-approximate set

---

## Learning objectives

1. Configure a **Many-Objective Evolutionary Algorithm** (ε-NSGA-II via Platypus/Borg) for the JUSTICE problem defined in Assignment 4.
2. Run optimisation **locally** using `ema_workbench`.
3. Inspect and plot the resulting **Pareto-approximate set** in objective space.
4. Understand the role of: population size, number of function evaluations (NFE), and ε values.
5. Save Pareto results to `results/` for convergence analysis in Assignment 6.

## Prerequisites

- **Assignment 4 completed** — the problem formulation (`config_student.json`) is required.

```{warning}
This assignment involves running an MOEA on JUSTICE. Allow **1–2 hours** for the optimisation
to complete on a standard laptop. Start early and do not close your computer during the run.
Results are saved automatically so you do not lose progress if you need to pause.
```

## Notebook

`assignments_ema/assignment_05_moea_local.ipynb`

## Submission

Submit `A5_<studentnumber>.ipynb` via Brightspace with all cells executed **and Pareto results saved** to `results/`.
