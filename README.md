# 📊 NSE Nifty 50 — Data Cleaning, Analysis & Visualization using Python

> Analyzed real-world NSE Nifty 50 stock market data using Python — cleaning, EDA, and visualization to identify market trends and top-performing stocks.


## 🎯 Objective

The objective of this project is to analyze real-world NSE Nifty 50 stock market data using Python. The project covers:

- Cleaning and preprocessing raw stock data with Pandas
- Performing exploratory data analysis to identify market sentiment
- Finding top gainers, losers, and long-term performers
- Visualizing price trends, volume, correlations, and returns using Matplotlib and Seaborn
- Drawing meaningful insights from the data to support investment decision-making


## 📁 Project Structure

nifty50-stock-analysis/
│
├── NSE_DATA.csv              # Raw dataset (50 Nifty stocks)
├── NSE_DATA_cleaned.csv      # Cleaned dataset (output)
├── NSE_Analysis.py           # Main Python script
├── README.md                 # Project documentation
│
├── plot1_sentiment_distribution.png
├── plot2_gainers_losers.png
├── plot3_yearly_returns.png
├── plot4_volume_turnover.png
├── plot5_heatmap.png
├── plot6_quadrant_scatter.png
└── plot7_52w_distance.png


## 📊 Dataset Description

The dataset contains a snapshot of all 50 Nifty stocks with the following columns:

| Column | Description |
|---|---|
| Symbol | Stock ticker name |
| Open | Opening price of the day |
| High | Highest price of the day |
| Low | Lowest price of the day |
| LTP | Last traded price |
| Chng | Absolute change in price |
| % Chng | Percentage change today |
| Volume (lacs) | Number of shares traded (in lakhs) |
| Turnover (crs.) | Total trade value (in crores) |
| 52w H | 52-week highest price |
| 52w L | 52-week lowest price |
| 365 d % chng | 1-year percentage return |
| 30 d % chng | 30-day percentage return |


## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas** — data loading, cleaning, and analysis
- **NumPy** — numerical operations
- **Matplotlib** — chart creation
- **Seaborn** — advanced visualizations

## 📂dataset used
https://www.kaggle.com/datasets/rohanrao/nifty50-stock-market-data

## 🧹 Data Cleaning Steps

1. Loaded raw CSV data using Pandas
2. Identified columns with comma-formatted numbers stored as strings
3. Removed commas and converted all price/volume columns to float
4. Handled missing values by filling with column median
5. Removed duplicate stock entries
6. Created new feature columns:
   - `Day_Range` — intraday price swing (High - Low)
   - `52w_Range_pct` — 52-week volatility percentage
   - `Dist_from_52wH` — how far the current price is from the 52-week high
   - `Sentiment` — classified each stock as Bullish, Bearish, or Neutral

## 📈 Analysis Performed

- **Market Sentiment** — counted bullish vs bearish stocks
- **Daily Return Stats** — mean, median, min, max of % change
- **Top 5 Gainers & Losers** — best and worst performers today
- **1-Year Return Rankings** — long-term performance of all 50 stocks
- **Volume & Turnover Analysis** — most actively traded stocks
- **Correlation Analysis** — relationships between key metrics
- **Quadrant Analysis** — 30-day vs 365-day return comparison
  
## 📉 Visualizations

| Plot | Description |
| plot1_sentiment_distribution | Market sentiment pie chart + return distribution |
| plot2_gainers_losers | Top 5 gainers and losers bar chart |
| plot3_yearly_returns | 1-year returns for all 50 stocks |
| plot4_volume_turnover | Volume vs turnover comparison (dual axis) |
| plot5_heatmap | Correlation heatmap of all numeric metrics |
| plot6_quadrant_scatter | 30-day vs 365-day quadrant scatter plot |
| plot7_52w_distance | Distance of each stock from its 52-week high |



## ▶️ How to Run

**1. Clone the repository**

git clone https://github.com/Harsha0402/nifty50-stock-analysis.git
cd nifty50-stock-analysis


**2. Install required libraries**

pip install pandas numpy matplotlib seaborn


**3. Run the script**

python NSE_Analysis.py




