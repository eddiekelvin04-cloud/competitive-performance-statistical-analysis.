# Advanced Statistical Evaluation of Competitive Performance Metrics

## Project Overview
This repository contains a comprehensive data engineering and statistical analysis pipeline executed on an un-modeled data environment (`Scores.csv`). The project isolates, operationalizes, and evaluates the relationship between a continuous performance metric (`passing_quote`) and discrete competitive success outcomes (`winner`). 

This independent study was compiled as formal evidence of special functional qualification for admission consideration to the **Master of Science in Data Science** program at **Technische Universität Dortmund**.

## Core Analytics Pipeline
1. **Data Ingestion & Integrity Audit:** Built a robust automated ingestion pipeline handling custom European semicolon delimiters (`sep=';'`), verifying 100% data density across $N = 304$ discrete records with zero missing data values.
2. **Exploratory Data Analysis:** Segmented cohort distributions to extract statistical metrics (means, medians, standard deviations, and range boundaries).
3. **Data Visualization:** Rendered a high-resolution comparative boxplot mapping the interquartile range (IQR) and median distribution shifts side-by-side.
4. **Inferential Hypothesis Testing:** Executed a two-tailed **Welch's T-Test** to account for unequal sample sizes ($n_{Loser} = 190$, $n_{Winner} = 114$) and heteroscedastic variances ($s^2_{Loser} = 36.84$, $s^2_{Winner} = 65.02$).

## Key Findings & Empirical Results
* **Descriptive Gap:** Successful competitors (Winners) exhibited a higher arithmetic mean ($\bar{x} = 81.08$, $\text{Median} = 83.0$) compared to non-successful entities ($\bar{x} = 78.84$, $\text{Median} = 79.0$).
* **Variance Anomaly:** Winners showed higher behavioral volatility ($s = 8.06$) than losers ($s = 6.07$), suggesting that success is heavily correlated with executing higher-risk, higher-reward strategies.
* **Statistical Significance:** The inferential framework yielded a **T-statistic of 2.5581** and an exact **P-value of 0.0113**. Because $p < 0.05$, the Null Hypothesis ($H_0$) was rejected with high mathematical confidence.

## Technologies Used
* **Language:** Python
* **Libraries:** `pandas`, `numpy`, `scipy.stats`, `matplotlib`, `seaborn`
* **Environments:** Jupyter Notebook

## Project Structure
* `/Data`: Raw data infrastructure (`Scores.csv`).
* `/Notebooks`: Main source code notebook containing data handling, visualization, and hypothesis scripts.
* `/Reports`: Final publication-quality PDF manuscripts submitted for institutional evaluation.
