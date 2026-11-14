R code for a systematic review and meta-analysis on the effect of ischemic preconditioning on exercise performance.


Methods implemented
Effect size: Hedges' g for crossover designs (standardised mean change, metafor::escalc)
Model: random effects, DerSimonian–Laird estimator (metafor::rma)
Subgroups by outcome type: time-based, power/work (meta-analysed); repetitions, distance (narrative synthesis)
Sensitivity analysis for the assumed pre–post correlation: r = 0.5 (primary), 0.7 and 0.9
Moderators: IPC location, number of cycles, cuff pressure, time from IPC to exercise, comparator
Publication bias: Egger's regression test and trim-and-fill


How to run
Install R (version 4.0 or later). Required packages (metafor, dplyr, ggplot2, gridExtra, scales) are installed automatically on first run.
From the repository folder, run:

Rscript 01_meta_analysis.R
Rscript 02_figures.R


Licence and citation
MIT licence. If you use this code, please cite the article above.
Contact: Artur Terbalyan, Academy of Physical Education in Katowice (a.terbalyan@awf.katowice.pl), ORCID 0000-0002-3628-8849
