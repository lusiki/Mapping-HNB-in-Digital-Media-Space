# HNB-DigiMedia: Attention Economics of Central Bank Communication

**Analyzing Croatian National Bank (HNB) Digital Media Coverage Using Attention Economics Frameworks**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![R](https://img.shields.io/badge/R-4.0+-blue.svg)](https://www.r-project.org/)

## Overview

This repository contains the research materials, code, and analysis for studying how the Croatian National Bank's (HNB) monetary policy communications compete for attention in Croatia's digital media ecosystem. The study applies attention economics theory to examine institutional communication effectiveness during a critical period that includes Croatia's Euro adoption (January 1, 2023).

**Principal Investigator:** Luka Šikić
**Project Codename:** HNB-DigiMedia v1.0
**Timeline:** January 2019 - December 2024 (6 years of coverage)

## Research Questions

1. How is attention to HNB-related content distributed across Croatia's digital media ecosystem?
2. Do official HNB communications achieve engagement proportional to their policy importance?
3. How do framing strategies and sentiment affect attention capture for monetary policy content?
4. Did Euro adoption create a structural break in attention patterns?

## Hypotheses

| ID | Hypothesis | Prediction |
|----|------------|------------|
| H1 | Power Law Distribution | Attention concentration follows extreme inequality (Gini > 0.80) |
| H2 | Institutional Attention Gap | Official HNB engagement lower than media/influencers |
| H3 | Negativity Bias | Negative economic news captures disproportionate attention |
| H4 | Event-Driven Spikes | Policy events generate 3-5x attention increases |
| H5 | Euro Transition Effect | Euro adoption = structural break in attention patterns |

## Working Paper

**Central Bank Voice in the Fiscal Conversation** - [View Paper](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/paper/drafts/Central%20Bank%20Voice%20in%20the%20Fiscal%20Conversation.html)

## Analysis Maps

Interactive HTML visualizations of the HNB digital media landscape:

| Map | Description | Link |
|-----|-------------|------|
| **Map 1** | Source and Actor Structure | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map1_source_actor_structure.html) |
| **Map 2** | Thematic Structure | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map2_thematic_structure.html) |
| **Map 3** | Sentiment Structure | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map3_sentiment_structure.html) |
| **Map 4** | Temporal Dynamics | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map4_temporal_dynamics.html) |
| **Map 5** | Institutional Attention Gap | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map5_institutional_attention_gap.html) |
| **Map 6** | Source Concentration and Market Structure | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map6_source_concentration.html) |
| **Map 7** | Content Amplification Chains | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map7_content_amplification.html) |
| **Map 8** | Readability and Accessibility | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map8_readability_accessibility.html) |
| **Map 9** | Event Attribution Analysis | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map9_event_attribution.html) |
| **Map 10** | Audience Segmentation | [View Map](https://raw.githack.com/lusiki/Mapping-HNB-in-Digital-Media-Space/main/outputs/maps/map10_audience_segmentation.html) |

> **Note:** Download the repository and open HTML files locally, or view via GitHub Pages when enabled.

## Repository Structure

```
HNBAttention/
├── README.md                 # Project overview (this file)
├── LICENSE                   # MIT License
├── .gitignore               # Git ignore rules
│
├── data/                    # Data files
│   ├── raw/                 # Original, unprocessed data
│   ├── processed/           # Cleaned and transformed data
│   └── external/            # External reference data (lexicons, etc.)
│
├── code/                    # Analysis code
│   ├── analysis/            # Main analytical scripts
│   ├── preprocessing/       # Data cleaning and preparation
│   └── visualization/       # Figure generation scripts
│
├── docs/                    # Documentation
│   ├── briefs/              # Project briefs and methodology
│   └── notes/               # Research notes and memos
│
├── paper/                   # Manuscript materials
│   ├── drafts/              # Paper drafts
│   ├── figures/             # Publication-ready figures
│   └── tables/              # Publication-ready tables
│
└── outputs/                 # Generated outputs
    ├── maps/                # Interactive analysis maps (HTML)
    ├── figures/             # Exploratory figures
    └── reports/             # Analysis reports (HTML, PDF)
```

## Methodology

### Data Sources
- **Platforms:** 13 digital media types (news portals, Facebook, Twitter/X, YouTube, forums)
- **Coverage:** 19,100+ articles from 150+ media sources
- **Period:** January 2019 - December 2024

### Actor Classification System

| Code | Category | Description |
|------|----------|-------------|
| HNB | Official HNB | Central bank official communications |
| REG | Regulators | HANFA, Ministry of Finance, DZS |
| BNK | Commercial Banks | ZABA, PBZ, Erste, OTP |
| FIN | Financial Media | Poslovni dnevnik, Lider, SEEbiz |
| GEN | General Media | Index, Jutarnji, 24sata, N1 |
| INT | International | Reuters, Bloomberg, ECB, IMF |
| ACA | Academic | EIZ, university economists |
| POL | Political | Government, opposition, MPs |
| INF | Influencers | Social media financial commentators |
| PUB | Public | Forums, comments, Reddit |

### Analysis Periods

1. **Pre-ERM II** (2019-01-01 to 2020-07-09): Full monetary sovereignty
2. **ERM II** (2020-07-10 to 2022-12-31): Euro transition period
3. **Euro Era** (2023-01-01 to 2024-12-31): ECB monetary policy

### Analytical Methods

- Market concentration metrics (Gini, HHI, CR5/10/20)
- Sentiment analysis with Croatian financial lexicon
- Framing analysis (technical, political, consumer, crisis)
- Event study methodology
- Interrupted time series (CausalImpact)

## Requirements

### R Packages
```r
# Core
tidyverse, data.table, lubridate

# Text Analysis
quanteda, tidytext, sentimentr

# Visualization
ggplot2, ggrepel, patchwork, scales

# Statistical
ineq, CausalImpact, broom

# Reporting
quarto, knitr, kableExtra
```

## Getting Started

1. Clone the repository
2. Ensure R (4.0+) and required packages are installed
3. Place raw data in `data/raw/`
4. Run preprocessing scripts in `code/preprocessing/`
5. Execute analysis scripts in `code/analysis/`

## Target Publications

- Journal of Central Banking
- European Journal of Political Economy
- Financial Theory and Practice

## Citation

If you use this research, please cite:

```bibtex
@article{sikic2026hnb,
  title={Attention Economics of Central Bank Communication: Evidence from Croatia's Euro Adoption},
  author={Šikić, Luka},
  journal={TBD},
  year={2026}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Methodology adapted from the DigiKat project framework
- Croatian National Bank for public data availability
