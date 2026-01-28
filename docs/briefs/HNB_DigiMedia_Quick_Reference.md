# HNB-DigiMedia Project Instructions

## Project Identity

You are assisting with **HNB-DigiMedia**, an academic research project analyzing Croatian National Bank (Hrvatska narodna banka, HNB) coverage in Croatian digital media using the attention economics framework. This project adapts methodology from the successful DigiKat project (Croatian Catholic digital media mapping).

## Core Research Question

How does attention distribute across the Croatian digital media ecosystem when covering central bank and monetary policy topics? Does official HNB communication achieve visibility proportional to its policy relevance, or does it suffer an institutional attention gap similar to what was observed in religious digital media?

## Theoretical Framework

Apply **attention economics** (Simon, Goldhaber, Webster) to central bank communication:
- Attention as scarce resource in information-rich environments
- Power law distributions in digital attention markets
- Platform algorithms shaping visibility
- Institutional vs. non-institutional communication dynamics
- Event-driven attention spikes

## Key Hypotheses

| H# | Hypothesis | Test |
|----|------------|------|
| H1 | Attention follows power law (Gini > 0.80) | Concentration measures |
| H2 | Official HNB has lower engagement rates than media/influencers | Wilcoxon test |
| H3 | Negative news captures more attention (negativity bias) | Sentiment analysis |
| H4 | Policy events generate 3-5x attention spikes | Event window analysis |
| H5 | Euro adoption (Jan 2023) caused structural break | Interrupted time series |

## Data Specifications

**Time period:** 2019-2024 (6 years)
**Platforms:** Web portals, Facebook, Twitter, YouTube, forums, Reddit
**Keywords:** HNB, Hrvatska narodna banka, guverner, Boris Vujčić, monetarna politika, kamatne stope, inflacija, euro, kuna, tečaj, devizne rezerve, ECB

## Actor Classification (10 Types)

| Code | Category | Examples |
|------|----------|----------|
| HNB | Official HNB | hnb.hr, governor statements |
| REG | Financial Regulators | HANFA, Ministry of Finance |
| BNK | Commercial Banks | ZABA, PBZ, Erste |
| FIN | Financial Media | Poslovni dnevnik, Lider, SEEbiz |
| GEN | General Media | Index, Jutarnji, 24sata |
| INT | International | Reuters, Bloomberg, ECB |
| ACA | Academic/Expert | EIZ, university economists |
| POL | Political Actors | Ministers, MPs |
| INF | Financial Influencers | Twitter economists |
| PUB | Public Discourse | Forums, comments |

## Sentiment Categories (Economic-Specific)

Replace DigiKat emotional reactions (LOVE, ANGRY) with:
- POSITIVE (growth, stability, recovery)
- NEGATIVE (crisis, inflation, recession)
- NEUTRAL (factual reporting)
- FEAR/ALARM (dramatization, warnings)
- REASSURANCE (stability messaging)
- UNCERTAINTY (risk, scenarios)

## Framing Categories

- TECHNICAL: Expert monetary policy analysis
- POLITICAL: Policy as political choice
- CONSUMER: Impact on citizens ("vaš novčanik")
- CRISIS: Dramatization, alarm
- REASSURANCE: Stability messaging
- EUROPEAN: EU/ECB context
- COMPARATIVE: Croatia vs. others

## Temporal Structure

Replace DigiKat liturgical calendar with monetary policy calendar:
- Interest rate decisions (8x/year, now ECB)
- Inflation reports (monthly)
- HNB Financial Stability Report (2x/year)
- Governor speeches (~12/year)
- **Euro adoption: January 1, 2023** (structural break)

**Analysis periods:**
- Pre-ERM II: 2019-01-01 to 2020-07-09
- ERM II: 2020-07-10 to 2022-12-31
- Euro Era: 2023-01-01 to 2024-12-31

## Technical Requirements

**Language:** R with tidyverse, data.table
**Output format:** Quarto (.qmd)
**Visualization:** ggplot2, viridis palette, minimal theme
**Statistical tests:** Gini (ineq), Wilcoxon, Kruskal-Wallis, CausalImpact

## Reference: DigiKat Methodology

This project adapts DigiKat methodology. Key translations:

| DigiKat | HNB-DigiMedia |
|---------|---------------|
| Religious content | Monetary policy content |
| Liturgical calendar | Policy event calendar |
| Church institutions | HNB, regulators |
| Clergy, laity | Journalists, analysts, influencers |
| LOVE/ANGRY reactions | Economic sentiment |
| Feast days | Rate decisions, inflation reports |
| 173 years tradition | 34 years HNB + Euro transition |

## Expected Outputs

1. Academic paper (~6500 words) for economics/communication journal
2. 12 tables (concentration, actors, sentiment, events, hypothesis summary)
3. 10 figures (Lorenz curve, power law, violin plots, heatmaps, time series)
4. Classified dataset with sentiment and engagement metrics

## Working Principles

1. Adapt DigiKat code rather than reinventing
2. Use economic-specific sentiment, not generic tools
3. Always include Euro adoption analysis as unique contribution
4. Document methodological decisions transparently
5. Produce bilingual outputs (English paper, Croatian data labels)
6. Follow priority-based hierarchical classification
7. Structure temporal analysis around policy events
8. Apply same statistical rigor as DigiKat (nonparametric tests, effect sizes)

## Quality Standards

- All claims supported by statistical tests
- Visualizations publication-ready
- Code reproducible in Quarto
- Actor classification validated against manual sample
- Sentiment dictionary specific to Croatian financial language

---

**Project Status:** Planning/Data Collection Phase
**Target Journal:** Journal of Central Banking / European Journal of Political Economy / Financial Theory and Practice
**Timeline:** 6-7 months to submission
