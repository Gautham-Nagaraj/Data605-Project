# World's Happiest Countries - Data Analysis
## Project Overview

This project investigates the multifaceted factors influencing the World Happiness Index and the global rankings of the happiest countries. Utilizing a combination of socio-economic, climate, and sentiment data, the aim is to uncover key determinants of national well-being beyond traditional economic indicators.

## Motivation
The inspiration for this analysis emerged from a sentiment analysis of a 2018 video, "World’s happiest countries: Explained," which challenged conventional wisdom by suggesting that a country's economy is not always the primary driver of happiness. Instead, the report highlights well-being and even climate as potentially more significant factors, especially given the consistent high rankings of Nordic/European countries. This project seeks to empirically validate and expand upon these observations.

## Analysis Questions
This study seeks to answer the following core questions:
- What are the average climate conditions of countries at the top and bottom of the world's happiest list?
- What is the economic status (GDP) of countries at the top and bottom of the list?
- Which is a more influential factor: a country's total GDP or its GDP per capita, in relation to happiness?
- How have the happiness rankings evolved and changed between 2018 and 2024?
- What impact does healthcare have on the overall quality of life and happiness?

## Data Sources
The project integrates data from several reputable sources:
World Happiness Index (2011-2024):
Source: Gallup World Poll
Description: Primary dataset containing happiness scores, ranks, and various "explained by" factors (Log GDP per capita, Social support, Healthy life expectancy, Freedom, Generosity, Perceptions of corruption).
Climate Data (1901-2023):
Source: World Bank Group (CCKP - Climate Change Knowledge Portal)
Description: Annual average surface air temperatures for various countries.
GDP by Country & GDP Per Capita:
Source: World Bank Group
Description: Datasets detailing Gross Domestic Product (GDP) and GDP per capita for countries across different years.

## Data Preprocessing
Data cleaning and transformation were crucial to prepare the datasets for analysis and were primarily performed using Power BI's Power Query capabilities, complemented by Python scripts for specific checks. Key steps included:
Year Filtering: All datasets were filtered to include data from 2018 onwards (up to 2023 where available), aligning with the sentiment analysis's timeframe.
Missing Value Handling:
Columns with high percentages of missing values (e.g., upperwhisker, lowerwhisker, and detailed "Explained by" columns from the World Happiness Index) were removed.
Countries with missing GDP or climate data that were not central to the analysis were excluded.
Data Unpivoting: Annual columns (e.g., 2018, 2019) in GDP, GDP per capita, and Climate datasets were unpivoted to create unified 'Year' or 'Date' columns, facilitating time-series analysis.
Column Management: Irrelevant columns (e.g., 'Country code', 'Indicator name') were removed, and remaining columns were renamed for consistency (e.g., 'Temperature °C').
Data Type Conversion: Columns were converted to appropriate data types (e.g., numeric, date, factor).
Data Model & Relationships
A robust data model was established by creating relationships between the cleaned datasets. Given that each dataset contains multiple entries per country across different years/dates, Many-to-Many relationships were formed based on the common Country name column across all tables.

Technologies Used
Power BI: For data transformation, cleaning, and relationship modeling.
Python: Used for specific data cleaning steps.
