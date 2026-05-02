# R code for stage-migration meta-analysis and averted-death modelling in China

This repository contains the core R code used for the meta-analysis of screening-associated stage migration and the calculation of deaths potentially averted by cancer screening for six major cancers in China.

Main script: `clean_core_code_meta_averted_death.txt`

Required input files:
- `00_stage_distribution_raw.xlsx`: raw stage-distribution data used for the meta-analysis
- `08_stage_data_intermediate.xlsx`: manually prepared intermediate file derived from the meta-analysis output and used for the averted-death calculation

Required packages: `readxl`, `dplyr`, `tidyr`, `metafor`

This repository includes core analytical code only and does not contain patient-level data.
