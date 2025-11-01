# Multiple Linear Regression on Marketing Promotion Data

## Project Overview
This project analyzes a small business's historical marketing promotion data using **Multiple Linear Regression (MLR)** to estimate sales from several marketing channels — **TV**, **radio**, **social media**, and **influencer promotions**.  

The goal is to help the business understand which promotional efforts most strongly influence sales and guide smarter marketing budget allocation.

---

## Objectives
- Explore and clean marketing data for analysis  
- Identify relationships between independent variables and sales  
- Build and evaluate a multiple linear regression model  
- Check model assumptions (linearity, normality, independence, constant variance, and multicollinearity)  
- Interpret results and communicate findings to non-technical stakeholders  

---

## Key Steps

### 1. Data Exploration
- Used **Pandas** and **Seaborn** to inspect data, visualize relationships, and handle missing values.  
- Continuous variables: `Radio`, `Social Media`, `Sales`  
- Categorical variables: `TV`, `Influencer`  

Findings:
- **Radio** shows a strong linear relationship with sales.  
- **TV** category levels also correlate positively with higher sales.  

---

### 2. Data Cleaning
- Removed missing values using `dropna()`.  
- Renamed columns with underscores for model compatibility.  
- Verified data types and structure.  

---

### 3. Model Building
Used **StatsModels OLS** to fit the regression model:

\[
\text{Sales} = 218.53 - 154.30(\text{TV}_{Low}) - 75.31(\text{TV}_{Medium}) + 2.97(\text{Radio})
\]

Model results:
- **R² = 0.904**, indicating that ~90% of sales variance is explained by the model.  
- **All p-values < 0.05**, confirming statistical significance of predictors.  

---

### 4. Model Assumptions
| Assumption | Status | Notes |
|-------------|---------|-------|
| Linearity | ✅ Met | Scatterplots confirm linear relationship |
| Independence | ✅ Met | Each marketing promotion is independent |
| Normality | ⚠️ Partially met | Slight deviation in residuals |
| Constant variance | ✅ Met | Even spread of residuals around 0 |
| Multicollinearity | ✅ Met | All VIFs < 5 |

---

### 5. Results & Insights
- **TV** and **Radio** marketing have the strongest impact on sales.  
- **Radio budget** increases sales by roughly **2.97 units** per additional million spent.  
- **Low TV** budgets significantly underperform compared to **High TV** budgets.  
- **Influencer** promotions showed weaker relationships and were excluded from the final model.  

---

## Key Takeaways
- Combining **TV and Radio** marketing yields the most predictive power for sales.  
- The model demonstrates strong explanatory performance (**R² = 0.904**).  
- Minor normality issues suggest room for refinement (e.g., transformation or adding more predictors).  

---

## Business Implications
For stakeholders:
- Invest more in **Radio** and **High TV** campaigns for better returns.  
- Reassess influencer marketing effectiveness.  
- Continue tracking promotion-level data for model updates and trend analysis.

---

## Tools & Libraries
- **Python 3**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **StatsModels**, **Scikit-learn**
- **SciPy**, **Patsy**

---

## Dataset
**File:** `marketing_sales_data.csv`  
Each row represents one marketing promotion campaign, with budgets across TV, Radio, Social Media, and Influencer categories.

---

## References
Saragih, H. S. (2020). *Dummy Marketing and Sales Data.*

---

## Author
**Essam Suliman**  
Marketing & Data Analysis Student — SEGi College KL  
