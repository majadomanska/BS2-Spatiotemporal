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

## Outputs

From Multi-Mutation Spatiotemporal Comparison:
- mutations_barplot.png
- mutations_comparison_table.csv
-/comparison_mutation_ERKKTR_ratio/group_level_summary.csv
- /comparison_mutation_ERKKTR_ratio/block_level_summary.csv

From agged Exposure Analysis Across Mutations:
- `lagged_exposure_plot.png` - line plot showing $RR(\tau)$ across temporal lags for WT and mutant cell lines  
- `lagged_exposure_table.csv`
- `lagged_exposure_full_RR_by_tau.csv`

From Parameter Robustness Assessment:
- parameter_robustness_window_sweep.csv
- parameter_robustness_window_sweep.png

From  ERK vs. AKT Propagation Comparison:
- B1_add_ERK_vs_AKT_comparison_table.csv
- B1_concat_ERK_vs_AKT_comparison_table.csv
- B1_ERK_vs_FoxO3A_RR_barplot.png
- B1_ERK_vs_FoxO3A_theta_barplot.png
- compare_rr_wszystkie.csv
- compare_rr_wzg_mutacji.csv
- /notebooks/B1_lag_analysis_profiles_official.csv
- /notebooks/B1_lag_analysis_summary_official.csv

---

