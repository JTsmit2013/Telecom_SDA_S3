# Telecom_SDA_S3

## Statistical Data Analysis for Megaline  
**Revenue Comparison: Surf vs. Ultimate Prepaid Plans**  

---

## Overview  
This project analyzes customer behavior to determine which of Megaline's prepaid plans—**Surf** or **Ultimate**—generates higher monthly revenue. Using 2018 usage data from 500 customers, the analysis supports strategic decisions for advertising and pricing.

---

## Objectives  
1. Prepare and clean the datasets for analysis.  
2. Analyze usage behavior in terms of call minutes, texts, and data per user per month.  
3. Calculate monthly revenue for each customer, accounting for overage fees.  
4. Test hypotheses to:  
   - Compare average revenues between Surf and Ultimate plan users.  
   - Evaluate revenue differences by geographic region (e.g., NY-NJ area vs. others).  
5. Provide actionable insights for Megaline’s commercial team.

---

## Data Overview  
⚠️ **Note:** The datasets used in this project are **not provided** in the repository. This project is for demonstration and educational purposes only.

The analysis is based on five datasets:  
- **Users** – Customer demographics and subscription details  
- **Calls** – Call durations per user per date  
- **Messages** – Text messages sent by date and user  
- **Internet** – Web session data (MB used per session)  
- **Plans** – Plan pricing and monthly allowances  

---

## Project Workflow  

### 1. Data Preparation  
- Converted date fields to datetime objects  
- Merged usage data with user and plan info  
- Aggregated monthly usage per user for:  
  - Call minutes (rounded up per call)  
  - Text messages  
  - Internet usage (MB to GB, rounded up)  
- Handled missing data and churned customers appropriately  

### 2. Revenue Calculation  
- Calculated monthly revenue by summing:  
  - Base monthly fee  
  - Overage fees for:  
    - Minutes (if over plan limit)  
    - Messages (if over plan limit)  
    - Internet (rounded GB overage × $ per GB)

### 3. Exploratory Analysis  
- Surf users tend to use fewer minutes, texts, and data on average  
- Ultimate users have more generous limits, resulting in fewer overage charges  
- Visualized distributions using histograms and boxplots  
- Calculated descriptive statistics (mean, std. dev., etc.)

### 4. Hypothesis Testing  
#### A. Revenue by Plan  
- **Null Hypothesis (H₀):** Mean revenue of Surf and Ultimate users is equal  
- **Alternative Hypothesis (H₁):** Mean revenues differ  
- **Result:**  
  - p-value < 0.05  
  - ✅ Reject H₀ → There **is** a statistically significant difference  
  - **Ultimate** plan users generate higher average revenue  

#### B. Revenue by Region (NY-NJ vs. Others)  
- **Null Hypothesis (H₀):** No revenue difference between NY-NJ area and other regions  
- **Result:**  
  - p-value > 0.05  
  - ❌ Do not reject H₀ → No statistically significant difference in average revenue by region  

---

## Key Findings & Conclusions  

- **Ultimate plan generates more revenue**:  
  On average, Ultimate users yield higher monthly revenue, primarily due to higher base fees and more consistent usage.
  
- **Surf plan users incur more overage fees**, especially for data. However, even with overages, they tend to generate less total revenue.

- **No regional revenue difference**: Customers in the NY-NJ region do not spend more than those in other areas, suggesting regional advertising should not be prioritized based on revenue alone.

---

## Recommendations  

- 📣 **Focus marketing on Ultimate plan**: Higher monthly fees and lower churn potential make it more profitable. Consider emphasizing its value in advertising.

- 📊 **Analyze churn data further**: Future work could assess if plan type correlates with churn behavior.

- 🌐 **Consider increasing Surf overage fees** or adjusting data limits to boost its profitability.

---

## Deliverables  
- Jupyter notebook with:
  - Cleaned and merged datasets  
  - Monthly usage and revenue calculations  
  - Visualizations of usage patterns  
  - Two hypothesis tests with statistical interpretations  
- Strategic insights to support pricing and marketing decisions  

---

## Tools & Libraries  
- Jupyter Notebook  
- Python 3.x  
- `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`  

---

## How to Use  
1. Clone the repository.  
2. Ensure the required datasets are available locally (not included here).  
3. Open `Telecom_S3.ipynb` in Jupyter Notebook.  
4. Run all cells to reproduce the analysis.
