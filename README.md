# Spatiotemporal Signal Propagation

## Project Description

This project analyzes spatiotemporal signal propagation in single-cell imaging data using biosensors associated with the ERK/MAPK and PI3K/AKT pathways. The analyses investigate how signaling activity propagates between neighboring cells, how propagation dynamics differ across mutations and how sensitive Relative Risk (RR)-based measurements are to analysis parameters.

The project includes multi-mutation comparisons of spatiotemporal propagation strength, lagged exposure analyses across different mutations, parameter robustness assessment and comparative analyses of ERK and AKT/FoxO signaling dynamics.

---

# Environment Setup

## Requirements

The project was developed and tested using:

```text
Python 3.12
Jupyter Notebook
```

---

## Clone Repository

```bash
git clone https://github.com/majadomanska/BS2-Spatiotemporal.git
cd BS2-Spatiotemporal
```

---

## Create Virtual Environment

```bash
python3 -m venv myenv
source myenv/bin/activate
```

---

## Install Required Packages

Install all required dependencies using:

```bash
pip install -r requirements.txt
```

---

# Reproducing Analyses

Open the corresponding notebook in Jupyter Notebook and run all cells sequentially.

## Task A1 — Mutation Comparison

Notebook:

```text
notebooks/TaskA1.ipynb
```

---

## Task A2 — Lagged Exposure Analysis

Notebook:

```text
notebooks/TaskA2_LaggedExposure.ipynb
```

---

## Task A3 — Parameter Robustness Assessment

Notebook:

```text
notebooks/TaskA3_ParameterRobustness.ipynb
```

---

## Task B1 — ERK vs. AKT Propagation Comparison

Notebook:

```text
notebooks/TaskB_IndependentResearch.ipynb
```

---

# Outputs

From Multi-Mutation Spatiotemporal Comparison:
- `mutations_barplot.png` -  Bar plot of mean relative risk by mutation (* = significant vs WT).
- `mutations_comparison_table.csv` - Per mutation: mean RR, spread, Mann–Whitney p-value vs WT, Bonferroni significance flag.
- `/comparison_mutation_ERKKTR_ratio/group_level_summary.csv` - Per mutation: mean/median relative risk across all sites.
- `/comparison_mutation_ERKKTR_ratio/block_level_summary.csv`- Per experiment–site: relative risk that a cell jumps soon after a neighbour jumps.
- `/comparison_mutation_ERKKTR_ratio/task_description.json` - Run settings and which mutations were included.

From agged Exposure Analysis Across Mutations:
- `lagged_exposure_plot.png` - line plot showing $RR(\tau)$ across temporal lags for WT and mutant cell lines  
- `lagged_exposure_table.csv` - summary table containing optimal lag $(\tau)$ * and maximum RR for each mutation
- `lagged_exposure_full_RR_by_tau.csv` - complete $RR(\tau)$ results for all tested temporal lags and mutations

From Parameter Robustness Assessment:
- `parameter_robustness_window_sweep.csv` - table containing $RR$ values and propagation statistics across tested future window parameters  
- `parameter_robustness_window_sweep.png` - plot showing Relative Risk as a function of future window size

From  ERK vs. AKT Propagation Comparison:
- `B1_ERK_vs_AKT_comparison_table.csv` - Per site × biosensor: RR and θ for WT, PTEN_del and AKT1_E17K
- `B1_add_ERK_vs_AKT_comparison_table.csv` -  Same metrics for extra PIK3CA_E545K and PIK3CA_H1047R sites
- `B1_concat_ERK_vs_AKT_comparison_table.csv` - All sites combined - input for stats and plots.
- `B1_ERK_vs_FoxO3A_RR_barplot.png` - bar plot of mean $RR$ by mutation, ERK vs FoxO3A side by side.
- `B1_ERK_vs_FoxO3A_theta_barplot.png` - bar plot of mean jump thresholds $(\theta)$ by mutation and biosensor.
- `mutations_comparison_table.csv` - Per mutation × biosensor: mean RR, spread, Mann–Whitney p vs WT, Bonferroni flag.
- `compare_rr_wszystkie.csv` - All sites pooled: one ERK vs FoxO3A RR comparison (Mann–Whitney). 
- `compare_rr_wzg_mutacji.csv` - Per mutation: ERK vs FoxO3A RR — Mann–Whitney p and Bonferroni flag.
- `/notebooks/B1_lag_analysis_profiles_official.csv` - RR at each time lag τ (0–30 frames) per mutation × biosensor.
- `/notebooks/B1_lag_analysis_summary_official.csv` - Best lag (τ*) and peak RR per mutation × biosensor.

---

