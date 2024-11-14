# NVIDIA Financial Analysis & Valuation Project 📈

This project provides a comprehensive financial analysis of **NVIDIA (NVDA)**, utilizing advanced valuation techniques, risk analysis, and data visualization. The goal was to estimate the intrinsic value of NVIDIA's stock and assess its risk profile based on historical data and projected financials.

## Project Overview
The analysis focuses on three main areas:
1. **Discounted Cash Flow (DCF) Valuation**: Estimating the intrinsic value per share using Free Cash Flow projections and a Terminal Growth Rate.
2. **Sensitivity Analysis**: Assessing how changes in key assumptions (e.g., WACC, Terminal Growth Rate) affect the valuation outcome.
3. **Risk Analysis (Value at Risk)**: Evaluating the potential downside risk of NVIDIA's stock returns based on historical data.

## Table of Contents
- [Installation](#installation)
- [Data Sources](#data-sources)
- [Analysis Steps](#analysis-steps)
- [Key Results](#key-results)
- [File Descriptions](#file-descriptions)
- [Conclusion](#conclusion)
- [License](#license)

## Installation
To run the analysis locally, ensure you have Python installed along with the necessary libraries.

## Data Sources
The data used for this analysis was extracted from Yahoo Finance using Selenium for web scraping:

- Income Statement: nvidia_income_statement.csv
- Cash Flow Statement: nvidia_cash_flow.csv
- Valuation Metrics: nvidia_valuation_measures.csv
- Historical Stock Data: nvidia_historical_data.csv
- Valuation Measures: nvidia_valuation_measures.csv
- Trading Information: nvidia_trading_information

Analysis Steps

1. Discounted Cash Flow (DCF) Valuation
- Data Cleaning: Extracted and cleaned Free Cash Flow data from the Cash Flow Statement.
- Growth Calculation: Calculated the Compound Annual Growth Rate (CAGR) to project future Free Cash Flows.
- Terminal Value: Estimated the Terminal Value using a conservative growth rate.
- Discounting: Discounted projected Free Cash Flows and Terminal Value using the Weighted Average Cost of Capital (WACC) of 13.63%.
- Intrinsic Value: Derived the intrinsic value per share based on the Enterprise Value.

2. Sensitivity Analysis
- Variables Tested: Explored a range of WACC values (11.5% to 15.5%) and Terminal Growth Rates (1% to 3%).
- Impact on Valuation: The analysis highlighted how changes in these key assumptions affect the estimated intrinsic value.
- Data Presentation: Results were restructured into a DataFrame for clarity and saved for further review.

3. Risk Analysis (Value at Risk)
- Daily Returns Calculation: Analyzed daily returns from historical stock data.
- VaR Calculation: Assessed the Value at Risk at both 95% and 99% confidence levels:
- 95% VaR: -2.79%, indicating the maximum expected loss on 95% of trading days.
- 99% VaR: -4.53%, highlighting the potential for larger losses during extreme market conditions.
- Visualization: Plotted a histogram of daily returns, including VaR thresholds, to visualize the risk distribution.

## Key Results
- DCF Valuation: The intrinsic value per share indicates a potential mismatch with the current market price, suggesting either undervaluation or overvaluation based on different growth scenarios.
- Sensitivity Analysis: Demonstrated significant sensitivity to changes in WACC and Terminal Growth Rate, emphasizing the importance of these assumptions in the valuation process.
- Risk Analysis: The Value at Risk analysis revealed moderate to high volatility, with potential for significant losses on rare occasions.

## File Descriptions
FinModel.ipynb: Jupyter Notebook containing the full analysis and Python code.
DCF_valuation_results.csv: Output file with DCF valuation results.
sensitivity_analysis.csv: Results of the sensitivity analysis.
risk_analysis_metrics.csv: Summary of the risk analysis metrics.

## Conclusion
This project provides a detailed and balanced evaluation of NVIDIA’s financial standing and risk profile:

- The DCF valuation highlighted potential value discrepancies based on market conditions and growth assumptions.
- The sensitivity analysis underscored the impact of key financial assumptions like WACC and Terminal Growth Rate, showcasing a range of possible intrinsic values.
- The risk assessment provided a comprehensive view of the potential downside risks, with significant volatility and possible losses during adverse market conditions.
- These insights can be valuable for investors and analysts looking to make informed decisions regarding NVIDIA’s stock, using data-driven techniques for valuation and risk management.

## Acknowledgments
Data was sourced from Yahoo Finance using web scraping techniques.
Special thanks to the Python community for the use of powerful libraries like pandas, numpy, matplotlib, scipy, and scikit-learn.
This project was made possible through tools like Tableau for data visualization and Jupyter Notebook for a streamlined analysis process.


### How to Use:
- Save this **README.md** file in the root directory of your GitHub repository.
- Customize any specific sections or add additional details if necessary.

This README provides a comprehensive and professional overview of your project, highlighting the key aspects of your analysis and results. Let me know if you need any changes or further assistance!
