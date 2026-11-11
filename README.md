# RLWM-data-analysis
The present repository is related to data analysis procedures in the paper "It depends on the Working Memory: Testing Correlations between Reinforcement Sensitivity Theory and Reinforcement Learning". Computational modeling analysis can be found in ipalmieri profile 

R scripts for the statistical analyses in Marques et al. (2026), *It depends on working memory: Testing correlations between Reinforcement Sensitivity Theory and Reinforcement Learning*. 

Preregistration: https://osf.io/qh4c6
Computational modelling code (Classic RL, RLWMi, RLWMi + Deduction): (https://github.com/ipalmieri/rlwm/tree/main/rlwm)

# Statistical analyses

| Script | Results in the paper |

| `01_correlations.R` | Table 1 (Pearson) and Table 2 (Spearman) |
| `02_mediation.R` | Sections 3.2 and 3.5 (lavaan, 5,000 bootstrap samples, seed 2026) |
| `03_regressions.R` | Section 3.6 and Figure 5 (exploratory) |

**Data.** Participant data are not included because the informed consent did not cover public data sharing. De-identified data are available from the corresponding author upon reasonable request, subject to ethics committee approval. The scripts expect a file `data.csv` (N = 110) with these columns:

- RLWM task: `Pcorrect_3`, `Pcorrect_6` (% correct, set size 3/6), `Persistence_3`, `Persistence_6` (perseverative errors), `NB2`, `NB3` (2-/3-back accuracy)
- RLWMi + Deduction parameters: `learning_rate`, `pers`, `eta3_wm`, `eta6_wm`
- RST-PQ: `RI_BAS_PQ`, `GDP_BAS_PQ`, `RR_BAS_PQ`, `Imp_BAS_PQ`, `BIS_PQ`, `FFFS_PQ`
- BIS/BAS: `DRIVE_BAS_CW`, `FS_BAS_CW`, `RR_BAS_CW`, `BIS_CW`
- `BIS_11`; DASS-21: `Depression_DASS`, `Anxiety_DASS`, `Stress_DASS`, `Total_DASS`

R packages: `psych`, `lavaan`, `ggplot2`.
