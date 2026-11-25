# CRM Coursework 1: Market Analysis and Stock Segmentation Using RFM

6BUIS017C CRM and CM with Business Intelligence, University of Westminster (IIT Sri Lanka).
Student: Steve Perera (W2052148)

## Contents
- `CRM_CW1_Tasks1_2.ipynb`: Google Colab notebook for Task 1 (data preparation and features) and Task 2 (segmentation and sensitivity)
- `data/`: saved data snapshot and outputs
  - `constituents.csv`, `adj_close.csv`, `close.csv`, `volume.csv`, `dividends.csv`, `splits.csv`, `benchmark_gspc.csv`
  - `metadata.json` and `task2_settings.json`: sources, retrieval date, package versions, seed and chosen k
  - `feature_table.csv`: one row per share (mean weekly return, beta, R, F, M)
  - `cluster_assignments.csv`: the four baseline solutions and the R and F only solution
  - `inclusion_exclusion_log.csv`: every ticker and why it was kept or removed
- `figures/`: all charts used in the report

## Settings
- Shares: S&P 500 list from Wikipedia, benchmark ^GSPC
- Period: 1 Jan 2021 to 31 Dec 2024 (yfinance end date 1 Jan 2025, exclusive)
- Observation date for RFM: 31 Dec 2024
- Random seed: 42

## How to run
1. Open the notebook in Google Colab.
2. Runtime, then Run all. This downloads fresh data and saves a new snapshot in `data/`.
3. To rerun from the saved snapshot instead, upload the `data/` folder and set `USE_CACHE = True` in the setup cell.
