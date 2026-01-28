# Data Directory

This directory contains all data files for the HNB-DigiMedia project.

## Structure

### `raw/`
Original, unprocessed data files as received from data sources.
- **Do not modify** files in this directory
- Preserve original file names and formats
- Document data provenance in accompanying metadata files

### `processed/`
Cleaned, transformed, and analysis-ready datasets.
- Standardized formats (CSV, RDS)
- Documented variable definitions
- Reproducible from raw data via preprocessing scripts

### `external/`
External reference data and resources.
- Sentiment lexicons (Croatian financial vocabulary)
- Actor classification codebooks
- Event calendars (HNB policy decisions, ECB meetings)
- Geographic/demographic reference tables

## Data Security

- Large data files (>100MB) should be stored externally (Dropbox, institutional server)
- Sensitive or restricted data should not be committed to Git
- Use `.gitignore` to exclude data files as needed

## Primary Dataset Location

Main dataset (`hnb.rds`) is stored at: `C:/Users/lsikic/Dropbox/hnb.rds`

This file contains ~19,100 articles with the following key variables:
- Article metadata (ID, date, source, URL)
- Content (title, text, author)
- Engagement metrics (likes, comments, shares, reach)
- Classification fields (sentiment, actor type, frame)
