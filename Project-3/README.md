# Introduction to Financial Engineering - Capital Asset Pricing Model

## Project Overview
The project aims to optimize portfolios using Capital Asset Pricing Model (CAPM) framework. It involves selecting a risk-free asset, such as a government bond, to establish its current yield, and choosing 10 risky assets from the market for analysis. Expected returns for the risky assets are computed using the CAPM formula, followed by the calculation of the Capital Market Line (CML) equation to plot the efficient frontier and CML. The tangency point on the efficient frontier represents the optimal portfolio allocation balancing risk and return. Individual Security Market Lines (SMLs) are computed for three selected assets, and relevant performance measures such as the Sharpe Ratio are used to evaluate portfolio performance. Additionally, the project compares portfolios constructed using Markowitz and CAPM approaches to gain insights into their respective strengths and weaknesses for informed investment decision-making.

## Directory Structure

| File/Folder                   | Description                                     |
| ------------------------------ | ----------------------------------------------- |
| CapitalAssetPricingModel.ipynb | Jupyter Notebook containing the project code and analysis. |
| Presentation_CapitalAssetPricingModel.pdf | PDF file containing the project presentation.  |
| risky_assets.csv | CSV file containing the closing price data for the selected risky assets. |
| market_data.csv | CSV file containing the closing price data for the market. |

## Risky Asset Selection
Closing price data over the past 3 months for the following 10 selected risky assets was obtained from Yahoo Finance:
- Microsoft Corporation (MSFT)
- JPMorgan Chase & Co. (JPM)
- Walmart Inc. (WMT)
- Salesforce, Inc. (CRM)
- McDonald's Corporation (MCD)
- Amazon.com, Inc. (AMZN)
- NVIDIA Corporation (NVDA)
- Caterpillar Inc. (CAT)
- The Coca-Cola Company (KO)
- Alphabet Inc. (GOOGL)

## Risk-Free Asset Selection
- Indian Railway Finance Corporation Ltd (Bond)
- Current Yield: 4.24%

## Capital Asset Pricing Model (CAPM)
CAPM calculates the expected rate of return for an asset or investment using the expected return on the market, a risk-free asset, and the asset's sensitivity to the market (beta).

### Market Data
- Nifty Bank (^NSEBANK)
- Market Return: Calculated using the percentage change between consecutive data points in the market data.

### CAPM Formula
μi = μrf + βi(μm - μrf)
- βi: Beta of investment
- μi: Expected return of investment
- μrf: Risk-free rate
- μm: Expected return of market

### CAPM Expected Returns (Risky Assets)
- Microsoft: 0.027500
- JPMorgan: 0.056402
- Walmart: 0.036176
- Salesforce: 0.024740
- McDonald's: 0.029928
- Amazon: 0.029128
- NVIDIA: 0.027721
- Caterpillar: 0.057252
- CocaCola: 0.038329
- Google: 0.005993

### Capital Market Line (CML)
The CML represents the optimal portfolio of risky assets. It touches the efficient frontier at the tangency point, indicating the highest Sharpe ratio.

### Security Market Line (SML)
The SML is a graphical representation of CAPM, helping to determine if an investment offers a favorable expected return compared to its risk.

## Markowitz Portfolio Optimization
Efficient Frontier and Capital Market Line were utilized for optimal portfolio construction.

## Comparing MPO and CAPM
Risk for the same desired return was compared between Markowitz Portfolio Optimization and Capital Asset Pricing Model.

## References
- [Capital Asset Pricing Model (CAPM)](https://www.investopedia.com/terms/c/capm.asp)
- [Capital Market Line](https://www.wallstreetmojo.com/capital-market-line/)
- [Security Market Line](https://www.investopedia.com/terms/s/sml.asp)
- [Sharpe ratio](https://www.investopedia.com/terms/s/sharperatio.asp)
- [MPO, CAPM Relationship](https://fastercapital.com/content/CAPM-and-Markowitz-Efficient-Set--Unveiling-the-Relationship.html)
- [Python Optimization Library](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.minimize.html)

## Authors
- [Akriti Gupta](mailto:gupta.97@iitj.ac.in)
- [Rishav Aich](mailto:aich.1@iitj.ac.in)
- [Sagnik Goswami](mailto:goswami.5@iitj.ac.in)
- [Tanish Pagaria](mailto:pagaria.2@iitj.ac.in)

(IIT Jodhpur Undergraduates - B.Tech. in Artificial Intelligence & Data Science)