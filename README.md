# Machine Learning and Predictive Analytics in Portfolio Optimisation  
*Applying Regularisation to Beat the Equal-Weighted Benchmark*  

**Course Project:** DBA3803 – Predictive Analytics in Business  
**Institution:** National University of Singapore (Exchange Semester)  
**Authors:** Group 19 (incl. Michaïl Maréchal)  
**Date:** October 2023  

---

## 📌 Project Overview  
This project explores how **regularisation techniques (Lasso & Ridge)** can be applied to **portfolio weight estimation** in order to avoid overfitting and enhance investment performance.  

The assignment benchmark was the **Equally Weighted (EW) Portfolio**, which our instructor suggested could not be consistently beaten. Through careful data selection, regularisation, and weight constraints, our group successfully **outperformed the EW portfolio in both cumulative returns and Sharpe ratio**.  

---

## ⚙️ Methodology  
- **Data:** Daily returns for 100 assets (252 trading days) from the Fama-French dataset  
- **Challenges:** Limited observations (252) vs. high dimensionality (99 covariates) → high overfitting risk  
- **Techniques Used:**  
  - **Lasso Regression:** Feature selection by shrinking irrelevant coefficients to zero  
  - **Ridge Regression:** Shrinking noisy variables to stabilize predictions  
  - **Fama-French Inspired Selection:** Focus on size (ME1–5) and value (BM6–10) factors → reduced to 24 assets  
  - **Weight Constraints:** Restricted asset weights (5th–95th percentile) to reduce volatility and avoid extreme bets  

---

## 📊 Key Findings  
- **Naive Lasso/Ridge (full dataset):** Failed to consistently outperform EW due to overfitting.  
- **Truncated dataset (24 assets):** Outperformed EW in cumulative returns (Lasso: 9.42%, Ridge: 9.32% vs. EW: 6.91%).  
- **With weight constraints:**  
  - Lasso: 26.61% cumulative return, Sharpe 0.054  
  - Ridge: 26.24% cumulative return, Sharpe 0.053  
  - EW: 6.91% cumulative return, Sharpe 0.041  
- **Conclusion:** Combining **factor-inspired data reduction + regularisation + weight constraints** allowed the model to outperform the EW benchmark — both in returns and risk-adjusted performance.  

---

## 🛠 Tech Stack  
- **Languages & Libraries:** Python, scikit-learn, pandas, NumPy, matplotlib  
- **Data Sources:** [Kenneth French Data Library](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html)  
- **Methods:** Regularisation (Lasso, Ridge), portfolio weight constraints, cumulative return and Sharpe ratio evaluation  

---

## 📈 Results Visualization  
- Cumulative return plots (EW vs. Lasso vs. Ridge)  
- Sharpe ratio comparisons with and without weight constraints  
- Impact of factor-inspired asset selection  

---

## 📜 Citation  
If referencing this work, please cite as:  

*Michaïl Maréchal et al. (2023). Machine Learning and Predictive Analytics in Portfolio Optimisation: Applying Regularisation to Beat the Equal-Weighted Benchmark. DBA3803 Predictive Analytics in Business, National University of Singapore (Exchange Semester).*  

