Global Cost of Living & Inflation Trends:
A Cross-Country Affordability Analysis

By: Atharva Deshmukh
Tools Used: Python (Numpy, Pandas, Scikit-learn, Plotly) | Tableau Public | Numbeo | World Bank
Interactive Dashboard: View on Tableau Public

Abstract
This project investigates how the cost of living, inflation, and income (GDP per capita PPP) interact across countries to shape global affordability. Using real-world data from Numbeo and World Bank Open Data, the study constructs an Affordability Ratio (Cost of Living ÷ GDP per capita) and applies K-Means clustering to categorize nations into three groups: Affordable, Expensive, and Volatile.
An interactive Tableau Public story visualizes these relationships through geographic, comparative, and ranking perspectives, helping identify global economic disparities and inflation-driven cost pressures.

Objective & Problem Statement
The central question guiding this research is:
“How do income levels and inflation trends affect the real affordability of living across nations?”
While traditional cost-of-living comparisons overlook income strength and inflation effects, this project seeks to provide a composite view of affordability. By analyzing the interaction of prices, purchasing power, and inflation, it highlights the imbalance between economic prosperity and consumer well-being across different income groups and regions.




Data Sources & Tools

Source	Dataset	Description
Numbeo (via Kaggle)	Cost of Living Index 2024	Provides cost indices for rent, groceries, restaurants, and overall living costs.
World Bank Open Data	CPI (FP.CPI.TOTL), Inflation %, GDP per Capita (PPP)	Offers macroeconomic indicators for 200+ countries.
Python Libraries	Pandas, NumPy, scikit-learn, Plotly	Data cleaning, merging, analysis, and clustering.
Tableau Public	Story dashboards	A visualization and storytelling platform for the final analysis.
Total countries analyzed: 100
Time frame: 2024 (latest data available)

Data Preparation & Methodology

•	Data Merging:
Combined Numbeo’s cost indices with World Bank GDP and inflation data using the country as the join key.
•	Feature Engineering:
Created a key metric:
Affordability Ratio = Cost of Living Index/ GDP per Capita (PPP)
Lower values indicate better affordability relative to income.
•	Preprocessing:
o	Handled missing values and normalized numeric fields.
o	Used StandardScaler to standardize features for clustering.
•	Clustering (K-Means):
o	Determined optimal k = 3 via Elbow and Silhouette methods.
o	Clustered countries using:
Cost_of_Living_Index, GDP_per_capita_PPP, Inflation_percent, and Affordability_Ratio.
•	Visualization:
Exported the final dataset and built interactive dashboards and story points in Tableau to illustrate insights visually.

Exploratory Findings & Correlations

Variable	Description	Global Range (2024)
Cost of Living Index	Relative price level	18.8 => 101.1
GDP per Capita (PPP)	Income measure	$1,884 => $150,772
Inflation (%)	Annual consumer price change	−0.46 => 33.24
Affordability Ratio	Cost ÷ Income	0.00041 => 0.01301
Correlation Summary (rounded):
•	GDP vs Cost of Living => +0.66 (wealthier countries = higher prices)
•	GDP vs Affordability Ratio => −0.54 (higher income = better affordability)
•	Inflation vs Affordability Ratio => +0.33 (inflation erodes affordability)
Interpretation:
High GDP countries often exhibit higher living costs, but their strong income levels neutralize inflation effects, keeping affordability stable. Developing economies, however, experience weaker income buffers, so even small inflation increases lead to steep cost pressure.





Cluster Analysis (K = 3)
Cluster	Countries	Cost Index	GDP PPP	Inflation %	Affordability Ratio	Interpretation
0	8	31.92	6,515	11.19	0.00526	Low-income, higher inflation =>least affordable.
1	51	35.33	26,830	3.49	0.00157	Mid-income, moderate cost & inflation => balanced affordability.
2	33	62.47	75,508	2.27	0.00094	High-income, high cost but stable inflation => expensive yet highly livable.
Cluster 0: Developing economies (e.g., Egypt, Kenya, Bangladesh), low costs but low incomes and high inflation.
Cluster 1: Emerging markets: moderate prices, stable growth, moderate inflation.
Cluster 2: Advanced economies (e.g., Switzerland, Singapore, Norway), high prices but very high incomes; strong purchasing power.


Key Insights & Discussion
•	Affordability ≠ Low Prices: Countries with low nominal costs often suffer from lower incomes and inflation volatility.
•	Income Buffer Matters: High-income countries sustain higher living costs without losing affordability.
•	Inflation’s Uneven Impact: The same inflation rate affects affordability differently across income groups.
•	Purchasing Power Gap: The affordability divide between developed and developing economies continues to widen.
•	Global Stability Zones: Western Europe, North America, and the Gulf countries maintain stable affordability; South Asia and parts of Africa remain vulnerable.

Conclusion & Recommendations
This analysis demonstrates that living cost evaluations must consider both income and inflation to assess real affordability.
The Affordability Ratio serves as a reliable composite measure for comparing economic well-being across nations.
Policy focus should be on:
1.	Strengthening income growth to offset inflation effects.
2.	Managing inflation expectations in developing economies.
3.	Promoting price transparency and real purchasing power indicators in international comparisons.
Future extensions can include time-series forecasting, regional segmentation (OECD vs non-OECD), and policy simulation scenarios to understand affordability under different inflation or income growth rates.

References & Project Links
•	Interactive Tableau Story: Global Cost of Living & Inflation Trends: Tableau Public
•	Dataset: Numbeo (via Kaggle, 2024) | World Bank Open Data (CPI, Inflation %, GDP PPP)
•	Tools Used: Python (Pandas, scikit-learn, Plotly), Tableau Public
•	Created by: Atharva Deshmukh, Stevens Institute of Technology, 2025

