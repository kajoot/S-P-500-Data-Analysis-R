# 5-Year Stock Analysis of Selected Companies (AAL, AMZN, NFLX, MGM, MSFT)

## Project Overview

This project analyzes **daily stock prices and trading volumes** of five major companies over a **5-year period (2013–2018)**.  
The goal is to explore:

- Stock **price trends** over time
- **Volatility** and risk patterns
- **Trading activity** via volume analysis
- **Comparative performance** across companies

The analysis focuses on **American Airlines (AAL)** as a case study before expanding to multiple companies to understand broader market dynamics.

**Presentation Link:**  
[View Project Presentation on Canva](https://www.canva.com/design/DAG9v02Xr-U/MGMCjFHIHA7sLyvSjnLgFA/edit?utm_content=DAG9v02Xr-U&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

---

## Dataset

- **Source:** `all_stocks_5yr.csv`
- **Columns:** `Name`, `date`, `open`, `high`, `low`, `close`, `volume`
- **Companies analyzed:**  
  - **AAL (American Airlines)**  
  - **AMZN (Amazon)**  
  - **NFLX (Netflix)**  
  - **MGM**  
  - **MSFT (Microsoft)**

---

## Tools & Libraries

- **Language:** R
- **Packages:** `tidyverse`, `ggplot2`, `lubridate`, `scales`
- **Key functions used:**  
  `read.csv`, `filter`, `select`, `group_by`, `summarise`, `ggplot`, `geom_line`, `geom_segment`, `geom_boxplot`, `coord_polar`

---

## Analysis Workflow

1. **Data Cleaning & Preparation**
   - Converted `date` column to Date type for time-series analysis
   - Filtered AAL data for detailed study
   - Extracted `Year` and `Month` for monthly/yearly aggregation

2. **Descriptive Statistics**
   - Calculated min, max, quartiles, median, mean, range, SD, and IQR for stock prices and volume
   - Summarized daily trading volume for each company

3. **Visualization**
   - **High-Low price plot:** Full 5-year range to assess volatility
   - **Zoomed plots (2017–2018 & Jan 2018):** Daily price trends for detailed analysis
   - **Yearly volume line chart:** Total volume per year per company
   - **Pie chart:** Market share by total 5-year trading volume
   - **Boxplots:** Daily and monthly volume distributions to detect variability and outliers

4. **Multi-Company Comparison**
   - Aggregated trading volumes across companies
   - Compared trends, volatility, and volume outliers

---

## Key Insights

- **AAL Stock Trends:** Moderate volatility with specific high-volume periods
- **Volume Analysis:**  
  - Microsoft & Amazon dominate trading volume  
  - Smaller companies like MGM show higher outlier frequency, indicating riskier trading behavior
- **Monthly Patterns:** Certain months show unusually high trading, often linked to company news or sector events
- **Investor Takeaways:**  
  - High-volume companies → safer, liquid investments  
  - Outlier days/months → opportunities for short-term trading

---

## Business Context

- **Stock rises in January 2018 for AAL:**  
  Driven by strong earnings, revenue growth, and share buybacks
- **Stock fall later in January 2018:**  
  Caused by rising fuel costs, higher operating expenses, and tempered guidance affecting investor confidence
- **Market lesson:**  
  Even if earnings are positive, rising costs or weaker future guidance can cause stock declines

---

## Technical Notes

- **Time-series analysis:** Using `geom_line` and `geom_segment` to visualize trends and daily ranges
- **Volume distribution:** Boxplots identify typical and outlier trading volumes
- **Aggregation:** `group_by` and `summarise` used for yearly and monthly summaries
- **Visualization insights:** Colors and shapes differentiate open, close, high, low, and company-specific data

---

