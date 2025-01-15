# Telecom_SDA_S3

# README  

## Project Title  
**Revenue Analysis of Megaline Prepaid Plans: Surf vs. Ultimate**  

## Project Overview  
This project analyzes customer behavior to determine which of Megaline's prepaid plans, Surf or Ultimate, generates more revenue. By examining usage data from 500 clients in 2018, this analysis will provide insights into customer behavior and guide Megaline's advertising budget allocation.  

## Objectives  
1. Clean and prepare the provided datasets for analysis.  
2. Analyze client behavior for calls, texts, and internet usage.  
3. Calculate monthly revenue per user, considering plan limits and overage charges.  
4. Perform hypothesis testing to:  
   - Compare average revenues between the two plans.  
   - Examine revenue differences between regions (e.g., NY-NJ area vs. others).  
5. Present conclusions and actionable insights for Megaline's commercial department.  

## Dataset Description  
The analysis is based on five datasets:  

### 1. Users  
- Contains demographic and plan details of clients.  
- Key columns:  
  - `user_id`  
  - `city`  
  - `plan`  
  - `reg_date`  
  - `churn_date`  

### 2. Calls  
- Includes data on calls made by users.  
- Key columns:  
  - `user_id`  
  - `call_date`  
  - `duration`  

### 3. Messages  
- Tracks text messages sent by users.  
- Key columns:  
  - `user_id`  
  - `message_date`  

### 4. Internet  
- Logs web session usage data.  
- Key columns:  
  - `user_id`  
  - `session_date`  
  - `mb_used`  

### 5. Plans  
- Details of Surf and Ultimate plans, including limits and overage charges.  
- Key columns:  
  - `plan_name`  
  - `usd_monthly_fee`  
  - `minutes_included`  
  - `messages_included`  
  - `mb_per_month_included`  
  - `usd_per_minute`  
  - `usd_per_message`  
  - `usd_per_gb`  

## Project Workflow  
1. **Data Preparation**  
   - Convert data types as needed.  
   - Handle missing values and outliers.  
   - Calculate monthly usage metrics per user for calls, texts, and internet.  

2. **Revenue Calculation**  
   - Compute monthly revenue by considering:  
     - Plan limits (minutes, messages, and data).  
     - Overage charges (calls, texts, and extra data usage).  

3. **Data Analysis**  
   - Visualize and describe distributions of calls, texts, and internet usage.  
   - Summarize key metrics such as mean, variance, and standard deviation.  

4. **Hypothesis Testing**  
   - Compare average revenues between the Surf and Ultimate plans.  
   - Analyze revenue differences based on geographic regions.  

5. **Conclusion**  
   - Provide actionable insights to support Megaline’s advertising and pricing strategies.  

## Key Insights and Deliverables  
- Detailed analysis of user behavior for both plans.  
- Revenue comparisons with visualizations and descriptive statistics.  
- Hypothesis test results with clear explanations.  
- Recommendations for Megaline’s commercial strategy.  

## Requirements  
- **Software**: Jupyter Notebook, Python 3.x  
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`  

## How to Use  
1. Clone the repository.  
2. Open the Jupyter Notebook file in your preferred environment.  
3. Execute the cells step-by-step to reproduce the analysis.  
4. Review the outputs, visualizations, and conclusions at the end of the notebook.  

## License  
This project is for educational purposes and is not intended for commercial use.  
