# COVID-19 ANALYSIS - POWER BI
![image](https://github.com/user-attachments/assets/1c455b55-9a3e-4faa-9681-2e4a200ae074)

## INTRODUCTION

This project focuses on a detailed analysis of COVID-19 data in India using Power BI.The objective is to uncover meaningful insights from COVID-19 data to support informed decision-making. The dataset includes key indicators such as confirmed cases, recoveries, deaths, and testing rates across various states and time periods.

Using Power BI, we perform data cleaning, transformation, and visualization to:

* Track the spread of the virus over time

* Identify high-risk states and regions

* Monitor trends in cases, recoveries, and fatalities

* Enable data-driven strategies for managing the pandemic

* This analysis helps visualize the impact of the pandemic and supports public health planning through clear, interactive dashboards.


### Tool Used: Power BI

### Dataset:
Latest COVID-19 India Status dataset - Kaggle

Columns in the dataset:

State/UTs,
Total Cases,
Active,
Discharged,
Deaths,
Population,
Active Cases,
Discharge Ratio,
Death Ratio.

## Data Cleaning
Preprocessing the dataset by handling missing values, duplicates, and ensuring consistency in data formats.

Steps Taken in Power Query Editor:

* Removed duplicates and irrelevant columns.
* Standardized data types (dates, numbers, text).
* Created new columns for Active Cases and Mortality/Recovery Rate

## DAX Calculations

Creating meaningful calculated columns and measures using Data Analysis Expressions (DAX) to derive key insights.

* Total Deaths = SUM('Latest Covid-19 India Status'[Deaths])
* Total Covid Cases = SUM('Latest Covid-19 India Status'[Total Cases])
* Total Recoveries = SUM('Latest Covid-19 India Status'[Recovered])
* Total Active Cases = [Total Cases] - [Total Deaths] - [Total Recoveries]
* Mortality Rate (%) = DIVIDE([Total Deaths], [Total Cases], 0) * 100
* Recovery Rate (%) = DIVIDE([Total Recoveries], [Total Cases], 0) * 100
* State Rank by Cases = RANKX(ALL('Latest Covid-19 India Status'[State]), [Total Cases], , DESC, Dense)

## INSIGHTS

*	Highest COVID-19 Cases: Certain states, such as Maharashtra and Kerala, have consistently reported the highest number of cases.
* Peak Infection Periods: Analysis of the timeline shows that infection spikes occurred during specific months, aligning with major events or relaxations in restrictions.
* Mortality & Recovery Trends: States with high mortality rates often had lower healthcare infrastructure or delayed interventions.
* State-wise Analysis: Some states exhibited unusual trends, requiring further investigation into their containment strategies and testing rates.

## CONCLUSION

* Identified key trends and high-risk regions using COVID-19 data in India

* Recommended improving healthcare infrastructure in severely affected states

* Suggested targeted containment strategies based on active case ratios

* Emphasized the importance of real-time data tracking for rapid response

* Advocated for better resource allocation to maximize healthcare impact
##
