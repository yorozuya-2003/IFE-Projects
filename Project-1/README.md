# Introduction to Financial Engineering - Technical Analysis

## Project Overview
The project focuses on implementing technical analysis in financial engineering. The primary task involves selecting an asset (e.g., stock, bond, ETF), gathering its closing prices over the past 3 years, and calculating four or more technical indicators. The goal is to create a combined indicator using weighted averages based on correlation analysis, enabling the prediction of bullish and bearish positions with the highest accuracy.

## Directory Structure

| File/Folder                   | Description                                     |
| ------------------------------ | ----------------------------------------------- |
| TechnicalAnalysis.ipynb | Jupyter Notebook containing the project code and analysis. |
| Predictions_TechnicalAnalysis.csv | CSV file containing the predicted bullish and bearish positions. |
| Report_TechnicalAnalysis.pdf   | PDF file containing the project report.          |
| Presentation_TechnicalAnalysis.pdf | PDF file containing the project presentation.  |
| GOOGL.csv | CSV file containing the Alphabet Inc Class A (GOOGL) stock data. |

## Asset Selection
The chosen asset for the project is Alphabet Inc Class A (GOOGL) stock data. The closing price dataset over the last three years was obtained from Yahoo Finance.

## Technical Indicators
Three general types of indicators were incorporated to cover various dimensions of the price trend:
- Trend Indicators: Moving Average (MA), Exponential Moving Average (EMA), Moving Average Convergence Divergence (MACD)
- Momentum Indicators: Relative Strength Index (RSI), Stochastic RSI, Kaufman’s Adaptive Moving Average (KAMA), True Strength Index (TSI), Rate of Change (ROC)
- Volatility Indicators: Bollinger Bands

## Correlation Analysis
A correlation matrix heatmap was plotted to identify relationships among indicators and their correlation with the closing price. Highly correlated features were eliminated to simplify the problem.

| Indicator          | Correlation with "Closing Price" |
| ------------------- | --------------------------------- |
| Bollinger Bands     | 0.991184                          |
| EMA                 | 0.974320                          |
| KAMA                | 0.965830                          |
| MA_200              | 0.498118                          |
| RSI                 | 0.217430                          |
| MACD                | 0.194318                          |
| Stochastic RSI      | 0.192073                          |
| TSI                 | 0.189873                          |
| ROC                 | 0.125787                          |


## Correlation Analysis Observations
### High Correlation:
Indicators showing high (> 0.95) correlation with each other:
- KAMA, EMA & Bollinger Bands
- MACD and TSI

### Low Correlation with "Closing Price":
Indicators showing very low correlation with the "closing price":
- TSI
- Stochastic RSI
- ROC

### Based on the Observations:
#### Elimination of Highly Correlated Indicators:
Highly correlated indicators were eliminated: KAMA, EMA, and TSI

#### Elimination of Features with Very Low Correlation with "Closing Price":
Features with very low correlation with "Closing Price" were eliminated: Stochastic RSI and ROC

### Remaining Indicators
(for constructing "Combined Indicator")
- Moving Average (MA)
- Moving Average Convergence Divergence (MACD)
- Relative Strength Index (RSI)
- Bollinger Bands


### The "Combined" Indicator
Weights were assigned to the remaining indicators based on their normalized correlation values with the closing price.

| Indicator            | Weight |
| -------------------- | ------ |
| Bollinger Bands      | 0.52   |
| MA_200               | 0.26   |
| RSI                  | 0.11   |
| MACD                 | 0.10   |


### Normalization Rules for Indicators' Resultant Values:
#### Bollinger Bands

| Condition                           | Predicted Position  |
| ----------------------------------- | ------------------- |
| Upper BB < Closing Price             | Bearish             |
| Middle BB < Closing Price < Upper BB | Bullish             |
| Lower BB < Closing Price < Middle BB | Bearish             |
| Closing Price < Lower BB             | Bullish             |

#### Relative Strength Index (RSI)

| Condition | Predicted Position  |
| --------- | ------------------- |
| RSI < 50   | Bearish             |
| RSI > 50   | Bullish             |

#### Moving Average (Window Length: 200 days)

| Condition         | Predicted Position  |
| ----------------- | ------------------- |
| MA < Closing Price | Bearish             |
| MA > Closing Price | Bullish             |

#### Moving Average Convergence Divergence (MACD)

| Condition               | Predicted Position  |
| ----------------------- | ------------------- |
| MACD < MACD Signal      | Bearish             |
| MACD > MACD Signal      | Bullish             |

### Resultant Values for Predicted Positions:

| Predicted Position | Indicator Resultant Value |
| ------------------- | -------------------------- |
| Bullish             | +1                         |
| Bearish             | -1                         |

### Weightage to Bullish or Bearish Positions:

Based on the above normalization, weightage was added to bullish or bearish positions according to the predictions of each indicator and their corresponding weights. The position with the dominant resultant weightage was returned as the predicted position for each timestamp.


## Literature Review
A comprehensive literature review supports the efficacy of combining indicators such as RSI with Bollinger Bands, using Moving Average and Bollinger Bands together, and the significance of momentum and trend indicators in predicting market movements.

## Prediction Accuracy
The combined indicator demonstrated an accuracy of 75.31% in predicting bullish and bearish positions.

## Further Improvements
To enhance predictive accuracy, future iterations could explore additional indicators such as volume, low, and high. The current project focused solely on the closing price data of the asset.

## References
- [Alphabet Inc Class A (GOOGL) Stock Data Trend](https://in.investing.com/equities/google-inc)
- [Technical Indicators Types](https://www.visualcapitalist.com/12-types-technical-indicators-stocks/)
- [Correlation Analysis in Technical Indicators](https://www.investopedia.com/ask/answers/051315/how-can-i-use-correlation-coefficient-predict-returns-stock-market.asp)
- [Python Library for Technical Analysis](https://technical-analysis-library-in-python.readthedocs.io/en/latest/)


## Authors
- [Akriti Gupta](mailto:gupta.97@iitj.ac.in) (B.Tech. Artificial Intelligence & Data Science)
- [Rishav Aich](mailto:aich.1@iitj.ac.in) (B.Tech. Artificial Intelligence & Data Science)  
- [Sagnik Goswami](mailto:goswami.5@iitj.ac.in) (B.Tech. Artificial Intelligence & Data Science)  
- [Tanish Pagaria](mailto:pagaria.2@iitj.ac.in) (B.Tech. Artificial Intelligence & Data Science)

(IIT Jodhpur Undergraduates)