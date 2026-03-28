📊 Bankruptcy Risk Factor Analysis (Taiwan Economic Journal)
This project identifies the primary factors influencing bankruptcy risk by applying the Altman Z-Score model to a dataset of 6,819 listed companies. The analysis focuses on financial health indicators and comparative trends between solvent and insolvent firms.

📌 Project Overview
The objective is to analyze financial ratios from the Taiwan Economic Journal (1999–2009) to determine key predictors of insolvency.

Dataset Size: 6,819 companies.
Features: 95 distinct financial ratios per observation.
Methodology: Statistical analysis and downsampling comparison using the Altman Z-Score.
🛠️ Tech Stack
The following tools were used for data processing, statistical analysis, and visualization:

Python 3.x
Pandas & NumPy: Data manipulation and numerical operations.
Matplotlib & Seaborn: Advanced data visualization (Boxplots, Line Charts).
Random: Stochastic sampling for dataset balancing.
📈 Methodology: The Altman Z-Score
To assess financial stability, we map the dataset's features to the five key ratios of the Altman Z-Score formula:

$$Z = 1.2X_1 + 1.4X_2 + 3.3X_3 + 0.6X_4 + 1.0X_5$$

Ratio	Financial Metric	Description
X1	Liquidity	Working Capital / Total Assets
X2	Profitability	Retained Earnings / Total Assets
X3	Operating Efficiency	EBIT / Total Assets
X4	Solvency	Equity / Total Liabilities
X5	Sales Efficiency	Total Asset Turnover
🔄 Workflow & Sampling Strategies
The dataset is highly imbalanced, containing significantly more solvent than insolvent companies. To ensure a fair comparison, the project implements an interactive sampling mechanism:

1. Sampling Options 🎲
Users can choose how to construct the comparison group of solvent companies:

[R] Random Sampling: Selects a random subset of healthy firms.
[S] Stratified / Rule-Based Selection: Filters for "top-performing" solvent companies (above-average TAGR, Liquidity, and Profitability) to compare insolvent firms against a financial "gold standard."
2. Exploratory Data Analysis (EDA) 🔍
Boxplots: Used to visualize the distribution of financial ratios and identify significant outliers in both groups.
Mean Comparison: Statistical comparison of averages between solvent and insolvent firms.
Trend Analysis: Tracking the Total Asset Growth Rate (TAGR) to observe the downward trajectory of firms approaching bankruptcy.
📊 Key Visualizations
The project generates several insights through:

Distribution Plots: Highlighting the "Safe", "Grey", and "Distress" zones of the Z-Score.
Line Charts: Visualizing the divergence in asset growth between company groups over time.
Boxplots: Comparing the variance of the 95 financial indicators.
🚀 How to Use
Clone the repository:
git clone https://github.com/DEIN-NUTZERNAME/bankruptcy-risk-prediction.git
Install dependencies:
pip install pandas matplotlib seaborn numpy
Run the Notebook:
Open the .ipynb file and follow the interactive prompts to choose your sampling strategy (R or S).
📝 Conclusion
By applying the Altman Z-Score and comparing balanced samples, this project demonstrates that specific liquidity and profitability ratios are early warning signs of financial distress. The Total Asset Growth Rate serves as a particularly strong dynamic indicator for identifying companies at risk.

Developed as project of the course Business Data Analyst 09-2025 (IHK / Business Data Professional).

