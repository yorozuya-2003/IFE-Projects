# Introduction to Financial Engineering - Markowitz Portfolio Optimization

## Project Overview
The project aims to optimize portfolios comprising 10 selected risky assets by applying Markowitz's mean-variance optimization. The process involves choosing assets, collecting closing prices over the past 3 months, calculating returns, and constructing the efficient frontier. Two points on the efficient frontier, representing varying risk tolerance levels, are selected. For each point, the corresponding weights for assets are determined to construct portfolios maximizing expected return for given risk levels. The deliverables include optimized portfolios and insights into risk-return trade-offs. The methodology and prediction accuracy are reported, showcasing the effectiveness of the mean-variance optimization approach.

## Directory Structure

| File/Folder                   | Description                                     |
| ------------------------------ | ----------------------------------------------- |
| MarkowitzPortfolioOptimization.ipynb | Jupyter Notebook containing the project code and analysis. |
| Report_MarkowitzPortfolioOptimization.pdf   | PDF file containing the project report.          |
| Presentation_MarkowitzPortfolioOptimization.pdf | PDF file containing the project presentation.  |
| assets.csv | CSV file containing the closing price data for the selected assets. |

## Asset Selection
The closing price data (over the past 3 months) of 10 selected risky assets was taken from Yahoo Finance, as listed below:

- Apple Inc. (AAPL)
- Alphabet Inc. (GOOGL)
- Microsoft Corporation (MSFT)
- Amazon.com, Inc. (AMZN)
- Tesla, Inc. (TSLA)
- Meta Platforms, Inc. (META)
- NVIDIA Corporation (NVDA)
- PayPal Holdings, Inc. (PYPL)
- Netflix, Inc. (NFLX)
- Visa Inc. (V)

## Return & Risk Measure Calculation
The percentage returns were calculated for each asset for each date by calculating the percentage change in the values through a series. Risk for each asset was calculated using the standard deviation of percentage returns for each asset.

## Markowitz Mean-Variance Optimization
The Markowitz Mean-Variance Optimization Model is a mathematical framework introduced by Harry Markowitz in 1952. It aims to minimize portfolio risk while achieving a target return. The optimization problem was formulated and solved using the CYXPY Python library. Efficient Frontier plots were generated to illustrate the optimal combinations of investments for the highest return at the lowest risk. Two points on the efficient frontier representing different risk tolerance levels were selected, and corresponding weights for assets were determined to construct portfolios.

## Trade-off Between Risk & Return (in Portfolio Choices)
The risk-return tradeoff principle states that potential return rises with an increase in risk. Calculations were performed for various risk metrics including Alpha Ratio, Beta Ratio, and Sharpe Ratio. Balancing risk and return is essential for constructing a portfolio aligned with an investor's objectives and risk tolerance.

## Limitations of Markowitz Optimization
Several limitations of the Markowitz Optimization were discussed, including the assumption of normal distribution, static inputs, estimation error, and single-period framework. Mitigation strategies were proposed to address these limitations.

## Markowitz Optimization Real-world Applications
The real-world applications of Markowitz Optimization were explored, including portfolio construction, risk management, use in ETFs, and the concept of the efficient frontier.

## Additional Work
Additional features such as calculating the global minimum risk for a desired return value and allowing short-selling were implemented. Corresponding weight values for these scenarios were calculated and visualized.

## References
- [Markowitz Model](https://en.wikipedia.org/wiki/Markowitz_model)
- [Markowitz Model of Selection](https://www.wallstreetmojo.com/markowitz-model/)
- [Markowitz Mean-Variance Portfolio Theory](https://docs.mosek.com/portfolio-cookbook/markowitz.html)
- [Modern Portfolio Theory](https://www.investopedia.com/terms/m/modernportfoliotheory.asp)
- [Practical Limitations of Modern Portfolio Theory](https://www.linkedin.com/pulse/practical-limitations-modern-portfolio-theory-samer-obeidat-mgm/)
- [Short Selling](https://www.investopedia.com/terms/s/shortselling.asp)
- [Risk-Return Trade-off](https://www.investopedia.com/terms/r/riskreturntradeoff.asp)
- [Python Library for Convex Optimization Problems](https://www.cvxpy.org/examples/basic/quadratic_program.html)

## Authors
- [Akriti Gupta](mailto:gupta.97@iitj.ac.in)
- [Rishav Aich](mailto:aich.1@iitj.ac.in)
- [Sagnik Goswami](mailto:goswami.5@iitj.ac.in)
- [Tanish Pagaria](mailto:pagaria.2@iitj.ac.in)

(IIT Jodhpur Undergraduates - B.Tech. in Artificial Intelligence & Data Science)