# Ischemic preconditioning (IPC) and exercise performance – meta-analysis code

R code for a systematic review and meta-analysis on the effect of ischemic preconditioning on exercise performance. Manuscript in preparation; the full citation will be added on publication.

## Repository contents

| File | Description |
|---|---|
| `01_meta_analysis.R` | Extraction table, effect sizes, meta-analytic models, sensitivity, moderator and publication-bias analyses |
| `02_figures.R` | Publication figures 1–4 (forest, sensitivity, funnel, moderators) |
| `LICENSE` | MIT licence |

The extracted study-level data are embedded in `01_meta_analysis.R` (data frame `dat`), so no separate data file is needed.

## Methods implemented

- Effect size: Hedges' g for crossover designs (standardised mean change, `metafor::escalc`)
- Model: random effects, DerSimonian–Laird estimator (`metafor::rma`)
- Subgroups by outcome type: time-based, power/work (meta-analysed); repetitions, distance (narrative synthesis)
- Sensitivity analysis for the assumed pre–post correlation: r = 0.5 (primary), 0.7 and 0.9
- Moderators: IPC location, number of cycles, cuff pressure, time from IPC to exercise, comparator
- Publication bias: Egger's regression test and trim-and-fill

## How to run

1. Install R (version 4.0 or later). Required packages (`metafor`, `dplyr`, `ggplot2`, `gridExtra`, `scales`) are installed automatically on first run.
2. From the repository folder, run:

```
Rscript 01_meta_analysis.R
Rscript 02_figures.R
```

`01_meta_analysis.R` writes `IPC_meta_analysis_results.csv` (pooled estimates for each correlation scenario) and draft figures. `02_figures.R` runs `01_meta_analysis.R` automatically if needed and saves the final figures: `Figure1_forest.png`, `Figure2_sensitivity.png`, `Figure3_funnel.png`, `Figure4_moderators.png`. Figures use the Palatino font; if it is not installed, change `FONT` at the top of `02_figures.R`.

## Licence and citation

MIT licence. If you use this code, please cite this repository (and the article, once published).

Contact: Artur Terbalyan, Academy of Physical Education in Katowice (a.terbalyan@awf.katowice.pl), ORCID [0000-0002-3628-8849](https://orcid.org/0000-0002-3628-8849)
