# withinhost_envstoch

This repository contains the inference code and the simulated data sets for the Virus Evolution publication titled "Environmental stochasticity can account for patterns of within-host respiratory virus evolution" by Xiao et al. (2026).This repository contains the inference code and the simulated data sets for the Virus Evolution publication titled "Environmental stochasticity can account for patterns of within-host respiratory virus evolution" by Xiao et al. (2026).



The analysis fits a logit-scale Brownian-motion model of environmental stochasticity to paired within-host variant frequency measurements. We show that environmental stochasticity can reproduce key features of empirically observed allele frequency changes. 

## Repository contents

| Path | Description |
|---|---|
| `data_gen.ipynb` | Builds the processed data tables from the raw source files and generates the simulated (mock) datasets, with and without measurement noise. |
| `measurement_error.ipynb` | Likelihood-based inference accounting for finite sequencing depth; produces the log-likelihood surfaces in `heatmap_results/`. |
| `fig_gen.ipynb` | Generates main text Figures 1–9. |
| `supplement.ipynb` | Generates Supplementary Figures S1–S9. |
| `data/` | Processed data tables and simulated datasets. |
| `data/raw_data/` | Original supplementary files from the published studies. |
| `heatmap_results/` | Precomputed log-likelihood surfaces. |

## Data

Processed tables of paired variant frequency measurements:

- `Table_S1.csv` — human influenza A virus (McCrone et al.)
- `Table_S2.csv` — SARS-CoV-2 (Tonkin-Hill et al.)
- `Table_S3.csv` — swine influenza A virus (Van Insberghe et al.)

Simulated datasets are stored as `.npy` arrays. 

## Requirements

Python 3.9+ with `numpy`, `scipy`, `pandas`, `matplotlib`, and `openpyxl` (for reading the raw `.xlsx` input).

```bash
pip install numpy scipy pandas matplotlib openpyxl jupyter
```
