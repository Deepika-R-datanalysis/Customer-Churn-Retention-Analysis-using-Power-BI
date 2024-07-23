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
6. Transform data to add conditional column for the tenure .

DATA VISUALIZATION:

  Customer Churn - Retention Analysis Dashboard:
  
1. Card representation to display KPI counts .
2. Stacked bar chart to show how the contract tenure affects the churn.
3. Stacked column chart to show if senior citizens affected churn more.
4. Doughnut chart to show the Churn Rate and Retention Rate.
5. Clustered Bar chart to show the churn count of customers.
   
   Other Metrics DAshboard :
   
1. Clustered Bar chart to show which type of internet service faced more churn.
2. Stacked column chart with drill down function to see the churn vs products opted like(Online backup ,online security,tech support, Device protection,streaming tv ,streaming movies).
3. Stacked Column Chart to show dependents vs Churn
4. Cards to display count of tickets raised,total amount charged

INSIGHTS:

As shown in the data Visualization, It can be deduced that:

7043 are the total customers . The churn rate is 27% and Retention rate is 73 %
Customers on the Year contract, have been with the company for long, while most of the customers on Month-to-Month contract increased the churn.
The company is at risk of losing recently joined customers. 
Yearly charges is $16.06M charges and Monthly Charges is $456.12K
2955 tech tickets were opened and 3632 admin tickets were opened.
Most of the churned customers did not sign up for Online Security and tech support and also did not sign up for Phone Services.
A lot of customers had an issue with Fiber Optics . 

RECOMMENDATION:

From analysis, majority of customers on monthly contracts increased churn.
The Company can try convincing customers to subscribe to Yearly contracts by giving discounts.
Also majority customers who churned did not sign up for Online Security and Tech Support. 
Customers age or having dependents din't impact churn much .
Retention Rate if we try can be increased by suggesting plans and theri savings on yearly contract than monthly contract.


