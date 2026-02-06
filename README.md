# Trader Sentiment Analytics

Analyzing how market sentiment influences trader behavior, risk, and performance using real trading data.

---

## Overview

This repository contains an end-to-end analytics workflow that:
- cleans and validates trade-level historical data
- aligns trades with the Fear & Greed Index using **IST timestamps**
- engineers daily account-level performance and behavior features
- compares outcomes across **Fear vs Greed** sentiment regimes using robust statistics
- segments traders into actionable archetypes
- (bonus) builds a time-aware predictive model for next-day trading quality

The project is designed to reflect **real-world fintech and trading analytics**, prioritizing interpretability, risk awareness, and decision-ready insights.

---

## Requirements

- Python 3.9+ (3.10 / 3.11 recommended)
- Jupyter Notebook or Google Colab

Python packages:
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- statsmodels
- scikit-learn
- pytz

---

## Setup

###  1) Clone the repository
git clone <repo-url>
cd <repo-name>
###  2) (Optional) Create and activate a virtual environment
macOS / Linux
python -m venv venv
source venv/bin/activate
Windows
python -m venv venv
venv\Scripts\activate
### 3) Install dependencies
Install manually:

pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn pytz

Data
Place the datasets in the data/ directory:

data/historical_data.csv — trade execution history

data/fear_greed_index.csv — daily sentiment index

##How to Run
### Option A: Run locally (Jupyter)
**jupyter notebook**
Open notebook.ipynb (or your notebook filename) and run all cells from top to bottom.

### Option B: Run in **Google Colab**
Upload notebook.ipynb to Google Colab

Upload both CSV files to the Colab runtime or mount Google Drive

Update file paths in the notebook if needed

##Outputs
The notebook generates the following artifacts in the outputs/ directory:

outputs/daily_account_metrics.csv

### Daily account-level KPIs, including:

realized PnL

win rate

trade frequency

position sizing (mean and tail)

fee intensity (bps)

drawdown proxies

sentiment labels

outputs/account_segments.csv

### Trader archetypes based on:

activity level (infrequent / medium / frequent)

capital usage (retail-like vs whale-like)

consistency (risk-aware vs unstable)

### These files can be used directly in Power BI / Tableau or loaded into SQL for further analysis.

### Key Analyses Included
Fear vs Greed Performance Comparison
realized PnL

win rate

drawdowns
(using robust, distribution-aware methods)

Behavioral Shifts Across Sentiment Regimes
trade frequency

position sizing

directional bias

execution cost (fee intensity)

Trader Segmentation
activity-based segmentation

size-based segmentation

consistency and risk profiling

### Bonus Modeling
time-aware next-day outcome estimation

leakage-safe validation

class imbalance handling

### Notes on Reproducibility
All timestamps are normalized to Asia/Kolkata (IST) before merging sentiment with trades.

Realized performance metrics use closed PnL only to avoid noise from open positions.

Validation is designed to avoid lookahead bias in time-series modeling.

### License
This project is provided for evaluation and demonstration purposes.


---
