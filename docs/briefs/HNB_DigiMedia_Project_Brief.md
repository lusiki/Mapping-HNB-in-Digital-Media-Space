# Project Brief: Attention Markets in Central Bank Communication
## Analysis of Croatian National Bank Coverage in Digital Media

**Project Codename:** HNB-DigiMedia
**Version:** 1.0
**Date:** January 2026
**Principal Investigator:** Luka Šikić

---

# I. PROJECT OVERVIEW

## Background

This project applies the attention economics framework to analyze how Croatian National Bank (Hrvatska narodna banka, HNB) related content performs in the Croatian digital media ecosystem. The methodology is adapted from the DigiKat project, which successfully mapped the Croatian Catholic digital media space using attention economics principles.

## Core Premise

Central bank communication has evolved from deliberate opacity to strategic transparency. In contemporary digital environments, official monetary policy communications compete for attention against financial journalists, analysts, influencers, and social media speculation. This project investigates whether attention economics principles observed in religious digital media (extreme concentration, institutional disadvantage, emotional drivers, calendar-based rhythms) also manifest in financial/monetary policy communication.

## Unique Opportunity: Euro Adoption

Croatia adopted the Euro on January 1, 2023. This represents a natural experiment unavailable in Eurozone legacy members, allowing pre/post comparison of central bank communication dynamics when the institution's core function fundamentally changes.

## Research Objectives

1. Map the structure and dynamics of HNB-related digital media coverage
2. Quantify attention distribution across platforms and actor types
3. Test whether official HNB communication achieves visibility proportional to its policy relevance
4. Analyze how different actors frame monetary policy and which frames capture attention
5. Examine how monetary policy events structure attention rhythms
6. Assess the Euro adoption effect on communication ecosystem

---

# II. THEORETICAL FRAMEWORK

## Primary Theory: Attention Economics

The attention economics paradigm (Simon, 1971; Goldhaber, 1997; Davenport & Beck, 2001) posits that in information-rich environments, attention becomes the scarce resource. Key predictions:

- Attention distributes according to power law, not normal distribution
- Winner-take-all dynamics emerge from preferential attachment
- Platform algorithms shape attention allocation
- Emotional content captures disproportionate attention

## Supporting Theories

| Theory | Key Authors | Application |
|--------|-------------|-------------|
| Central Bank Communication | Blinder et al. (2008) | Effectiveness depends on reaching target audiences |
| Media Framing | Entman (1993) | Different frames affect public understanding |
| Information Cascades | Banerjee (1992) | How news spreads and potentially distorts |
| Credibility and Trust | Kydland & Prescott (1977) | Digital metrics as credibility proxy |
| Negativity Bias | Baumeister et al. (2001) | Negative news captures more attention |

## Conceptual Translation from DigiKat

| DigiKat (Religious Media) | HNB Analysis (Financial Media) |
|---------------------------|--------------------------------|
| Religious digital ecosystem | Financial/monetary policy ecosystem |
| Attention to religious content | Attention to central bank communication |
| Liturgical calendar rhythms | Monetary policy calendar rhythms |
| Institutional Church vs. grassroots | Official HNB vs. financial commentators |
| Emotional devotion (LOVE reactions) | Economic sentiment (FEAR, TRUST, UNCERTAINTY) |
| 173 years of Catholic publishing | 34 years of HNB independence, Euro adoption 2023 |
| Actor types: clergy, laity, institutions | Actor types: regulators, banks, media, influencers |

---

# III. RESEARCH QUESTIONS AND HYPOTHESES

## Research Questions

**RQ1:** How is attention to HNB-related content distributed across digital platforms and actors?

**RQ2:** Does official HNB communication achieve visibility proportional to its policy relevance, or does it suffer an institutional attention gap?

**RQ3:** How do different actors frame monetary policy, and which frames capture more attention?

**RQ4:** What role do monetary policy events play in structuring attention rhythms?

**RQ5:** How did Euro adoption affect the structure of HNB-related digital communication?

## Hypotheses

**H1 (Power Law Distribution):** Attention to HNB-related content follows a power law distribution with extreme concentration (Gini coefficient > 0.80, power law R² > 0.90).

**H2 (Institutional Attention Gap):** Official HNB sources achieve lower engagement rates than financial media outlets and financial influencers, reflecting misalignment between institutional communication styles and platform affordances.

**H3 (Sentiment Asymmetry):** Negative economic news captures disproportionately more attention than positive or neutral news, consistent with negativity bias in news consumption.

**H4 (Event-Driven Attention):** Monetary policy events (interest rate decisions, inflation reports, governor speeches) generate attention spikes 3-5 times above baseline levels.

**H5 (Euro Transition Effect):** Euro adoption (January 1, 2023) represents a structural break in attention patterns, with decreased HNB-specific attention and increased ECB/European framing post-adoption.

**H6 (Source Credibility Hierarchy):** Official HNB sources are cited more frequently in quality/specialized financial media but less frequently in general news portals and social media.

---

# IV. DATA REQUIREMENTS

## Corpus Definition

| Parameter | Specification |
|-----------|---------------|
| **Time period** | January 1, 2019 to December 31, 2024 (6 years) |
| **Geographic scope** | Croatian digital media, plus international sources covering Croatia |
| **Languages** | Croatian (primary), English (international coverage) |
| **Unit of analysis** | Individual article/post/video |

## Keyword Taxonomy

### Primary Keywords (Croatian)
```
HNB, Hrvatska narodna banka, guverner, Boris Vujčić, 
monetarna politika, kamatne stope, kamatna stopa,
inflacija, euro, kuna, tečaj, devizne rezerve,
financijska stabilnost, bankarski sektor, krediti,
Europska središnja banka, ESB, ECB
```

### Secondary Keywords (Context)
```
cijene, poskupljenje, rast cijena, životni standard,
štednja, depoziti, zajmovi, hipoteka, stambeni krediti,
eurozona, ERM II, konvergencija, maastrichtski kriteriji
```

### Exclusion Terms
```
# Exclude unrelated "euro" mentions
euro kvalifikacije, euro nogomet, eurovizija, eurosong
```

## Platform Coverage

| Platform | Priority | Collection Method | Expected Volume |
|----------|----------|-------------------|-----------------|
| Web portals (news sites) | High | Web scraping | Very high |
| Facebook | High | CrowdTangle or Meta API | High |
| Twitter/X | High | Academic API / alternatives | Moderate |
| YouTube | Medium | YouTube Data API | Moderate |
| Forums (Forum.hr) | Medium | Web scraping | Moderate |
| Reddit (r/croatia, r/financije) | Medium | Reddit API | Low-moderate |
| Instagram | Low | CrowdTangle | Low |
| LinkedIn | Low | Manual or API | Low |

## Required Variables per Record

| Variable | Description | Type |
|----------|-------------|------|
| `ID` | Unique identifier | String |
| `DATE` | Publication date | Date |
| `TIME` | Publication time | Time |
| `SOURCE` | Publisher/account name | String |
| `SOURCE_TYPE` | Platform category | Categorical |
| `URL` | Original URL | String |
| `TITLE` | Article/post title | String |
| `TEXT` | Full text content | String |
| `AUTHOR` | Author name (if available) | String |
| `INTERACTIONS` | Total engagement (likes + comments + shares) | Integer |
| `LIKES` | Like/reaction count | Integer |
| `COMMENTS` | Comment count | Integer |
| `SHARES` | Share/retweet count | Integer |
| `FOLLOWERS` | Account follower count at time of posting | Integer |
| `REACH` | Estimated reach (if available) | Integer |
| `SENTIMENT` | Automated sentiment score | Numeric |
| `ACTOR_TYPE` | Classified actor category | Categorical |
| `FRAME_TYPE` | Identified framing category | Categorical |
| `EVENT_PROXIMITY` | Days from nearest policy event | Integer |

---

# V. ACTOR CLASSIFICATION SYSTEM

## Classification Hierarchy

The classification follows a priority-based hierarchical system, processing each source through multiple identification layers. This mirrors the DigiKat approach but adapted for financial media context.

### Priority 1: Manual Overrides (Known High-Visibility Sources)

```
OFFICIAL_HNB = [
    "hnb.hr", "hrvatska narodna banka", "hnb", 
    "boris vujčić", "boris vujcic", "guverner hnb"
]

FINANCIAL_REGULATORS = [
    "hanfa", "ministarstvo financija", "porezna uprava",
    "hrvatska agencija za nadzor financijskih usluga"
]

MAJOR_FINANCIAL_MEDIA = [
    "poslovni dnevnik", "lider", "lider media", "seebiz",
    "bloomberg adria", "tportal poslovni", "poslovni.hr"
]

COMMERCIAL_BANKS = [
    "zagrebačka banka", "zaba", "privredna banka zagreb", "pbz",
    "erste bank", "otp banka", "raiffeisen", "addiko",
    "hrvatska poštanska banka", "hpb", "podravska banka"
]

INTERNATIONAL_SOURCES = [
    "reuters", "bloomberg", "financial times", "ecb",
    "european central bank", "imf", "world bank", "ebrd"
]
```

### Priority 2: Domain-Based Classification

```
domain_patterns = {
    "Official HNB": ["hnb.hr"],
    "Financial Regulators": ["hanfa.hr", "mfin.gov.hr"],
    "Financial Media": ["poslovni.hr", "lider.media", "seebiz.eu", "bloombergadria.com"],
    "General News - Quality": ["jutarnji.hr", "vecernji.hr", "novilist.hr", "slobodnadalmacija.hr"],
    "General News - Tabloid": ["24sata.hr", "index.hr", "net.hr", "dnevnik.hr"],
    "Public Broadcaster": ["hrt.hr", "rtl.hr", "novatv.hr"],
    "News Agency": ["hina.hr"],
    "Academic": ["eizg.hr", "hnbneuf.hr", "efzg.hr", "efst.hr"]
}
```

### Priority 3: Name Pattern Matching

```
# Political actors (government, opposition)
political_patterns = [
    "vlada", "ministar", "sabor", "predsjednik", "hdz", "sdp",
    "zastupnik", "premijer", "plenković", "plenkovic", "milanović"
]

# Academic/expert
academic_patterns = [
    "profesor", "prof.", "dr.", "ekonomist", "analitičar",
    "institut", "fakultet", "sveučilište"
]

# Banking sector
banking_patterns = [
    "banka", "bank", "direktor banke", "glavni ekonomist"
]

# Financial influencers (social media native)
influencer_indicators = [
    high follower count on finance topics,
    regular financial commentary,
    not affiliated with institution
]
```

### Priority 4: Platform-Aware Classification

```
# Social media specific rules
if platform in ["twitter", "facebook", "instagram", "youtube"]:
    if is_verified_account and has_institutional_affiliation:
        classify based on affiliation
    elif follower_count > 5000 and financial_content_ratio > 0.5:
        classify as "Financial Influencer"
    else:
        classify as "Public Discourse"

# Forum/comment specific
if platform in ["forum", "reddit", "comment"]:
    classify as "Public Discourse"
```

### Priority 5: Default Classification

```
if no_match_found:
    return "General Media" if is_media_outlet else "Public Discourse"
```

## Final Actor Categories (10 Types)

| Code | Category | Definition | Examples |
|------|----------|------------|----------|
| `HNB` | Official HNB | Direct central bank communication | hnb.hr, governor speeches, press releases |
| `REG` | Financial Regulators | Other regulatory bodies | HANFA, Ministry of Finance, DZS |
| `BNK` | Commercial Banks | Banking sector communication | Erste, PBZ, ZABA corporate communications |
| `FIN` | Financial Media | Specialized business journalism | Poslovni dnevnik, Lider, SEEbiz |
| `GEN` | General Media | Mainstream news coverage | Index, Jutarnji, 24sata, HRT |
| `INT` | International Sources | Foreign media and institutions | Reuters, Bloomberg, ECB, IMF |
| `ACA` | Academic/Expert | Economists, researchers, analysts | EIZ, university economists, think tanks |
| `POL` | Political Actors | Government, opposition commentary | Ministers, MPs, party statements |
| `INF` | Financial Influencers | Social media finance personalities | Twitter economists, YouTube explainers |
| `PUB` | Public Discourse | Forums, comments, general public | Reddit, Forum.hr, article comments |

---

# VI. SENTIMENT AND FRAMING ANALYSIS

## Sentiment Categories

Unlike the DigiKat emotional reaction analysis (LOVE, WOW, HAHA, SAD, ANGRY), financial media sentiment requires economic-specific categories:

| Sentiment | Definition | Indicators |
|-----------|------------|------------|
| **POSITIVE** | Optimistic economic outlook | growth, recovery, stability, improvement, success |
| **NEGATIVE** | Pessimistic economic outlook | crisis, decline, inflation, recession, risk, threat |
| **NEUTRAL** | Factual reporting without valence | reports, announces, states, according to |
| **FEAR/ALARM** | Crisis framing, dramatization | warns, danger, collapse, urgent, alarming |
| **REASSURANCE** | Stability messaging, calming | under control, stable, confident, managing |
| **UNCERTAINTY** | Ambiguous outlook | may, could, uncertain, depends, scenario |

## Croatian Financial Sentiment Lexicon

```r
# Positive economic terms
positive_financial <- c(
  "rast", "porast", "povećanje", "oporavak", "stabilnost", "stabilan",
  "investicije", "ulaganja", "zaposlenost", "zapošljavanje",
  "izvoz", "suficit", "višak", "konvergencija", "napredak",
  "poboljšanje", "optimizam", "povjerenje", "likvidnost",
  "profitabilnost", "solventnost", "kapitaliziranost"
)

# Negative economic terms
negative_financial <- c(
  "inflacija", "poskupljenje", "kriza", "pad", "smanjenje",
  "recesija", "deficit", "manjak", "dug", "zaduženost",
  "nezaposlenost", "deprecijacija", "devalvacija", "šok",
  "gubitak", "propadanje", "stečaj", "nelikvidnost",
  "nesigurnost", "volatilnost", "turbulencije"
)

# Fear/alarm terms
fear_terms <- c(
  "upozorava", "prijeti", "opasnost", "alarm", "hitno",
  "dramatično", "katastrofa", "kolaps", "urušavanje",
  "panika", "strah", "zabrinutost", "ozbiljno"
)

# Reassurance terms
reassurance_terms <- c(
  "pod kontrolom", "stabilizirano", "umiruje", "uvjerava",
  "sigurno", "zaštićeno", "otporno", "izdržljivo",
  "upravljivo", "predvidivo", "pouzdano"
)

# Uncertainty terms
uncertainty_terms <- c(
  "možda", "moguće", "moglo bi", "neizvjesno", "neizvjesnost",
  "rizik", "scenarij", "projekcija", "očekuje se",
  "ovisi o", "ako", "ukoliko", "pretpostavka"
)
```

## Framing Categories

| Frame | Definition | Typical Sources | Keywords |
|-------|------------|-----------------|----------|
| **TECHNICAL** | Expert monetary policy analysis | HNB, academics, financial media | kamatna stopa, monetarna transmisija, bazni efekt |
| **POLITICAL** | Policy as political choice/conflict | Political actors, general media | vlada, odluka, pritisak, odgovornost |
| **CONSUMER** | Impact on ordinary citizens | General media, tabloids | vaš novčanik, krediti, cijene, poskupljenje |
| **CRISIS** | Dramatization, alarm framing | Tabloids, some financial media | kriza, alarm, prijeti, dramatično |
| **REASSURANCE** | Stability and control messaging | HNB, government | pod kontrolom, stabilno, sigurno |
| **EUROPEAN** | EU/Eurozone context | International, some domestic | ECB, eurozona, EU, europski |
| **COMPARATIVE** | Croatia vs. others | Financial media, academics | usporedba, prosjek EU, regija, bolje/lošije od |

---

# VII. TEMPORAL ANALYSIS FRAMEWORK

## Monetary Policy Calendar

Unlike the stable liturgical calendar in DigiKat, the monetary policy calendar contains both regular and irregular events:

### Regular Events (Predictable)

| Event | Frequency | Pre-Euro | Post-Euro |
|-------|-----------|----------|-----------|
| Interest rate decision | 8x/year | HNB Council | ECB Governing Council |
| Inflation report (DZS) | Monthly | Same | Same |
| HNB Financial Stability Report | 2x/year | Same | Same |
| HNB Annual Report | 1x/year | Same | Same |
| Governor Bulletin/Speech | ~12x/year | Variable | Variable |
| HNB Macroeconomic Projections | 2x/year | Same | Same |

### Irregular Events (Unpredictable but significant)

| Event Type | Examples | Expected Effect |
|------------|----------|-----------------|
| External economic shocks | COVID-19, energy crisis, war | Very high spike |
| Banking sector events | Bank failures, mergers | High spike |
| Currency events | Pre-Euro: exchange rate moves | Moderate spike |
| Political interference | Government-HNB tensions | High spike |
| International ratings | S&P, Moody's, Fitch changes | Moderate spike |

### Event Window Analysis

```r
# Define event windows
event_analysis <- function(event_date, data, window_days = 3) {
  
  # Pre-event window
  pre_start <- event_date - window_days - 3
  pre_end <- event_date - window_days
  
  # Event window
  event_start <- event_date - window_days
  event_end <- event_date + window_days
  
  # Post-event window
  post_start <- event_date + window_days
  post_end <- event_date + window_days + 7
  
  pre_activity <- data[DATE >= pre_start & DATE < pre_end, .(
    volume = .N,
    engagement = sum(INTERACTIONS, na.rm = TRUE)
  )]
  
  event_activity <- data[DATE >= event_start & DATE <= event_end, .(
    volume = .N,
    engagement = sum(INTERACTIONS, na.rm = TRUE)
  )]
  
  # Calculate effect size
  volume_effect <- (event_activity$volume / as.numeric(event_end - event_start + 1)) /
                   (pre_activity$volume / as.numeric(pre_end - pre_start)) - 1
  
  return(list(
    event_date = event_date,
    pre_daily_volume = pre_activity$volume / as.numeric(pre_end - pre_start),
    event_daily_volume = event_activity$volume / as.numeric(event_end - event_start + 1),
    volume_effect_pct = volume_effect * 100
  ))
}
```

## Euro Adoption Analysis (Structural Break)

The Euro adoption on January 1, 2023 represents a natural experiment. Analysis should include:

### Period Definition

| Period | Dates | Characteristics |
|--------|-------|-----------------|
| **Pre-ERM II** | 2019-01-01 to 2020-07-09 | Full monetary sovereignty |
| **ERM II** | 2020-07-10 to 2022-12-31 | Transition period, fixed exchange rate |
| **Euro Era** | 2023-01-01 to 2024-12-31 | ECB monetary policy, HNB as transmission |

### Interrupted Time Series Design

```r
# Create period indicators
data[, period := case_when(
  DATE < as.Date("2020-07-10") ~ "Pre-ERM",
  DATE < as.Date("2023-01-01") ~ "ERM-II",
  TRUE ~ "Euro"
)]

# Interrupted time series model
library(CausalImpact)

# Define pre-period and post-period for Euro adoption
pre_period <- c(as.Date("2021-01-01"), as.Date("2022-12-31"))
post_period <- c(as.Date("2023-01-01"), as.Date("2024-12-31"))

# Run causal impact analysis
impact <- CausalImpact(time_series_data, pre_period, post_period)
```

### Expected Euro Effects

| Dimension | Hypothesis | Measurement |
|-----------|------------|-------------|
| HNB attention volume | Decrease (ECB becomes primary) | Daily article count |
| Actor diversity | More international sources | Entropy of actor distribution |
| Framing | More European, less national | Frame frequency analysis |
| Governor visibility | Decreased centrality | Named entity frequency |
| Public interest | Initial spike, then normalization | Search trends, engagement |

---

# VIII. ANALYTICAL METHODS

## 1. Market Structure and Concentration

**Identical methodology to DigiKat:**

| Measure | Formula/Method | Package |
|---------|----------------|---------|
| Gini coefficient | `ineq::ineq(x, type = "Gini")` | `ineq` |
| Lorenz curve | Cumulative distribution plot | `ggplot2` |
| Power law fit | `lm(log10(engagement) ~ log10(rank))` | base R |
| CR5, CR10, CR20 | Sum of top N shares | base R |
| HHI | Sum of squared market shares | base R |

## 2. Institutional Attention Gap

**Engagement rate calculation:**

```r
# Engagement rate per source (follower-normalized)
source_engagement <- data[, .(
  posts = .N,
  total_interactions = sum(INTERACTIONS, na.rm = TRUE),
  mean_followers = mean(FOLLOWERS, na.rm = TRUE),
  engagement_rate = sum(INTERACTIONS, na.rm = TRUE) / mean(FOLLOWERS, na.rm = TRUE) * 100
), by = .(SOURCE, ACTOR_TYPE)]

# Group comparison
source_engagement[, institution_group := fifelse(
  ACTOR_TYPE %in% c("HNB", "REG", "ACA"),
  "Institutional",
  "Non-Institutional"
)]

# Statistical test
wilcox.test(engagement_rate ~ institution_group, data = source_engagement)
kruskal.test(engagement_rate ~ ACTOR_TYPE, data = source_engagement)
```

## 3. Sentiment Analysis

```r
# Dictionary-based sentiment scoring
calculate_sentiment <- function(text, pos_dict, neg_dict, fear_dict, reassure_dict) {
  
  text_lower <- tolower(text)
  words <- unlist(strsplit(text_lower, "\\W+"))
  
  pos_count <- sum(words %in% pos_dict)
  neg_count <- sum(words %in% neg_dict)
  fear_count <- sum(words %in% fear_dict)
  reassure_count <- sum(words %in% reassure_dict)
  
  total_words <- length(words)
  
  return(list(
    positive_ratio = pos_count / total_words,
    negative_ratio = neg_count / total_words,
    fear_ratio = fear_count / total_words,
    reassure_ratio = reassure_count / total_words,
    net_sentiment = (pos_count - neg_count) / total_words,
    dominant_sentiment = case_when(
      fear_count > reassure_count & fear_count > neg_count ~ "FEAR",
      reassure_count > fear_count ~ "REASSURANCE",
      neg_count > pos_count ~ "NEGATIVE",
      pos_count > neg_count ~ "POSITIVE",
      TRUE ~ "NEUTRAL"
    )
  ))
}
```

## 4. Framing Analysis

```r
# Frame detection via keyword patterns
detect_frame <- function(text) {
  
  text_lower <- tolower(text)
  
  frames <- list(
    TECHNICAL = c("kamatna stopa", "monetarna politika", "transmisijski mehanizam",
                  "bazni efekt", "inflacijska očekivanja", "likvidnost"),
    POLITICAL = c("vlada", "ministar", "politička", "odluka vlade", "pritisak",
                  "odgovornost", "sabor", "oporba"),
    CONSUMER = c("vaš novčanik", "građani", "potrošači", "krediti", "rate",
                 "poskupljenje", "životni standard", "cijene u dućanima"),
    CRISIS = c("kriza", "alarm", "upozorenje", "dramatično", "prijeti",
               "kolaps", "katastrofa", "hitno"),
    REASSURANCE = c("pod kontrolom", "stabilno", "sigurno", "nema razloga za brigu",
                    "upravljivo", "očekivano"),
    EUROPEAN = c("ecb", "eurozona", "europska unija", "eu", "europska središnja banka",
                 "brisel", "frankfurt"),
    COMPARATIVE = c("u usporedbi", "prosjek eu", "regija", "slovenija", "mađarska",
                    "bolje od", "lošije od", "rang lista")
  )
  
  frame_scores <- sapply(frames, function(keywords) {
    sum(sapply(keywords, function(k) grepl(k, text_lower)))
  })
  
  if (max(frame_scores) == 0) return("NEUTRAL")
  return(names(which.max(frame_scores)))
}
```

## 5. Temporal Analysis

```r
# Daily aggregation
daily_stats <- data[, .(
  volume = .N,
  total_engagement = sum(INTERACTIONS, na.rm = TRUE),
  mean_sentiment = mean(SENTIMENT, na.rm = TRUE),
  unique_sources = uniqueN(SOURCE),
  hnb_share = sum(ACTOR_TYPE == "HNB") / .N
), by = DATE]

# Event effect analysis
events <- data.table(
  event_name = c("Interest Rate Decision", "Inflation Report", "Euro Adoption"),
  event_date = as.Date(c("2022-07-15", "2022-08-15", "2023-01-01")),
  event_type = c("regular", "regular", "structural")
)

event_effects <- lapply(1:nrow(events), function(i) {
  event_analysis(events$event_date[i], data, window_days = 3)
})
```

## 6. Network Analysis (Optional Advanced)

```r
# Citation/mention network
library(igraph)

# Extract mentions of sources/actors in articles
extract_citations <- function(text, source_list) {
  mentioned <- source_list[sapply(source_list, function(s) grepl(s, text, ignore.case = TRUE))]
  return(mentioned)
}

# Build citation network
edges <- data[, .(
  from = SOURCE,
  to = extract_citations(TEXT, unique(data$SOURCE))
), by = ID]

citation_network <- graph_from_data_frame(edges, directed = TRUE)
```

---

# IX. OUTPUT SPECIFICATIONS

## Tables

| Table | Content | Purpose |
|-------|---------|---------|
| 1 | Platform distribution | Overview of ecosystem |
| 2 | Concentration measures | H1 testing |
| 3 | Top 10 sources | Elite identification |
| 4 | Actor type distribution | Ecosystem structure |
| 5 | Engagement rates by actor | H2 testing |
| 6 | Statistical tests summary | Hypothesis testing |
| 7 | Sentiment distribution | Overall tone |
| 8 | Sentiment by actor type | H3 testing |
| 9 | Framing by actor type | Framing analysis |
| 10 | Event effects | H4 testing |
| 11 | Euro period comparison | H5 testing |
| 12 | Hypothesis summary | Results synthesis |

## Figures

| Figure | Type | Content |
|--------|------|---------|
| 1 | Bar chart | Platform engagement efficiency |
| 2 | Lorenz curve | Attention inequality |
| 3 | Log-log scatter | Power law distribution |
| 4 | Violin plot | Institutional vs. non-institutional engagement |
| 5 | Heatmap | Sentiment by actor type |
| 6 | Heatmap | Framing by actor type |
| 7 | Time series | Daily volume with events marked |
| 8 | Bar chart | Event effects on attention |
| 9 | Interrupted time series | Euro adoption effect |
| 10 | Network diagram | Citation/information flow (optional) |

---

# X. IMPLEMENTATION ROADMAP

## Phase 1: Data Collection (Months 1-2)

| Task | Duration | Output |
|------|----------|--------|
| Finalize keyword taxonomy | 1 week | Keyword list document |
| Set up scraping infrastructure | 2 weeks | Working scrapers |
| Collect historical web data | 3 weeks | Web corpus |
| Collect social media data | 2 weeks | Social corpus |
| Data cleaning and deduplication | 1 week | Clean dataset |
| Manual validation sample | 1 week | Validation report |

## Phase 2: Classification and Annotation (Month 3)

| Task | Duration | Output |
|------|----------|--------|
| Apply actor classification | 1 week | Classified dataset |
| Manual validation of classification | 1 week | Accuracy report |
| Sentiment scoring | 1 week | Sentiment-annotated data |
| Frame detection | 1 week | Frame-annotated data |

## Phase 3: Analysis (Months 4-5)

| Task | Duration | Output |
|------|----------|--------|
| Descriptive statistics | 1 week | Summary tables |
| Concentration analysis | 1 week | H1 results |
| Engagement gap analysis | 1 week | H2 results |
| Sentiment analysis | 1 week | H3 results |
| Temporal analysis | 1 week | H4 results |
| Euro adoption analysis | 2 weeks | H5 results |
| Robustness checks | 1 week | Sensitivity analyses |

## Phase 4: Writing and Submission (Months 6-7)

| Task | Duration | Output |
|------|----------|--------|
| Draft preparation | 3 weeks | Full manuscript |
| Internal review | 1 week | Revised draft |
| Final revisions | 1 week | Submission-ready paper |
| Journal submission | 1 week | Submitted manuscript |

---

# XI. REFERENCE IMPLEMENTATION: DIGIKAT

The DigiKat project provides a working template for this analysis. Key files and approaches to reference:

## Code Structure

```
/analysis
  /01_data_collection
    - web_scraper.R
    - social_media_collector.R
  /02_classification
    - actor_classification_v4.R      # Adapt this for HNB actors
  /03_analysis
    - map_1_platform_actors.qmd      # Concentration analysis
    - map_3_emotional.qmd            # Sentiment analysis (adapt)
    - map_4_temporal.qmd             # Event analysis
  /04_paper
    - attention_markets_paper.qmd    # Full paper template
```

## Key Adaptations Required

| DigiKat Component | HNB Adaptation |
|-------------------|----------------|
| Actor classification lists | Replace with financial media actors |
| Emotional reactions (LOVE, ANGRY) | Replace with economic sentiment |
| Liturgical calendar | Replace with monetary policy calendar |
| Feast days | Replace with policy events |
| Liturgical seasons | Replace with economic/Euro periods |
| Religious keywords | Replace with financial keywords |

---

# XII. POTENTIAL CHALLENGES AND SOLUTIONS

| Challenge | Risk Level | Mitigation Strategy |
|-----------|------------|---------------------|
| Limited CrowdTangle access | High | Alternative: direct scraping, commercial tools |
| Twitter API restrictions | High | Use academic access, archive.org, alternative collectors |
| Croatian sentiment accuracy | Medium | Build custom dictionary, validate with manual coding |
| Actor misclassification | Medium | Manual validation sample, iterative refinement |
| Data gaps (older periods) | Medium | Use multiple sources, acknowledge limitations |
| Causal inference limitations | Medium | Multiple robustness checks, careful interpretation |
| HNB cooperation | Low | Frame as independent research, request official event calendar |

---

# XIII. EXPECTED DELIVERABLES

1. **Academic Paper** (~6500 words) targeting Journal of Central Banking or European Journal of Political Economy

2. **Dataset** (anonymized for sharing) with classified articles, sentiment scores, and engagement metrics

3. **Methodological Documentation** for replication

4. **Policy Brief** for HNB communication strategy (optional)

5. **Presentation** for academic conferences (ASSA, EEA, Croatian Economic Association)

---

# XIV. KEY CONTACTS AND RESOURCES

## Data Sources

| Source | Contact/Access | Purpose |
|--------|----------------|---------|
| HNB | Press office, public data | Official communications, event calendar |
| DZS | Public statistics | Inflation data, economic indicators |
| Meta/CrowdTangle | Academic application | Facebook/Instagram data |
| Twitter | Academic API application | Twitter data |

## Reference Literature

### Central Bank Communication
- Blinder, A. et al. (2008). Central bank communication and monetary policy: A survey of theory and evidence.
- Born, B. et al. (2014). Central bank communication on financial stability.

### Attention Economics
- Simon, H. (1971). Designing organizations for an information-rich world.
- Goldhaber, M. (1997). The attention economy and the net.
- Webster, J. (2014). The marketplace of attention.

### Media and Finance
- Tetlock, P. (2007). Giving content to investor sentiment.
- Gentzkow, M. & Shapiro, J. (2010). What drives media slant?

---

# XV. INSTRUCTIONS FOR CLAUDE

When working on this project, Claude should:

1. **Reference DigiKat methodology** as the proven template, adapting rather than reinventing

2. **Use R and data.table** as primary analytical tools, consistent with DigiKat

3. **Follow the priority-based classification system** exactly as specified

4. **Apply economic-specific sentiment analysis**, not generic sentiment tools

5. **Structure temporal analysis around policy events**, not calendar dates alone

6. **Always test the Euro adoption structural break** as the unique contribution

7. **Produce outputs in both English and Croatian** as needed

8. **Generate Quarto documents** (.qmd) for reproducibility

9. **Create visualizations consistent with DigiKat style** (ggplot2, viridis palette, minimal theme)

10. **Document all methodological decisions** for transparency

---

**Document prepared for project migration and new thread initialization.**

**End of Project Brief**
