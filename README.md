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

# **Methodology and Technologies**

**Methodology**

-Data Reviewing, Data Cleaning & Preprocessing

-Exploratory Data Analysis (EDA)

-Statistical Analysis & Top 10 and Bottom 10 (2011-2021)

-Clustering Analysis 

**Technologies**

-Data Processing: Python (Pandas, NumPy)

-Visualization: Matplotlib
 
-Modeling: Scikit-learn (Regression, Clustering)
 
-Collaboration: GitHub, Jupyter Notebook


# **Dataset & Sources**

🔗 Dataset used: Pharmaceutical Drug Spending - DataHub https://datahub.io/core/pharmaceutical-drug-spending

📌 Key Features in the Dataset:

![alt text](https://github.com/tqq199548/Team-2-Cohort-5/blob/3d42a8f1c6b6f83a6e8a16e9bbfea1e5296988ca/Backup-Pictures/image-1.png)


# **Data Over View**

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

**Data Cleaning**
  
1. **Heatmap of correlation** to analyze relationships between variables.  
2. **Scatter plot** of all countries and timeframes to observe graph patterns.  
3. **Pivot table** to visualize missing years and select years along with risk factors.  
4. **Missing Values Table**: Overview of the number of countries with missing data, highlighting those that require imputation.
5. **Imputation of missing values** along with risk factors.


**Heatmap of correlation**

To gain an initial understanding of how the variables interact, a correlation heatmap was generated. Several noteworthy correlations emerge:

- **PC_HEALTHXP** and **PC_GDP** show a relatively strong positive correlation(0.72), suggesting that countries spending a higher percentage of GDP on pharmaceuticals also tend to allocate a larger share of their health budgets to pharmaceuticals.

- **PC_GDP** and **USD_CAP** display a moderately high correlation(0.64), indicating that as pharmaceutical spending rises relative to GDP, per capita spending in USD also tends to increase.

**Visualizing missing years and selection of timeframe**

xxxxx picture

This pivot table clearly illustrates data availability across different countries and years. Each green cell represents an existing observation for a given country-year combination, while the white cells highlight missing years.From this visualization, we can quickly see which years and countries are most densely populated with data. For instance, certain earlier years may have sporadic coverage, whereas more recent years often feature more consistent records. This overview is crucial for determining where data imputation will be needed. 

To complement the pivot table, we also generated a summary table that lists, for each country, the total number of observations, the count of missing values, and the percentage of missing data specifically from 2011 to 2021. This numeric breakdown helps us quantify data gaps more precisely:

- Countries with low or zero missing values are prime candidates for in-depth analysis without requiring extensive data imputation.
- Countries with high percentages of missing data highlight areas where additional investigation or targeted imputation strategies may be necessary.

## Rationale for Using 2011–2021
 - **Recency and Relevance**: By narrowing our focus to 2011–2021, we ensure our analysis captures modern trends in pharmaceutical spending, making our insights more applicable to current policy and market decisions.

- **Consistent Coverage**: Both the pivot table and the numeric summary reveal that most countries have more comprehensive data for this recent decade. Limiting our scope to these years minimizes the extent of missing values and, consequently, reduces the need for imputation.

- **Reduced Complexity**: A decade-long timeframe offers a balanced window for capturing meaningful variations in spending without digging deep into older and potentially less relevant data. This more focused dataset is easier to manage and helps us draw clearer comparisons across countries.




# **Data Exploration**

Top 10

Bottom 10

Cluster Review

# **Risks**

# **Conclusion**

# **More Actions** 
