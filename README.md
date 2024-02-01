# CREDITCARD-LAUNCH-ANALYTICS

## **Project Overview:**

Mitron Bank is a legacy financial institution headquartered in Hyderabad. They want to introduce a new line of credit cards, aiming to broaden its product offerings and reach in the financial market.

AtliQ Data Services aquired the pilot project provided with the sample dataset of 4000 customers across five cities on their online spend and other details. AtliQ Data Services aims to provide actionable insights guiding the customization of credit cards based on customer needs and market trends.


_[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiNDA3MTk5YTgtNGI2NC00NWFiLWE0YTUtMDQ0NzhiODA0ZWQ2IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)_

## **Tools used:**

- Microsoft Excel
- Power BI

## **Task List:**

As a data analyst who has been provided with sample data need to accomplish step by step tasks and conduct analysis mentioned below to acheive the required data driven insights and recomandations.

- Explore basic statistics and distribution of key variables.
- Analyze the distribution of customers across age groups, cities, occupations, genders, and marital status and identify any patterns or trends.
- Examine spending patterns across different months, categories, and payment types.
- Identify popular spending categories and peak spending months.
- Identify customer segments with high online spending.
- Determine the correlation between age group, income, and spending.
- Analyze spending patterns across different cities. Identify potential cities for targeted credit card promotions.

## **Datasets:**
- Dim_customer: contains Customer details, such as customer ID, gender, city, age group, average income (for a period of 6 months), marital status, and occupation.
- Fact_spend: Details about spending behavior, including customer ID, spending month, payment type, spending, and spending category.

## **Key metrics:**

- Total Customers
- Total Income
- Total Spendings
- Total Average Income
- Average Income Monthly
- Average Spends Monthly
- Average Income Utilization %
- Credit card spends
- Credit card spends%

## *Problem Understanding and Dataset Review:*
Before diving into data analysis, it's crucial to fully understand the problem statement we aim to address. Carefully reviewing the dataset is essential to ensure accurate and meaningful insights.

## *Data Cleaning and Transformation:*
- Checked for null and duplicate values in the dataset.
- Created a average spends custom column for dim_customers table ([total_spending]/6).
= Created dim_month table to produce dynamic calculations and measures. 
## *3. Data Modeling:*

<img width="337" alt="Screenshot 2024-02-01 131055" src="https://github.com/AkhilMusuloju/CREDITCARD-LAUNCH-ANALYTICS/assets/142907602/3250726d-a496-45c1-8791-8fa5d70ff89c">

## *Defining KPIs and Other Metrics:*

- Creted Measure Total_Avg_spends = Divide ( total_spends,6,0)
  
- Created a measure for average income utilization:
  Avg_income_utilization% = DIVIDE([Total_Avg_spends], [Total_Avg_Income], 0).

- Created a measure for Total Credit Card Spending:
  TotalCreditCardSpending =
   CALCULATE(
   [total_spending],
  fact_spends[payment_type] = "Credit Card"
  ).
- Created a measure for CC%:
  CC% = [TotalCreditCardSpending]/[total_spending].

## *Data Visualization:*

  Demographic Analysis
  
<img width="574" alt="Demographic Analysis" src="https://github.com/AkhilMusuloju/CREDITCARD-LAUNCH-ANALYTICS/assets/142907602/4e262137-c8fe-420b-938d-b734217e78e3">

  Expenditure Analysis
  
<img width="575" alt="Expenditure Analysis" src="https://github.com/AkhilMusuloju/CREDITCARD-LAUNCH-ANALYTICS/assets/142907602/a8d81fa7-33bf-45ed-9713-3698eb8e6b57">

## *Enhanced User Interactivity:*

Added page navigation to navigate between the two dashboards seamlessly.



