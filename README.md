# 📊 Bankruptcy Risk Factor Analysis (Taiwan Economic Journal)

This project identifies the primary factors influencing bankruptcy risk by applying the **Altman Z-Score** model to a dataset of 6,819 listed companies from the Taiwan Economic Journal (1999–2009).

---

## 📌 Project Overview

The objective of this analysis is to determine key predictors of insolvency based on financial indicators. 

- **Dataset Size:** 6,819 companies.
- **Features:** 95 distinct financial ratios per observation.
- **Goal:** Identifying the statistical differences between solvent and insolvent firms.

---

- ## 📂 Data Source

The dataset used in this project is sourced from **Kaggle**:
- **Dataset:** [Bankruptcy Prevention](https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction) (based on the Taiwan Economic Journal).
- **Timeframe:** 1999 to 2009.

---

## 🛠️ Tech Stack

The following libraries were used for data processing, statistical analysis, and visualization:

- **Pandas & NumPy:** For data manipulation and mapping the 95 financial ratios.
- **Matplotlib & Seaborn:** For exploratory data analysis and visual comparisons.
- **Random:** To implement stochastic sampling for balancing the dataset.

---

## 📈 Methodology: The Altman Z-Score

To evaluate financial stability, the analysis maps the dataset features to the five key ratios of the **Altman Z-Score** formula:

$$Z = 1.2X_1 + 1.4X_2 + 3.3X_3 + 0.6X_4 + 1.0X_5$$

| Ratio | Financial Metric | Description |
| :--- | :--- | :--- |
| **X1** | Liquidity | Working Capital / Total Assets |
| **X2** | Profitability | Retained Earnings / Total Assets |
| **X3** | Operating Efficiency | EBIT / Total Assets |
| **X4** | Solvency | Equity / Total Liabilities |
| **X5** | Sales Efficiency | Total Asset Turnover |

---

## 🔄 Workflow & Sampling Strategies

Since the dataset is highly imbalanced, the project features an interactive sampling mechanism to ensure a fair comparison between groups.

### 1. Sampling Options 🎲
The user can choose between two strategies to select the comparison group of solvent companies:
- **[R] Random Sampling:** A purely stochastic selection of healthy firms.
- **[S] Stratified / Rule-Based Selection:** Filters for "top-performing" companies (based on above-average growth and liquidity) to create a "gold standard" comparison group.

### 2. Exploratory Data Analysis (EDA) 🔍
- **Boxplots:** Used to visualize distributions and detect outliers across the 95 ratios.
- **Trend Analysis:** Investigating the **Total Asset Growth Rate (TAGR)** to observe financial trajectories before insolvency.
- **Mean Comparison:** Analyzing the statistical gap between solvent and insolvent entities.

---

## 🚀 How to Use

### 1. Clone the repository
git clone https://github.com/DEIN-NUTZERNAME/bankruptcy-risk-prediction.git

### 2. Install dependencies
pip install pandas matplotlib seaborn numpy

### 3. Run the Notebook

Open the `company-analysis-for-lending-z-score-formula.ipynb` file in Jupyter Notebook or VS Code and follow the interactive prompts to choose your sampling strategy (`R` or `S`).

## 🎓 About this Project
This project was developed as the final capstone project for the certification course "Business Data Analyst" at the IHK (Industrie- und Handelskammer) in collaboration with the Business Data Professional Community.

It demonstrates the application of statistical methods and financial theory to real-world economic data to solve business-critical problems.

## 📄 License
This project is licensed under the MIT License. See the LICENSE file for more details.
