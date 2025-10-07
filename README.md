# Global Cost of Living & Inflation Trends  
### *A Cross-Country Affordability Analysis (2024)*  

**By:** [Atharva Deshmukh](https://github.com/Atharva2901)  
 **Tools Used:** Python (NumPy, Pandas, Scikit-learn, Plotly) | Tableau Public | Numbeo | World Bank  
 [**Interactive Dashboard → View on Tableau Public**](https://public.tableau.com/app/profile/atharva.deshmukh3017/viz/GlobalCostofLivingInflationTrendsACross-CountryAffordabilityAnalysis/Story1?publish=yes)

---

##  Abstract

This project investigates how the **cost of living**, **inflation**, and **income (GDP per capita PPP)** interact across countries to shape global affordability.  
Using real-world data from **Numbeo** and **World Bank Open Data**, the study constructs an **Affordability Ratio = Cost of Living / GDP per Capita** and applies **K-Means clustering** to categorize nations into three groups:  Affordable,  Expensive, and  Volatile.  

An interactive **Tableau Public story** visualizes these relationships through geographic, comparative, and ranking perspectives, helping identify **global economic disparities** and **inflation-driven cost pressures**.

---

## Objective & Problem Statement

> **How do income levels and inflation trends affect the real affordability of living across nations?**

Traditional cost-of-living comparisons overlook income strength and inflation effects.  
This project provides a **composite view of affordability**, analyzing how prices, purchasing power, and inflation interact to highlight imbalances between prosperity and consumer well-being across regions.

---

## Data Sources & Tools

| Source | Dataset | Description |
|---------|----------|-------------|
| **Numbeo (via Kaggle)** | Cost of Living Index 2024 | Provides indices for rent, groceries, restaurants, and overall living costs. |
| **World Bank Open Data** | CPI (FP.CPI.TOTL), Inflation %, GDP per Capita (PPP) | Macroeconomic indicators for 200+ countries. |
| **Python Libraries** | Pandas, NumPy, Scikit-learn, Plotly | Data cleaning, merging, analysis, clustering. |
| **Tableau Public** | Story dashboards | Visualization & storytelling platform. |

**Total countries analyzed:** 100  **Time frame:** 2024 (latest data)

---

## Data Preparation & Methodology

- **Data Merging:** Combined Numbeo indices with World Bank GDP and inflation data on country.  
- **Feature Engineering:** Created `Affordability Ratio = Cost of Living Index / GDP per Capita (PPP)` → lower = better affordability.  
- **Preprocessing:** Handled missing values and standardized numeric fields (`StandardScaler`).  
- **Clustering (K-Means):** Optimal *k = 3* (via Elbow + Silhouette). Used features → `Cost_of_Living_Index`, `GDP_per_capita_PPP`, `Inflation_percent`, `Affordability_Ratio`.  
- **Visualization:** Exported final dataset → built interactive dashboards and story points in Tableau.

---

## Exploratory Findings & Correlations

| Variable | Description | Global Range (2024) |
|-----------|--------------|---------------------|
|  Cost of Living Index | Relative price level | 18.8 → 101.1 |
|  GDP per Capita (PPP) | Income measure | $1 ,884 → $150 ,772 |
|  Inflation (%) | Annual consumer price change | −0.46 → 33.24 |
|  Affordability Ratio | Cost ÷ Income | 0.00041 → 0.01301 |

**Correlation Summary (rounded):**  
- GDP vs Cost of Living → **+0.66** (wealthier countries = higher prices)  
- GDP vs Affordability Ratio → **−0.54** (higher income = better affordability)  
- Inflation vs Affordability Ratio → **+0.33** (inflation erodes affordability)  

**Interpretation:** High-GDP countries often show higher costs, but strong income levels neutralize inflation effects.  
Developing economies have weaker income buffers, so small inflation rises cause steep cost pressures.

---

##  Cluster Analysis (K = 3)

| Cluster | Countries | Cost Index | GDP PPP | Inflation % | Affordability Ratio | Interpretation |
|:--:|:--:|:--:|:--:|:--:|:--:|:--|
|  **0** | 8 | 31.92 | 6 ,515 | 11.19 | 0.00526 | Low income + high inflation → least affordable. |
|  **1** | 51 | 35.33 | 26 ,830 | 3.49 | 0.00157 | Mid income, balanced cost & inflation. |
|  **2** | 33 | 62.47 | 75 ,508 | 2.27 | 0.00094 | High income, expensive but stable. |

**Cluster 0:** Developing economies (Egypt, Kenya, Bangladesh) → low costs but low incomes & high inflation.  
**Cluster 1:** Emerging markets → moderate prices, stable growth, moderate inflation.  
**Cluster 2:** Advanced economies (Switzerland, Singapore, Norway) → high prices, very high income, strong purchasing power.

![Global Map](visuals\elbow_silhoutte_snaps\elbow_method.jpg)
![Global Map](visuals\elbow_silhoutte_snaps\silhoutte_scores.jpg)
---

##  Key Insights & Discussion

- **Affordability ≠ Low Prices:** Low-cost countries often face low income & inflation volatility.  
- **Income Buffer Matters:** High-income countries sustain costs without losing affordability.  
- **Inflation’s Uneven Impact:** Same inflation rate affects nations differently.  
- **Purchasing Power Gap:** Affordability divide between developed and developing economies is widening.  
- **Global Stability Zones:** Western Europe, North America, and Gulf countries remain stable; South Asia & Africa are vulnerable.
- 
**![Global Map](visuals\tableau_screenshots\Gobal_clusters_map.jpg)**
---

##  Conclusion & Recommendations

This analysis proves that **living-cost evaluations must include both income and inflation** to reflect true affordability.  
The **Affordability Ratio** is a robust composite measure of real well-being.  

**Policy Focus:**
1. Strengthen income growth to offset inflation.  
2. Manage inflation expectations in developing economies.  
3. Promote price transparency & purchasing-power metrics for cross-country comparisons.  

**Future Extensions:** time-series forecasting, regional segmentation (OECD vs non-OECD), and policy simulation scenarios to evaluate income and inflation effects over time.

---

##  References & Project Links

-  **Interactive Tableau Story:** [Global Cost of Living & Inflation Trends](https://public.tableau.com/app/profile/atharva.deshmukh3017/viz/GlobalCostofLivingInflationTrendsACross-CountryAffordabilityAnalysis/Story1?publish=yes)  
-  **Dataset:** Numbeo (via Kaggle, 2024) | World Bank Open Data (CPI, Inflation %, GDP PPP)  
-  **Tools Used:** Python (Pandas, Scikit-learn, Plotly), Tableau Public  
-  **Created By:** Atharva Deshmukh, Stevens Institute of Technology (2025)

---
