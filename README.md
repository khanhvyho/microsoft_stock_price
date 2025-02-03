# Microsoft Stock Time Series Model Project

This repository contains my attempt to answer if weekly Mean Volume and weekly Past Net Price affect weekly Current Net Price Microsoft stock (from 2015/04/01 to 2021/03/31).
My initial hypothesis is Past volume is positively associated with Current Net Price while Past Net Price is negatively associated with Current Net Price.

## Project Structure

A complete code reprort attempt is available at `./code/report.Rmd`.

## Data

The raw dataset used for the analysis is available at `./data/Microsoft_Stock.csv`. It was downloaded from [Kaggle](https://www.kaggle.com/datasets/vijayvvenkitesh/microsoft-stock-time-series-analysis?resource=download).

- microsoftdata has 1511 observations of 6 variables. These variables include Date, Open, High, Low, Close, and Volume.

- weekly_microsoft_data is the dataset we will use to analyze. The original dataset provides daily data, which gives non-stationary results. 
We convert into weekly data for stationary. This dataset has 314 observations of 4 variables. These variables include Week (week), Date (date), Net Price (net_price), and Mean Volume (mean_volume).

## Result

- Past trading volume is not significantly associated with current net price.

- Past net price is significantly negatively associated with current net price.

- Current net price can be predicted using the past 5 weeks net price.