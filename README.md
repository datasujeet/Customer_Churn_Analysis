# Customer Churn Analysis

## Project Overview
This repository contains an exploratory data analysis (EDA) of a telecommunications customer churn dataset, aimed at identifying factors influencing customer retention and churn. The dataset includes 7,043 customer records with 21 attributes, covering demographics, service subscriptions, billing details, and churn status. The analysis, performed using Python (Pandas, Matplotlib, Seaborn), focuses on data cleaning, statistical insights, and visualizations to uncover patterns, particularly around payment methods and their impact on churn.

## Dataset
- **Source**: The dataset (`Customer Churn.csv`) contains customer data from a telecommunications company.
- **Attributes**: 21 columns, including:
  - `customerID`: Unique customer identifier
  - `gender`, `SeniorCitizen`, `Partner`, `Dependents`: Demographic details
  - `tenure`, `PhoneService`, `MultipleLines`, `InternetService`, etc.: Service subscriptions
  - `MonthlyCharges`, `TotalCharges`, `PaymentMethod`, `Contract`: Billing information
  - `Churn`: Target variable (Yes/No)
- **Size**: 7,043 rows, no missing values, no duplicates.

## Analysis Summary
The EDA was conducted in a Jupyter Notebook (`Chrun_Customer_analysis_EDA.ipynb`) and includes the following key components:

### Data Preparation
- **Cleaning**:
  - Replaced blank values in `TotalCharges` with 0 and converted to float.
  - Transformed `SeniorCitizen` from binary (0/1) to categorical ("No"/"Yes").
  - Verified no missing values or duplicates.
- **Statistical Insights**:
  - Mean tenure: 32.37 months (range: 0–72).
  - Mean monthly charges: $64.76 (range: $18.25–$118.75).
  - Mean total charges: $2,279.73 (range: $0–$8,684.80).
  - Churn rate: 26.54% (1,869 churned, 5,174 retained).

### Key Findings
- **Churn by Payment Method**:
  - Visualized using a Seaborn count plot with churn rates:
    - **Electronic check**: 44.99% churn rate (1,076/2,371).
    - **Mailed check**: 18.70% churn rate (308/1,612).
    - **Bank transfer (automatic)**: 16.77% churn rate (258/1,543).
    - **Credit card (automatic)**: 15.30% churn rate (233/1,523).
  - **Insight**: Customers using electronic checks are significantly more likely to churn, suggesting potential issues with this payment method. Automatic payment methods (bank transfer, credit card) correlate with higher retention.

### Visualizations
- A count plot illustrates churn distribution by payment method, with bar labels for clarity and rotated x-axis labels for readability.
- The visualization highlights the high churn rate for electronic check users, providing a clear visual cue for further investigation.

## Repository Structure
├── Customer Churn.csv              # Dataset <br>
├── Chrun_Customer_analysis_EDA.ipynb # Jupyter Notebook with EDA <br>
├── README.md                       # This file

## 🖼️ Screenshots

| Customer Churn Analysis | Categorical Feature Distribution |
|---------|-----------|
| ![Customer Churn Analysis](https://github.com/datasujeet/Customer_Churn_Analysis/blob/main/tca.png) | ![Categorical Feature Distribution](https://github.com/datasujeet/Customer_Churn_Analysis/blob/main/Subplots.png) 


## Key Insights
- **Payment Method Impact**: Electronic check users have a 44.99% churn rate, nearly three times higher than automatic payment methods (15.30%–16.77%). This suggests operational or experiential issues with electronic checks.
- **Retention Opportunity**: Promoting automatic payment methods could reduce churn, as they are associated with lower churn rates.
- **Data Quality**: The dataset is clean and ready for advanced analyses, such as predictive modeling.

## Future Work
- **Additional Visualizations**: Explore churn by contract type, tenure, or internet service using plots like box plots or histograms.
- **Statistical Tests**: Perform chi-square tests for categorical variables (e.g., `PaymentMethod`) and t-tests for numerical variables (e.g., `MonthlyCharges`) to validate findings.
- **Predictive Modeling**: Build machine learning models (e.g., logistic regression, random forests) to predict churn and quantify feature importance.
- **Customer Segmentation**: Segment customers by tenure and payment method to design targeted retention strategies.

## Recommendations
- **Investigate Electronic Checks**: Analyze transaction failures or customer feedback to address high churn rates.
- **Promote Automatic Payments**: Offer incentives to encourage adoption of bank transfers or credit cards.
- **Enhance Retention Strategies**: Target electronic check users with personalized support or discounts to improve retention.

- ## 🔗 Connect with Me

- **LinkedIn**: [LinkedIn Profile](https://www.linkedin.com/in/sujeetdatascience1/)
- **Email**: data.sujeet@gmail.com
