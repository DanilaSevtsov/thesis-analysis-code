# Still Carrying? Carry-Based Investing in Equities and Commodities

This repository contains the **R Markdown source** used to generate the empirical analysis from the master’s thesis *Still Carrying? Post-Publication Performance and Implementation of Equity & Commodity Carry*.  
**Data is not included.** All market data comes from Bloomberg and must be supplied by the user. The accompanying thesis PDF (not part of this repo) contains the figures, discussion, and write-up; this Rmd is the reproducible backbone of the analysis.

## Key points

- **Provided:** R Markdown file with all code to (re)compute carry, build portfolios (long-short, long-only, blends with FF3/momentum), apply risk controls (risk parity, volatility targeting), and evaluate implementation frictions (turnover, costs).  
- **Not provided:** Bloomberg data (required inputs), pre-rendered images/outputs (those appear in the thesis).  
- **Data source:** Bloomberg Terminal exports (e.g., futures/spot prices, dividend proxies, expiry schedules). Users must obtain their own licensed data.

## Requirements

- **R** (version ≥ 4.2 recommended)  
- **Core R packages** (install if missing):  
  `tidyverse`, `lubridate`, `readxl`, `purrr`, `dplyr`, `ggplot2`, `scales`, `tidyquant`, `quantmod`, `zoo`, `moments`, `RColorBrewer`, `corrplot`, `quadprog`, `slider`  
  Example installation snippet:
  ```r
  pkgs <- c("tidyverse","lubridate","readxl","purrr","dplyr","ggplot2","scales",
            "tidyquant","quantmod","zoo","moments","RColorBrewer","corrplot",
            "quadprog","slider")
  install.packages(setdiff(pkgs, installed.packages()[,1]))
