# 🏥Pharmaceutical Drug Spending by Countries 🗺

**Team Members:** 

* Aliya Asad ([AliyaAsad](https://github.com/AliyaAsad))
* Koukou Tian ([tqq199548](https://github.com/tqq199548))
* Pavanndeep Kaur ([Pavendeep93](https://github.com/Pavandeep93))
* Reza Tehrani ([RezaDSI](https://github.com/RezaDSI))
* Victor Leung ([Vleung3782](https://github.com/Vleung3782))

# **Project Background**
**Why is Pharmaceutical Drug Spending Important?**

Pharmaceutical spending is a key component of healthcare expenditure worldwide. It represents the cost incurred by individuals, governments, and insurance providers on prescription drugs, over-the-counter medicines, and self-medication.
In recent years, rising drug costs have raised concerns regarding:
Affordability: Higher drug prices make essential medications inaccessible to lower-income populations.
Healthcare Policy: Policymakers and governments aim to balance innovation incentives for pharmaceutical companies while regulating costs.
Economic Burden: Pharmaceutical spending impacts GDP, public health budgets, and insurance systems.



# **Project Overview**

This project analyzes global pharmaceutical drug spending trends, comparing expenditures across different countries and identifying key economic and healthcare insights. The goal is to uncover the latest patterns that help policymakers, pharmaceutical companies, and healthcare professionals make informed decisions.

**🔎 Key Business Questions:**

✔Investigate the relationship between pharmaceutical spending and GDP in years. 

✔How does GDP impact pharmaceutical spending across countries? 

**💡 Potential Impact:**

 -For Policymakers: Optimize drug pricing policies & healthcare budgets
 
 -For Investors: Identify high-growth pharmaceutical markets
 
 -For Healthcare Providers: Understand the affordability of medications

# **Technologies Applied**

-Data Processing: Python (Pandas, NumPy)

-Visualization: Matplotlib
 
-Modeling: Scikit-learn (Regression, Clustering)
 
-Collaboration: GitHub, Jupyter Notebook


# **Dataset & Sources**

🔗 Dataset used: Pharmaceutical Drug Spending - DataHub https://datahub.io/core/pharmaceutical-drug-spending

📌 Key Features in the Dataset:

| Variables      | Meaning                                    | Potential Link                                                    |
|--------------|---------------------------------------------|--------------------------------------------------------------------|
| LOCATION     | Country code                                | Compare different countries' spending patterns                     |
| TIME         | Year                                       | Analyze trends over time (e.g., drug spending growth)              |
| PC_HEALTHXP  | % of total health spending allocated to drugs | See how drug costs contribute to overall healthcare expenses     |
| PC_GDP       | % of GDP spent on drugs                    | Compare pharmaceutical spending to economic growth                  |
| USD_CAP      | Drug spending per capita (PPP-adjusted)     | Evaluate affordability & impact on individuals                     |
| TOTAL_SPEND  | Total national drug spending (millions)     | Measure overall market size & growth                               |


# **Data Overview**

**🌍 View the Interactive Map**

👉 [Click here to view the Pharmaceutical Spending Map] https://tqq199548.github.io/pharma-map/

**🗨Data Set Q&A**
| Question                                                 | Analysis                                     |
|:---------------------------------------------------------|:---------------------------------------------|
| How many countries are in this dataset?                  | There are 44 countries in this dataset.      |
| How many years are in this dataset?                      | There are 53 years in this dataset.          |
| What is the year range of this dataset?                  | The data ranges from the years 1970 to 2022. |
| What is the total number of observations in the dataset? | There are 1341 observations in this dataset. |
| What is the total number of possible observations?       | There are 2332 possible observations.        |
| How many values are missing?                             | There are 0 missing values in the dataset.   |


# **Data Cleaning & Preprocessing**
    
**Heatmap of correlation**

<img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/correlation_heatmap.png" width="500">


To gain an initial understanding of how the variables interact, a correlation heatmap was generated. Several noteworthy correlations emerge:

- **PC_HEALTHXP** and **PC_GDP** show a relatively strong positive correlation(0.72), suggesting that countries spending a higher percentage of GDP on pharmaceuticals also tend to allocate a larger share of their health budgets to pharmaceuticals.

- **PC_GDP** and **USD_CAP** display a moderately high correlation(0.64), indicating that as pharmaceutical spending rises relative to GDP, per capita spending in USD also tends to increase.

**Visualizing missing years and selection of timeframe**

![alt text](https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/pivot_table.png)

This pivot table clearly illustrates data availability across different countries and years. Each green cell represents an existing observation for a given country-year combination, while the white cells highlight missing years.From this visualization, we can quickly see which years and countries are most densely populated with data. For instance, certain earlier years may have sporadic coverage, whereas more recent years often feature more consistent records. This overview is crucial for determining where data imputation will be needed. 

To complement the pivot table, we also generated a summary table that lists, for each country, the total number of observations, the count of missing values, and the percentage of missing data specifically from 2011 to 2021. This numeric breakdown helps us quantify data gaps more precisely.


## Rationale for Using 2011–2021
 - **Recency and Relevance**: By narrowing our focus to 2011–2021, we ensure our analysis captures modern trends in pharmaceutical spending, making our insights more applicable to current policy and market decisions.

- **Consistent Coverage**: Both the pivot table and the numeric summary reveal that most countries have more comprehensive data for this recent decade. Limiting our scope to these years minimizes the extent of missing values and, consequently, reduces the need for imputation.

- **Reduced Complexity**: A decade-long timeframe offers a balanced window for capturing meaningful variations in spending without digging deep into older and potentially less relevant data. This more focused dataset is easier to manage and helps us draw clearer comparisons across countries.


# **Data Exploration**

**1. Identify Top 10 and Bottom 10 Countries (based on USD per capita pharmaceutical spending):**

**-Top 10 Countries:** 

<img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Top%2010%20spenders.png" width="500">

**Key Observations:**

The USA leads significantly, with the highest per capita spending Other high spenders include: Malta (MLT) → A comparatively smaller economy country with high per capita spending. Switzerland (CHE) → Known for its robust healthcare system. France (FRA) → Major European economy with steady healthcare investments

------------

**-Bottom 10 Countries:**

<img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Bottom%2010%20spenders.png" width="500">


**Key Observations:**

Gradual Increase: The spending increases gradually from the top to the bottom of the list, with the last country on the list having the highest spending among these ten, approaching 400 USD. The list includes a mix of countries from different regions, such as Europe (Croatia, Estonia, Denmark), the Middle East (Israel), and Latin America (Chile, Brazil, Mexico, Costa Rica, Colombia). This indicates that low spending per capita is not confined to one specific region but is a global issue.

-------

**2. Scatter Plot Review on Outliers**

<img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/Identifying-Top-10-and-Bottom-10-Country-Spenders/Scatter%20plot%20new.png" width="500">

**Key Observations:**

The USA shows exceptionally high pharmaceutical spending per capita (730 USD) despite a low GDP percentage (1.6%), indicating disproportionate spending and BGR (Bulgaria) exhibits significantly low spending (461 USD),despite allocating 2.5% of its GDP, making it an outlier on the lower end. BY examining the scatter plot, most of the data points form an upward-sloping pattern, as GDP% increases, pharmaceutical spending per capita generally rises, indicating a positive correlation.

-----------

**3. Clustering Analysis**

**Elbow Plot Review** 

The primary purpose of Elbow Plot Review is to:

1. Identify the Optimal k
   
2. Avoid Overfitting or Underfitting

3. Improve Interpretability of Clusters

<p align="center">
    <img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Elbow%20Method%20For%20Optimal%20k%20(USD_CAP%20%26%20TOTAL_SPEND).png" width="400" height="300">
    <img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Elbow%20Method%20For%20Optimal%20k%20with%20Line%20for%20k%3D3%20(PC_GDP%20%26%20PC_HEALTHXP).png" width="400" height="300">
    <img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Elbow%20Method%20For%20Optimal%20k%20with%20Line%20for%20k%3D3%2C%20USD_CAP%20%26%20PC_GDP.png" width="400" height="300">
</p>

**Primary purpose of Clustering Analysis:**

1. Identify patterns of data that may not be immediately apparent

2. Segment data into meaningful sub-group or clusters, allowing for more focused analysis & decision making

3. Facilitate further data exploration that could lead to new insights & discoveries.



**Clustering Analysis for the following feature pairs:**

1. PC_GDP & PC_HEALTHXP
2. USD_CAP & PC_GDP
3. USD_CAP & TOTAL_SPEND

---------------------------
**Clustering Analysis for PC_GDP & PC_HEALTHXP, optimal k=3**

<img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Scatter%20Plot%20of%20PC_GDP%20vs%20PC_HEALTHXP%20(k%3D3).png" width="800">

**Oberservation:** 

Cluster 0: ['AUS', 'AUT', 'BEL', 'CHE', 'COL', 'CRI', 'CYP', 'DNK', 'EST', 'FIN', 'GBR', 'IRL', 'ISL', 'ISR', 'LUX', 'NLD', 'NOR', 'SWE']

Cluster 1: ['BRA', 'CAN', 'CZE', 'DEU', 'ESP', 'FRA', 'HRV', 'ITA', 'JPN', 'KOR', 'LTU', 'LVA', 'MEX', 'MLT', 'POL', 'PRT', 'ROU', 'SVK', 'SVN', 'USA']

Cluster 2: ['BGR', 'GRC', 'HUN']

----------------------------

**Clustering Analysis for PC_GDP & USD_CAP, optimal k=3**

<img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Scatter%20Plot%20of%20PC_GDP%20vs%20USD_CAP%20(k%3D3).png" width="800">


**Oberservation:** 

Cluster 0: ['AUS', 'AUT', 'BEL', 'BRA', 'COL', 'CRI', 'CYP', 'CZE', 'DNK', 'ESP', 'EST', 'FIN', 'GBR', 'IRL', 'ISL', 'ISR', 'ITA', 'LUX', 'NLD', 'NOR', 'PRT', 'SVN', 'SWE']

Cluster 1: ['BGR', 'GRC', 'HRV', 'HUN', 'KOR', 'LTU', 'LVA', 'MEX', 'POL', 'ROU', 'SVK']

Cluster 2: ['CAN', 'CHE', 'DEU', 'FRA', 'JPN', 'MLT', 'USA']

-----------------------------
**Clustering Analysis for USD_CAP & TOTAL_SPEND (with USA data), optimal k=3**

<img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Scatter%20Plot%20of%20USD_CAP%20vs%20TOTAL_SPEND%20(k%3D3).png" width="800">


**Oberservation:** 

Cluster 0 for k=3: ['AUS', 'AUT', 'BEL', 'BGR', 'BRA', 'CHE', 'COL', 'CRI', 'CYP', 'CZE', 'DNK', 'ESP', 'EST', 'FIN', 'GBR', 'GRC', 'HRV', 'HUN', 'IRL', 'ISL', 'ISR', 'ITA', 'KOR', 'LTU', 'LUX', 'LVA', 'MEX', 'MLT', 'NLD', 'NOR', 'POL', 'PRT', 'ROU', 'SVK', 'SVN', 'SWE']

Cluster 1 for k=3: ['USA']

Cluster 2 for k=3: ['CAN', 'DEU', 'FRA', 'JPN']

--------------------------------------------
**Clustering Analysis for USD_CAP & TOTAL_SPEND (WITHOUT USA data), optimal k=3**

<img src="https://github.com/tqq199548/Team_2_Pharmaceutical_Drug_Spending_by_Countries/blob/main/Backup-Pictures/Scatter%20Plot%20of%20USD_CAP%20vs%20TOTAL_SPEND%20(k%3D3)%20EXCLUDE%20USA.png" width="800">

**Oberservation:** 

Cluster 1: BRA, COL, CRI, CYP, DNK, EST, HRV, ISR, LVA, MEX, NLD, NOR, POL, PRT, ROU

Cluster 2: CAN, DEU, FRA, JPN

Cluster 3: AUS, AUT, BEL, BGR, CHE, CZE, ESP, FIN, GBR, GRC, HUN, IRL, ISL, ITA, KOR, LTU, LUX, MLT, SVK, SVN, SWE



# **🏁Key Findings from the Analysis📌**

**1️⃣ Pharmaceutical Spending is Strongly Correlated with Economic Strength.**

Developed countries (e.g., USA, Canada, Switzerland, Germany) allocate significantly higher per capita and total spending on pharmaceuticals.
Developing nations (e.g., Mexico, Brazil, Colombia) have lower absolute spending but may still allocate a substantial percentage of GDP to pharmaceuticals.

**2️⃣ Clustering Analysis Reveals Spending Patterns**

Countries cluster into three distinct groups based on PC_GDP, PC_HEALTHXP, and USD_CAP.
Cluster 2 (USA, Switzerland, Canada, Germany) represents high-income nations with very high per capita spending.
Cluster 0 & 1 show a mix of developed & developing economies, indicating varying affordability levels for pharmaceuticals.

**3️⃣ The USA is a Significant Outlier**

The USA has exceptionally high pharmaceutical spending, standing alone in some clusters (US per capital spending more than doubled compared to some developed countries).
Possible reasons: Higher drug prices, private healthcare dominance, and patent-protected medications.

**4️⃣ Spending vs. Health Outcomes**

Higher per capital spending positively correlates with better healthcare quality rankings and life expectancy.
However, inefficiencies exist, as some high-spending countries do not always have the best healthcare outcomes.

# **📈Recommendations**

**🔹 For Policymakers:**
Implement price control measures on essential medications.
Encourage the adoption of generic drugs to lower costs.

**🔹 For Investors & Pharmaceutical Companies:**
Invest in emerging pharmaceutical markets in developing economies.
Explore trends in aging populations that drive higher pharmaceutical demand.

**🔹 For Healthcare Systems & Insurers:**
Develop strategies to ensure affordable drug pricing without stifling innovation.
Promote preventative healthcare to reduce overall pharmaceutical dependency.

# **🗨 For Future Research & Analysis:**
Investigate government healthcare policies and their impact on drug pricing.
Analyze the impact of pharmaceutical R&D investments on national drug costs.
Expand the dataset to include post-2022 trends, particularly in the aftermath of the COVID-19 pandemic.

# **Videos:**
