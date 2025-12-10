# Housing Affordability Trends in the United States (1984–2024)
## Contributors
* Arthur Darma (adarma2)
* Laura (ichunc2)

## Summary 
The purpose of this project is to investigate long term housing affordability in the United States by examining the trends in median home prices relative to median household income from 1984 to 2024. During this period, the United States experienced several major economic shifts including deregulation periods, the 2008 financial crisis, and the COVID-19 pandemic, all of which influenced both housing markets and wage dynamics. Our central research question is whether wages have kept pace with increasing housing costs, and whether home affordability has worsened over time.

Our initial project plan included the All Transactions House Price Index (USSTHPI), a widely used indexed measure of changes in housing values. However, as we progressed through the project we discovered that MSPUS (Median Sales Price of Houses Sold) better communicates affordability because it represents actual dollar values rather than index values. MSPUS also aligns directly with household income data (MEHOINUSA646N), which is also expressed in dollars, allowing direct comparisons without conversion. Because of this, we decided to focus primarily on MSPUS and MEHOINUSA646N.

The visualization produced from merging these datasets reveals a clear and consistent pattern: median home prices increased substantially faster than median household income. In the 1980s and early 1990s, both variables showed gradual upward movement, although home prices still grew faster. The divergence, however, becomes most visually significant starting around the early 2000s, especially in the period leading up to the 2008 financial crisis. During this time, easy mortgage access and speculative buying contributed to rapidly rising home values while wages grew slowly and inconsistently.

After the financial crisis, home prices dropped sharply around 2008–2011, while incomes experienced stagnation rather than similar decline. Following this temporary correction, home prices recovered rapidly and continued rising at a much faster rate than income through the 2010s. The most striking part of the graph occurs during 2020–2023, during the COVID-19 period, when home prices surged dramatically due to record low interest rates, and housing inventory shortages. Meanwhile, median income increased only gradually, leading to the steepest affordability gap observed in the 40 year period.

The results strongly reinforce the claim that wage growth has not matched housing price growth and that housing affordability has declined substantially in the United States. This finding is consistent with national discussions of generational wealth, housing inequality, and barriers to homeownership for younger generations. The visualization serves as evidence that housing affordability has become a structural challenge rather than a temporary economic fluctuation.

## Data Profile
### MSPUS
The MSPUS dataset represents the median sales price of homes sold in the United States. It is published and maintained by the Federal Reserve Economic Data system and is widely used in housing market research, economic forecasting, and affordability analysis. The dataset is provided in CSV format and contains historical time series observations going back several decades. The values are expressed in U.S. dollars and represent actual sale prices rather than an index. This is important because the values reflect real, nominal home prices paid by consumers at the time of sale, making the data more intuitive for understanding affordability.

MSPUS is reported at a quarterly frequency, which means that each year contains four separate observations. Because our project focuses on long term trends across multiple decades, we aggregated these quarterly values into annual averages in order to align the dataset with the annual frequency of the income dataset. Annualizing the data also helps remove seasonal fluctuations and month to month market volatility while still capturing broader economic movements. The dataset does not include personal identifiers or geographic breakdowns, making it ethically safe and compliant with privacy requirements.

The MSPUS dataset is particularly suitable for affordability analysis because it provides direct information about housing prices that consumers actually encounter, as opposed to hypothetical or index-based price estimates. Index data such as USSTHPI are valuable for tracking percentage changes but can be difficult for general interpretation. MSPUS reflects real price levels, making it easier to visually compare housing prices to median household income values.
### MEHOINUSA646N
MEHOINUSA646N is also published by FRED and provides historical estimates of median household income. Like MSPUS, it is offered in CSV form and structured as a yearly time series dataset. The values represent nominal U.S. dollars, meaning that income figures are not adjusted for inflation. Because this dataset already follows an annual frequency, no aggregation was required. Using nominal income rather than inflation adjusted values allows us to compare the actual dollar amounts households earned during each year, which aligns directly with the nominal home price values.

Median household income represents the income of the “typical” household rather than the average, which helps avoid distortion caused by extremely high income households. This makes the dataset well suited for affordability studies and long term economic trend analysis. It also provides a valuable perspective on wage growth and purchasing power over time. Since the dataset is population level without any personal or sensitive information, there are no privacy implications associated with its use.

### Ethical and Legal Considerations
Both datasets are openly accessible, publicly maintained sources intended for academic and public use. They do not contain personal identifiers or private records. FRED’s terms of use allow redistribution of derived datasets and visualizations, including academic analysis. Therefore, there are no ethical restrictions or legal limitations relevant for this project.

We selected MSPUS and MEHOINUSA646N because both provide real monetary values that allow direct comparison between home prices and household income. This makes the affordability relationship immediately interpretable, without requiring conversion from index data. Together, these datasets provide clean, trustworthy, and easy to analyze information for evaluating long term housing affordability in the United States.

## Data Quality
Because we set up plan for this project to examines long term affordability trends across forty years, ensuring data consistency and comparability across time is an important part of the workflow. We performed several basic quality checks and preprocessing steps to make sure the data could be meaningfully merged and visualized. The MSPUS dataset is reported quarterly, while the household income dataset is reported annually, so the most important quality consideration was aligning the two sources into a common frequency. To address this, we calculated the yearly average for MSPUS so that each observation would represent a full calendar year. This step removes seasonal fluctuations and short term volatility in the housing market and ensures that both datasets represent similar time intervals.

We also converted the date fields into proper datetime objects. FRED datasets store dates as text strings, so converting them allows easier merging, filtering by year, and visualizing over time. After converting dates and aggregating to annual values, we aligned the overlapping time ranges between the two datasets. Although each dataset spans many years historically, only the shared period (approximately 1984–2024) was used in our final merged dataset. By doing this we could avoid inconsistencies that might be arise from comparing years where only one dataset is present.

Another quality check involved confirming that all values were numeric and properly formatted. Both datasets contain only clean numeric values, so no additional transformations were required. Because FRED is a highly structured data source maintained by the Federal Reserve, the data does not suffer from typical quality issues such as missing values, corrupted entries, or non numeric anomalies. We did not encounter missing years that affected the final merged analysis, and therefore no imputation procedures were necessary.

While the datasets are clean and reliable, there are several methodological limitations related to the nature of the data rather than errors within it. The most important limitation is that both MSPUS and MEHOINUSA646N are nominal values, meaning they are not adjusted for inflation. When inflation rises, nominal income may appear to increase even if purchasing power does not improve. For this reason, a more advanced affordability analysis would include inflation adjustment using CPI-U. However, the purpose of this project was to perform a straightforward comparison of prices and incomes over time, so nominal values were sufficient for demonstrating the growing gap between housing prices and wages.

Another limitation involves averaging quarterly housing prices into annual values. While necessary for alignment, this step smooths monthly variation and reduces short run effects that might be visible in higher frequency data. Still, because the project focuses on long term economic trends rather than short term fluctuations, annualizing is an appropriate strategy and a common practice in economic research.

In summary, although the datasets have structural differences (quarterly vs annual frequencies), the data itself is clean, consistent, and well maintained. After minimal preprocessing, both datasets merged smoothly into a unified time series. The main limitations relate to nominal values and annual averaging rather than data quality problems.

## Findings 
The merged visualization of median home prices and median household income reveals several clear findings about long term affordability in the United States. The most prominent observation is that housing prices have increased at a much faster rate than income since the mid 1980s. While incomes have experienced gradual, steady growth over time, home prices have risen more sharply and have accelerated especially during certain economic periods. This widening gap indicates that, for many households, purchasing a home has become progressively more difficult over the decades even as incomes increased nominally.

A second major finding is that affordability began to decline most notably around the early 2000s. During this period, median home prices rose rapidly due in part to expanding access to mortgage credit, relaxed lending standards, and increasing demand. Meanwhile, median household income did not rise at anywhere close to the same pace. This divergence is especially visible in the visualization and represents a structural turning point where home prices began separating more dramatically from income growth. The early 2000s housing boom directly contributed to the affordability challenges that later peaked during the housing bubble.

The third key finding is that the period from 2020 to 2023 shows the most dramatic affordability gap in the entire timeline. During the COVID-19 pandemic, several factors converged to push home prices upward very quickly. Historically low interest rates made borrowing cheaper, remote work allowed people to move to new locations, and housing inventory shortages limited supply. Increased buyer competition combined with supply issues drove prices up substantially. At the same time, median household income did increase but nowhere near the same magnitude. This led to the steepest divergence between housing prices and income seen in the dataset, suggesting that affordability has become more constrained than ever.

Looking at specific historical events further supports these observations. Around 2006, the United States entered a housing bubble marked by inflated home prices and risky lending products. The graph clearly shows a steep rise in MSPUS during this period. Following that, the financial crisis of 2008 caused a significant crash in home prices. The visualization reflects this drop around 2008–2011, while income did not fall nearly as dramatically. After the crisis, prices eventually recovered and continued rising, but incomes remained comparatively flat. This post crisis recovery period created another widening gap, setting the stage for the even larger affordability challenges that emerged during the pandemic.

Overall, the graph demonstrates that wage growth has not kept pace with housing costs. Incomes move upward in a gradual line, while home prices form a much steeper trajectory. Even without adjusting for inflation, the nominal comparison supports the conclusion that housing affordability has deteriorated over time. For average households, buying a home has become increasingly less attainable, particularly for younger generations who entered the housing market during periods of high price levels and limited wage growth. These findings align with widespread public concerns about housing affordability and provide visual evidence of long term economic imbalance in the United States housing market.

## Future Work
There are several directions that future work could take to extend the analysis presented in this project. One of the most important improvements would be adjusting both home prices and median household income for inflation. Because both datasets are expressed in nominal dollars, long term comparisons can be affected by changes in purchasing power and price levels that occur over time. Using CPI-U (Consumer Price Index for All Urban Consumers) would allow us to convert both series into real dollars, providing a clearer picture of affordability that reflects actual changes in economic conditions rather than nominal growth. Adjusting for inflation would also help us evaluate whether real incomes have been able to keep up with the rising cost of housing once price changes in the broader economy are taken into account.

Another valuable extension would be to calculate a formal affordability ratio, such as dividing the median sales price by median household income, or comparing mortgage payment estimates to income levels. This would create a single metric that could track affordability over time and allow us to summarize how much harder homeownership has become. Affordability ratios are widely used in economic and housing policy research, and including one in future work would make the findings more comparable to external studies.

The analysis could also be expanded geographically. Both datasets used in this project are national averages, which simplifies interpretation but hides important regional and metropolitan differences. Housing markets in major urban areas such as San Francisco, New York, and Austin operate very differently from national trends, and income levels vary significantly across states and regions. Incorporating regional or state level data would allow us to identify where affordability challenges are most severe and how local factors may contribute to housing inequality.

In addition, demographic extensions could provide valuable insight into generational and socioeconomic effects. Research shows that younger generations face greater barriers to homeownership due to slower wage growth and higher entry level housing prices. Exploring demographic types such as age, income, or first time homebuyers, could reveal how affordability changes impact different groups unequally. This would also connect the analysis more closely to public policy discussions centered on wealth inequality and access to housing.

Another area of future work involves forecasting. Time series models could be used to project future home prices and income levels and to estimate how affordability may evolve under different economic scenarios. Forecasting could incorporate variables related to interest rates, construction costs, employment, and demographic trends. Such extensions would be useful for policymakers, economists, and households planning for long term financial decisions.

Finally, future work could involve expanding the dataset to include mortgage rates, inventory data, or housing starts. These variables would help explain why prices rise when incomes do not and could highlight relationships between policy, supply constraints, and affordability outcomes. More comprehensive analysis would deepen our understanding of the structural factors driving housing market changes and would provide a more complete picture of long term afordability in the United States.

## Reproducing 
1. Install Python 3.11 or higher
2. Clone the repository

```
git clone https://github.com/arthurdarma/477.git
```

```
cd 477
```

3. Install requirements

```
pip install -r requirements.txt
```
All raw input data needed by the notebook is already included in the repository under:
data/raw/MSPUS.csv
data/raw/MEHOINUSA646N.csv

4. Next, open the Jupyter notebook:
```
jupyter notebook notebooks/housing_affordability_analysis.ipynb
```
5. Run all cells in the notebook to reproduce the analysis and visualizations.

For archival and grading purposes, this processed output CSV is also uploaded to Box and can be downloaded from the following link:

https://uofi.box.com/s/1g6aryqtevrpbgh4xjvqa35vd0t3sy0c

While Snakemake could automate the workflow, given the simplicity of our pipeline, we use a single Jupyter Notebook with a Run All instruction instead.

## References

Federal Reserve Economic Data (FRED). Median Sales Price of Houses Sold in the United States (MSPUS). https://fred.stlouisfed.org/series/MSPUS
Federal Reserve Economic Data (FRED). Median Household Income in the United States (MEHOINUSA646N). https://fred.stlouisfed.org/series/MEHOINUSA646N