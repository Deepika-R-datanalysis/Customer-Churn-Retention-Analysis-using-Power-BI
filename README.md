# Customer-Churn-Retention-Analysis-using-Power-BI
PWC Virtual Internship Program

In this project we will do the following :

Define proper KPI's
Using Power BI ,we will create a dashboard for the retention manager reflecting the KPI's 
Find the customers who left within the last month
Find the retention rate and churn rate using the churn dataset . 
Write a short email to him (the engagement partner) explaining the findings, and including suggestions as to what needs to be changed

We will use DAX functions in Power BI


DATA CLEANING :

Check the dataset for nulls and duplicate rows .
Check the datatype 
Create a duplicate column for churn as churn-copy and replace values of yes to 1 and No to 0 (to ease our calculation ) and change type to whole number.

DATA ANALYSIS:

New Measures created using power quesry window:

1. Distinct count of customers = DISTINCTCOUNT('01 Churn-Dataset (2)'[customerID])
2. Churn Count = SUM('01 Churn-Dataset (2)'[Churn - Copy])
3. Retained customers count = (DISTINCTCOUNT('01 Churn-Dataset (2)'[customerID])- SUM('01 Churn-Dataset (2)'[Churn - Copy]))
4. Retention Rate = CALCULATE([Retained customers count]/[Distinct count of customers])*100
5. Churn Rate = CALCULATE('01 Churn-Dataset (2)'[Churn Count]/[Distinct count of customers])*100

DATA VISUALIZATION:

1. Card representation to display KPI counts .
2. Stacked bar chart to show how the contract tenure affects the churn.
3. Stacked column chart to show if senior citizens affected churn more.
4. Doughnut chart to show the Churn Rate and Retention Rate.
5. Clustered Bar chart to shpw the churn count of customers.


