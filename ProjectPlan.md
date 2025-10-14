# Project Plan

## Overview
This project will analyze long-term economic trends in the United States by 
examining the relationship between housing prices and wages over the last 40 years. 
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
Documentation Lead. I will be responsible for downloading and managing datasets, 
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

This project will follow the data lifecycle model introduced in class, 
beginning with data acquisition from the FRED database, where datasets will be downloaded 
in CSV format and stored in a structured repository. Raw data will be preserved without 
alteration, and metadata will be documented to describe the origin, structure, and 
variables of each dataset. Data will be integrated using Python and the Pandas library by 
aligning datasets on a common year variable. During this process, data quality checks will be 
conducted to identify missing years, inconsistent units, or unusual values. 
Cleaning procedures will be applied as necessary, including handling missing records and 
potentially adjusting income values for inflation to allow meaningful comparisons over time. 
All datasets used are publicly available and contain no personal or sensitive information, 
so privacy risks are minimal; however, ethical data practices will still be maintained, 
including citing all sources and avoiding misleading transformations.

## Timeline
Data collection and repository structure setup will be completed by mid to late October. 
Data integration will be completed shortly afterward, followed by cleaning and inflation 
adjustment. The interim project report will be submitted by November 11, 2025. 
The main analysis and visualization work will be done through late November. The final 
report and GitHub release will be completed by December 10, 2025.

## Constraints
Income values may need inflation adjustment using an additional dataset.

## Gaps
A decision has not yet been made on how to adjust for inflation, though using the 
Consumer Price Index dataset is a likely approach. 

## References
Federal Reserve Economic Data (FRED): https://fred.stlouisfed.org  

