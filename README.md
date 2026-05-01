# Forbes Billionaires Data Analysis

## Project Overview

This project analyzes the **Forbes Billionaires** dataset using Python and pandas. The main goal is to explore wealth distribution, country-wise trends, age patterns, industries, and top billionaires through data cleaning and visualization.

## Dataset Description

- **File**: `forbes_richman.csv`
- **Rows**: 2632 (after cleaning: 2509)
- **Columns**: Rank, Name, Net Worth, Age, Country, Source, Industry

**Key Features**:
- Net Worth is stored as string (`$219 B`)
- Contains European characters (loaded with `encoding="latin1"`)
- Some rows contain missing and null values

## Data Cleaning Steps

- Renamed columns to lowercase with underscores
- Converted `net_worth` from string (`$219 B`) to numeric using `pd.to_numeric()` and regex
- Dropped completely empty rows (`dropna(how='all')`)
- Handled missing values (especially in `age` column — 3.15% missing)

## Analysis & Visualizations

### Country Analysis
- Number of billionaires by country (top countries: USA, China, India, Germany)
- Total net worth by country
- Top 5 billionaires from USA, India, and China with pie charts

### Age Analysis
- Age distribution of billionaires (Histogram with KDE)
- Youngest billionaire: **Kevin David Lehmann** (19 years, Germany)
- Oldest billionaire: **George Joseph** (100 years, USA)
- Age group analysis using `pd.cut()`

### Industry Analysis
- Number of billionaires by industry
- Total net worth by industry (Finance & Investments vs Technology)

### Word Cloud
- Word cloud generated from the `Source` column to show common sources of wealth

### Individual Country Insights
- Created a reusable function `country_pie_chart(country_name)` to show wealth distribution of top 5 billionaires + "Others"

## Key Insights
- United States has the highest number of billionaires and highest total wealth
- Technology and Finance & Investments dominate billionaire industries
- Significant difference between count of billionaires vs total wealth in countries
- Youngest and oldest billionaires identified

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- WordCloud

**Project Purpose**:  
Practice of data cleaning, exploratory data analysis (EDA), visualization, and handling real-world messy data.

Made for learning and revision.
