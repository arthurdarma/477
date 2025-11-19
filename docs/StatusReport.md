# Interim Status Report
## Project Overview
Our project aims to analyze long term affordability trends by comparing median household income with median home prices over the last four decades. The goal is to determine whether wages have kept pace with the rising cost of housing, and whether affordability has worsened over time. This topic has become increasingly important, especially in the wake of housing price surges during and after the COVID-19 pandemic, along with slower wage growth that many households continue to experience. Housing affordability affects financial stability, generational wealth, and economic mobility, making this a timely and socially relevant area of study.

Since submitting our initial Project Plan, we have refined our dataset selections, confirmed our primary analysis approach, and begun reviewing and organizing our collected data. Our focus has shifted toward comparing nominal (non inflation adjusted) median home prices and nominal median household incomes, which more accurately reflect real world experiences of buyers and earners in each respective year. Providing a direct, intuitive basis for analyzing how difficult it is for the average American household to afford a home based on actual reported income and actual home sale prices.

## Task Update
We have successfully collected all three datasets from the Federal Reserve Economic Data we plan to use for this project. These include:

1. Median Sales Price of Houses Sold in the United States (MSPUS) – This dataset provides real, dollar value median home sale prices for each year and serves as our primary housing cost dataset.

2. Median Household Income in the United States (MEHOINUSA646N) – This dataset provides nominal household income values and serves as our primary income dataset, allowing direct comparison with MSPUS.

3. All-Transactions House Price Index (USSTHPI) – This dataset provides an indexed representation of housing market growth over time and is being used as a supporting reference series to provide additional context.

All three datasets were downloaded in CSV format and stored in the /data/raw folder of our GitHub repository. The datasets are now ready for cleaning and integration.

## Storage and Organization
Our repository follows a structured folder layout consistent with our Project Plan:

* /data/raw – Contains the original downloaded MSPUS, MEHOINUSA646N, and USSTHPI datasets.
* /data/processed – Will store cleaned and merged datasets once integration is complete.
* /notebooks – Contains initial exploratory analysis work.
* /docs – Contains documentation files, including ProjectPlan.md and StatusReport.md.

## Data Integration

We have begun the initial stages of data integration. The MSPUS and MEHOINUSA646N datasets both report data annually, which makes merging by year straightforward. USSTHPI is reported quarterly, so we plan to compute annual averages for consistency, although this dataset will be used only as a supporting trend reference. Integration work is currently in progress in a Jupyter notebook.

Our main focus remains on nominal dollar comparisons, so no inflation adjustments or re indexing are required before merging MSPUS with MEHOINUSA646N. Once the merge is complete, we will verify whether there are any missing years or overlapping values that require attention.

## Analysis

Analysis remains in progress. We have started exploring the datasets in a Jupyter notebook, performing basic data loading. However, full analysis including affordability ratio calculation, trend comparisons, and statistical interpretation has not yet been completed.

Our planned analyses include:

* A line chart comparing MSPUS and MEHOINUSA646N across the study period.
* A computed “affordability ratio,” defined as:
Affordability = MSPUS / Median Household Income
* A secondary supporting graph using USSTHPI to show indexed housing price trends.
* Summary statistics to capture decade by decade changes.

These steps will be completed after the integration and cleaning phases are finalized.

## Documentation and Provenance

All work has been documented within the GitHub repository. Updates to dataset descriptions, project plans, and file structure have been recorded using Markdown files in the /docs folder. Git commit logs provide a transparent view of contributions from both team members. Tags such as project-plan and project-plan-v2 have been created to mark milestone submissions. We will create a similar status-report tag for this milestone.

## Updated Timeline and Task Status

Dataset acquisition has been completed, and all datasets have been downloaded and reviewed. The repository setup is also finished, with the folder structure fully established. Data exploration is currently in progress, and we have completed initial checks to understand the structure and content of each dataset. Data integration is also underway, as we are working on merging the nominal datasets by year. Data cleaning is in progress as well, with a focus on ensuring consistency across years and preparing the datasets for analysis. The affordability analysis is planned to begin once the merged dataset is finalized. Final visualizations are also planned, with an expected completion date in early December. The final project submission remains due on mid December 2025.

## Changes to Project Plan

We made several adjustments to the original Project Plan based on improved clarity and relevance:

1. Shift to Nominal Dollar Analysis
We replaced the inflation adjusted income dataset (MEHOINUSA672N) with the nominal dataset (MEHOINUSA646N) to match MSPUS (also nominal) avoiding unnecessary CPI based adjustments and aligns with real world affordability conditions.

2. USSTHPI Re-classified as Supporting Dataset
Instead of using USSTHPI as a main dataset, it is now used only for contextual trend comparison because it is indexed and not directly comparable to nominal dollar income.

3. CPI Dataset Removed
CPI is no longer needed under our nominal dollar approach to reduce complexity and keeps analysis more aligned with our primary research question.

## Team Contributions
Arthur Darma

Arthur has led data acquisition, repository organization, and initial dataset exploration. He downloaded and documented all datasets, set up the folder structure, and began early integration work in Jupyter notebooks. He also contributed to editing the Project Plan updates and preparing this Interim Status Report.

Laura

Laura contributed by helping refine the Project Plan text. She also participated in early data inspection and repository cleanup tasks.

Both team members have committed work through their individual GitHub accounts, ensuring transparent version history.

## References

Federal Reserve Economic Data (FRED). Median Sales Price of Houses Sold in the United States (MSPUS). https://fred.stlouisfed.org/series/MSPUS
Federal Reserve Economic Data (FRED). Median Household Income in the United States (MEHOINUSA646N). https://fred.stlouisfed.org/series/MEHOINUSA646N
Federal Reserve Economic Data (FRED). All-Transactions House Price Index for the United States (USSTHPI). https://fred.stlouisfed.org/series/USSTHPI