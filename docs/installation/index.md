# 🐍 Software Installation

To run the EPA141A assignments and labs you need a working **Python 3.12 environment** with the course packages installed, plus the **JUSTICE** climate model. We use **conda** to manage the environment.

```{admonition} Allow 15–30 minutes
:class: tip
The environment contains several large packages (GeoPandas, FaIR, EMA Workbench).
A fresh install typically takes 15–30 minutes depending on your internet speed.
```

```{admonition} Complete setup & orientation guide
:class: seealso

Need everything in one place — models, labs, assignments, and installation — with worked code examples and troubleshooting? Open the **[Setup & Orientation guide](../_static/setup_and_orientation.html)** (standalone HTML, opens in the same tab).
```

## Choose your installation method

::::{grid} 1 1 2 2
:gutter: 3

:::{grid-item-card} 🖱️ Graphical Installation
:link: graphical
:link-type: doc

**Recommended for most students.**
Uses Anaconda Navigator — no terminal required.
+++
[→ Graphical Installation](graphical.md)
:::

:::{grid-item-card} ⌨️ Command-Line Installation
:link: cli
:link-type: doc

**Faster and more reliable.**
Uses the `conda` terminal command.
+++
[→ Command-Line Installation](cli.md)
:::

::::

## What gets installed

The `epa141a` conda environment includes:

| Package | Version | Used in |
|---------|---------|---------|
| Python | 3.12 | All |
| JupyterLab | ≥ 4.0 | All |
| `ema-workbench` | ≥ 3.0 | All assignments & labs |
| `numpy`, `pandas` | latest stable | All |
| `matplotlib`, `seaborn` | latest stable | All |
| `scipy` | ≥ 1.10 | All |
| `SALib` | ≥ 1.4 | Assignment 2, Lab 2 |
| `platypus-opt` | ≥ 1.1 | Assignments 5–8, Labs 4–6 |
| `deap` | ≥ 1.4 | Assignments 5–8 |
| `ipyparallel` | ≥ 8.6 | Assignments 5–6 |
| `plotly` | ≥ 5.19 | Assignment 7, Lab 5 |
| `geopandas` | ≥ 0.14 | Assignment 7 |
| `fair` | **2.1.3 (exact)** | All (JUSTICE climate model) |
| `h5py` | ≥ 3.10 | All (JUSTICE HDF5 data files) |
| `pycountry` | ≥ 24.6 | All (JUSTICE region mapping) |
| `kaleido` | ≥ 0.2 | Assignment 7 (Plotly figure export) |
| `tqdm` | ≥ 4.0 | Assignments 1, 2, 3, 8 |

```{warning}
`fair` must be version **2.1.3 exactly**. JUSTICE was developed and tested against this version.
Do not upgrade it.
```

## Two-part installation

The setup has two parts:

1. **Create the conda environment** — installs all Python packages.
2. **Install JUSTICE in editable mode** — makes the `justice`, `solvers`, and `analysis` packages importable.

Both parts are covered step-by-step in the installation guides above.

## Verifying the installation

After installation, open `assignments_ema/assignment_01_exploratory_modeling.ipynb` and run **Exercise 0** (the first code cell). You should see output like:

```
✓  justice
✓  numpy
✓  pandas
✓  matplotlib
✓  ema_workbench
✓  scipy
✓  seaborn

Python 3.12.x
```

Every package should show `✓` with no red errors. If anything shows `✗`, see the Troubleshooting section at the bottom of the installation guide you followed.

## Kernel name

The Jupyter kernel is registered as **`EPA141A (JUSTICE)`**. Always select this kernel (not the base Python kernel) when opening assignment or lab notebooks.
