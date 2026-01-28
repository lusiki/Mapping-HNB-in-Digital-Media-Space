# Code Directory

This directory contains all analysis code for the HNB-DigiMedia project.

## Structure

### `preprocessing/`
Data cleaning and preparation scripts.
- `01_load_data.R` - Load raw data from sources
- `02_clean_data.R` - Clean and standardize variables
- `03_create_variables.R` - Derive analytical variables
- `04_merge_datasets.R` - Combine data sources

### `analysis/`
Main analytical scripts corresponding to paper sections.
- `01_descriptive_stats.R` - Summary statistics and data overview
- `02_concentration_analysis.R` - Gini, HHI, power law tests (H1)
- `03_institutional_gap.R` - HNB vs media engagement analysis (H2)
- `04_sentiment_analysis.R` - Negativity bias tests (H3)
- `05_event_study.R` - Policy event attention spikes (H4)
- `06_structural_break.R` - Euro adoption CausalImpact (H5)
- `07_framing_analysis.R` - Frame classification and effects
- `08_robustness_checks.R` - Sensitivity analyses

### `visualization/`
Figure generation scripts.
- `fig_concentration.R` - Lorenz curves, Gini visualization
- `fig_temporal.R` - Time series plots
- `fig_comparison.R` - Actor/source comparisons
- `fig_events.R` - Event study visualizations
- `theme_hnb.R` - Custom ggplot2 theme for publication

## Coding Standards

- Use tidyverse style guide
- Document functions with roxygen2 comments
- Set random seeds for reproducibility
- Use relative paths from project root
- Keep scripts modular and focused
