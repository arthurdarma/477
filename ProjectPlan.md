# Project Plan

## Overview
This project will analyze long term economic trends in the United States by 
examining the relationship between housing prices and wages over the last 40 years. Recent years, especially after the COVID-19 pandemic, we have seen housing price surges while wage growth remained moderate. This widening gap has drawn attention concerned with generational wealth and housing accessibility.
Housing affordability is a growing economic concern as many believe that wage growth 
has not kept pace with rising housing costs. By using real historical data, this project will 
evaluate how housing prices and median household income have changed over time and whether 
housing has become more or less affordable for the average American. 

## Research Question
The primary research question guiding this project is: 
**How have housing prices changed compared to wages in the United States over the last 40 years?** 
Additional questions include whether wage growth has kept up with housing price increases, 
whether housing affordability has declined over time, and whether there are specific decades 
or economic periods where gaps between wages and housing prices widened significantly.

## Team
This project will be completed by two team members: Arthur Darma who will serve as the 
Data Acquisition, Data Integration and Analysis Lead, and Laura, who will serve as the 
Documentation Lead. Arthur will be responsible for downloading and managing datasets, 
integrating datasets, performing analysis using Python, and creating visualizations. 
Laura will focus on documenting metadata, and assisting with Markdown documentation. 
Both of us will collaborate on data cleaning, analysis decisions, GitHub commits, and 
reporting.

## Datasets
This project will use three datasets from the Federal Reserve Economic Data (FRED), 
a trusted and authoritative public data source. The first and main dataset is the 
All-Transactions House Price Index for the United States, which tracks 
changes in housing prices over time as an index. This dataset is useful for measuring 
the percentage growth of housing prices over the last five decades. 
The second main dataset is Median Household Income in the United States, 
also from FRED, which provides annual median household income figures in dollars. 
This dataset will allow comparison between wage growth and housing price changes. 
As additional supporting data, the Median Sales Price of Houses Sold in the United States 
(MSPUS) will also be used. Unlike the house price index, this dataset provides real housing 
prices in U.S. dollars, making it useful for interpreting inflation-adjusted affordability 
and providing real-world context to the analysis. All three datasets will be downloaded in 
CSV format.

In addition to these primary datasets, we may include the Consumer Price Index (CPI-U) from FRED to adjust median household income and housing prices for inflation, ensuring all values are comparable in real terms. This will help provide a more accurate picture of affordability over time. To improve interpretability, data will also be standardized by indexing both income and housing prices to a common base year (e.g., 1980 = 100). This allows percentage growth comparisons across decades. Each dataset’s metadata including variable names, frequency, and units will be documented in a shared data dictionary to support transparency and reproducibility.

## Data Lifecycle Approach
This project will follow the data lifecycle model introduced in class. 
Data will first be acquired from FRED through CSV downloads and stored in a 
structured repository. Raw data will be preserved unmodified. Metadata will be documented 
to describe dataset origin, structure, and variables. The datasets will then be integrated 
using Python and the Pandas library by matching on the year variable. Data quality checks 
will be performed to identify any missing years, unit inconsistencies, or unusual values. 
Cleaning procedures will be applied as needed, including handling missing data and adjusting 
income values for inflation to allow meaningful comparisons. The data will then be analyzed 
using descriptive statistics, and visualizations of long-term trends. One potential analysis we are looking to do is to calculate a ‘housing affordability ratio,’ such as median house price divided by median household income, to quantitatively show how affordability changed over time.

## Ethical Data Handling
This project uses publicly available datasets that do not include any personal or 
sensitive information, so privacy risk is minimal. All data sources will be credited to 
meet licensing and reuse requirements. Transparency will be maintained through proper 
citations and by documenting methods clearly. No data manipulation will be performed that 
could misrepresent findings.

## Storage and Organization
Data will be organized using a clear folder structure within the GitHub repository. 
Raw data will be stored in a "data/raw" directory, and cleaned or merged data will be saved 
in a "data/processed" directory. Jupyter notebooks will be stored in a "notebooks" directory
, while documentation including reports will be stored in a "docs" folder. 
This structure will support project clarity and reproducibility.


## Workflow and Reproducibility
The analysis will be conducted using Jupyter notebooks to provide a clear 
and reproducible workflow. Each step of the process, from data loading to final 
visualizations, will be documented. GitHub will be used for version control to track 
changes and ensure provenance. For example, we are looking to include charts comparing inflation-adjusted income and housing prices over time, and maybe highlighting decade-over-decade percentage changes.

## Timeline
Data collection and repository structure setup will be completed by mid to late October. 
Data integration will be completed shortly afterward, followed by cleaning and inflation 
adjustment. The interim project report will be submitted by November 11, 2025. 
The main analysis and visualization work will be done through late November. The final 
report and GitHub release will be completed by December 10, 2025.

## Constraints
- Income values may require inflation adjustment using an additional dataset.  
- The data is not yet standardized by indexing both income and housing prices to a common base year, which may limit direct comparison of growth rates.  
- Regional variations in housing prices and income are also not currently addressed — future work could incorporate state-level or metropolitan data for deeper insight.  
- Major economic shocks (e.g., the 2008 financial crisis and COVID-19) have not yet been isolated, which could affect the interpretation of long-term trends.  
- Project timing and data availability may restrict the use of more advanced analytical methods beyond descriptive statistics.

## Gaps
- A clear decision has not yet been made on how to perform inflation adjustment, though the Consumer Price Index (CPI) from FRED is the most likely approach.  
- The analysis currently focuses on national averages, which may obscure inequality between regions or demographic groups.  
- Further research could explore whether affordability trends differ across age cohorts, income brackets, or housing types to provide a more comprehensive understanding of the issue.

## References
Federal Reserve Economic Data (FRED): https://fred.stlouisfed.org  

