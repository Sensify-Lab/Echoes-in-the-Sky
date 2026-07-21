# Scripts Overview

This folder contains the currently retained research scripts. Most were written against local research data stored outside this repository under generic `local_data/...` placeholders.

## Current Files

- `_bluesky_data_collection.py`
  Collects Bluesky posts for a fixed query set and date window.

- `add_sentiment_to_parquet.py`
  Adds sentiment scores and labels to parquet files.

- `cleanup_merged_columns.py`
  Removes unused columns from merged parquet outputs.

- `eo_bluesky_figures.py`
  Generates figures for the executive-order versus Bluesky comparison outputs.

- `sentiment_break_analysis.py`
  Runs structural-break analysis on sentiment time series.

- `sentiment_monthly_overview.py`
  Builds monthly sentiment summary tables and figures.

- `sentiment_theme_heatmap_labels.py`
  Produces labeled theme heatmaps from precomputed monthly tables.

- `sentiment_theme_monthly_overview.py`
  Generates per-theme monthly sentiment overview figures.

- `structure_break_analysis.py`
  Runs structural-break analyses on theme activity over time.

- `verify_parquet_schema.py`
  Prints schema details for a parquet file.

## Important Assumptions

- Paths under `local_data/...` are placeholders for the original research workspace and are not included in this repository.
- Most scripts write outputs next to the local datasets they analyze.
- Several scripts expect intermediate CSV or parquet files produced by earlier steps.

## Recommended Use

If you are adapting this repository:

1. Start by reading the constants at the top of each script.
2. Replace the hardcoded `BASE_DIR`, `WORK_DIR`, or parquet glob paths with your own local paths.
3. Run one script at a time rather than treating this folder as a complete pipeline.
4. Treat the checked-in sample CSVs as examples, not as full reproduction inputs.
