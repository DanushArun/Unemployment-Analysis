# Unemployment Analysis

An exploratory notebook comparing unemployment patterns across Indian regions and dates.
It visualizes two supplied datasets; it does not train a forecasting model.

## What is in the repository

[Task_2.ipynb](Task_2.ipynb) contains cleaning, regional comparisons, time-series plots and
before/after March 2020 summaries. Saved outputs show 740 rows in the first cleaned dataset
and 267 in the second. These are historical notebook outputs, not a fresh data verification.

## Run the analysis

```bash
git clone https://github.com/DanushArun/Unemployment-Analysis.git
cd Unemployment-Analysis
python3 -m venv .venv
source .venv/bin/activate
python -m pip install jupyter pandas numpy matplotlib seaborn
jupyter notebook Task_2.ipynb
```

Supply `Unemployment in India.csv` and `Unemployment_Rate_upto_11_2020.csv` separately.
Neither dataset is committed. Replace the author's absolute CSV paths before running cells.
Dependencies are not pinned, so package versions can affect reproducibility.

## Analysis flow

1. Load the two CSV files and normalize column names.
2. Parse dates, replace infinite values and remove missing rows.
3. Plot changes over time and compare regions.
4. Compare observations before and after March 2020.

The date parser coerces invalid dates to missing values. Cleaning therefore changes the
sample; inspect removed records before drawing conclusions.

## Evidence and limits

Notebook JSON and Python cell syntax were checked for this documentation update.
The analysis was not rerun because its input files are absent.

Regional averages and period comparisons describe the supplied samples. They do not establish
that a particular event caused unemployment changes, and they are not current economic data.
There is no automated test suite, deployment service or trained prediction artifact here.
