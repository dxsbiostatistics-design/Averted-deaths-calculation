Title

R code for meta-analysis of screening-associated stage migration and core calculation of deaths averted by cancer screening in China

Overview

This repository contains the core R scripts used in our study of screening-averted deaths for six major cancers in China. The repository includes code for:

Meta-analysis of stage distribution in screening programmes
estimation of stage-specific proportions across studies
separate pooled estimates for Chinese and multi-country screening programmes
adjustment for overdiagnosis in stage I disease
Core modelling of deaths averted by screening
estimation of expected deaths under non-screening and screening scenarios
calculation of deaths averted under China-specific and multi-country screening scenarios
incorporation of screening adherence into the modelling framework
Included scripts
01_meta_stage_distribution.R
Performs the meta-analysis of stage distributions for six cancers and applies overdiagnosis correction.
08_averted_deaths_core_model.R
Uses stage distributions, stage-specific mortality risks, incidence counts, and adherence rates to estimate deaths averted under different screening scenarios.
Required R packages

The scripts require the following R packages:

readxl
dplyr
tidyr
metafor
Input data

The scripts require Excel input files placed in the working directory:

file1:number of stage for six major cancers (0-六癌分期整理.xlsx)
Used for the meta-analysis of stage distribution.
file2:stage distribution derived from meta-analysis (8-stage.data.xlsx)
Used for the averted-death calculations.
Expected variables

For 8-stage.data.xlsx, the following variables are required:

Cancer
Group
Stage
Percentage
Group values

The code assumes the following groups:

Non-screening
Multi-country screening
Chinese screening
Stage values

The code assumes four stages:

I
II
III
IV
Cancers included

The analysis includes six major cancers:

Lung
Female breast
Colorectum
Oesophagus / Esophagus
Stomach
Liver
How to run
Place the required Excel files in the working directory.
Open R or RStudio.
Install required packages if needed.
Run the scripts in sequence:
source("01_meta_stage_distribution.R")
source("08_averted_deaths_core_model.R")
Outputs

The scripts generate:

pooled stage distributions by cancer and stage
corrected stage distributions after overdiagnosis adjustment
expected deaths under non-screening and screening scenarios
averted deaths under ideal uptake and observed adherence
death reduction percentages for each cancer

Some output lines for writing Excel files are included in the scripts but commented out.

Notes
These scripts provide the core analytical code only.
The repository does not include full patient-level data.
Users may need to adapt file paths and input file names to their own environment.
Cancer names and grouping labels in the input files must exactly match those used in the scripts.
Reproducibility

All custom R code used in these analyses is publicly available without restriction in this repository. The repository includes code for the meta-analysis, calculation of deaths averted, and bias correction.

Contact

For questions regarding the code, please contact the corresponding author.
