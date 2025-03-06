# Prophet Challenge - Mercado Libre Analysis

## Overview

In this project, I analyzed the relationship between hourly Google search traffic and Mercado Libre's stock price. Mercado Libre, the leading e-commerce platform in Latin America with over 200 million users, was the subject of this analysis. The goal was to predict search traffic patterns and explore how these patterns might relate to the company's stock price movements.

## Project Steps

### Step 1: Analyzing Unusual Patterns in Hourly Google Search Traffic

I began by slicing the Google search traffic data for the month of May 2020, which was a significant month for Mercado Libre as the company released its quarterly financial results. I visualized the search traffic during this period to identify any unusual patterns or spikes. I calculated the total search traffic for May 2020 and compared it to the median search traffic across all months. This allowed me to assess whether there was an increase in search activity during the financial results release.

### Step 2: Mining the Search Traffic Data for Seasonality

In this step, I explored the hourly search data to identify any seasonal patterns in user interest. I grouped the data by hour, day, and week of the year to understand the following:
- Whether there are certain hours of the day with more search traffic
- Which days of the week have the highest search volume
- Whether there is a noticeable increase in search traffic during specific weeks, such as the winter holidays

These insights could potentially help marketing teams focus their efforts on the most opportune times to maximize ROI.

### Step 3: Relating the Search Traffic to Stock Price Patterns

Next, I analyzed the relationship between the Google search traffic data and Mercado Libre's stock price. I merged the stock price data with the search traffic data into a single DataFrame. I focused on the first half of 2020 (January to June) and compared the trends in both time series, especially in the context of the global financial impact of the pandemic.

I also created additional columns in the dataset:
- **Lagged Search Trends**: This column represented search traffic shifted by one hour.
- **Stock Volatility**: This was calculated using a four-hour exponentially weighted rolling average.
- **Hourly Stock Return**: This column calculated the percent change in stock price on an hourly basis.

By analyzing these columns, I determined whether there was a predictable relationship between lagged search trends and stock volatility or stock returns.

### Step 4: Creating a Time Series Model with Prophet

In the final step, I used the Prophet time series forecasting model to predict future search traffic trends. I preprocessed the data to fit the format required by Prophet and then estimated the model. The model provided forecasts for future search traffic, and I visualized the individual time series components to gain insights into:
- The times of day when search traffic is at its peak
- The day of the week with the highest search traffic
- The lowest point for search traffic over the course of the year

These insights could be valuable for both marketing teams and financial analysts looking to predict trends based on search behavior.

## Tools and Libraries Used

- **Pandas**: For data manipulation and analysis
- **Matplotlib / Seaborn**: For data visualization
- **Prophet**: For time series forecasting
- **Jupyter Notebook / Google Colab**: For coding and running the analysis

## Conclusion

Through this analysis, I was able to identify key patterns in the search traffic data and assess how these patterns might relate to Mercado Libre’s stock performance. The insights from this project could help the company optimize its marketing strategy by targeting peak search times and potentially inform financial decision-making based on the relationship between search interest and stock volatility.
