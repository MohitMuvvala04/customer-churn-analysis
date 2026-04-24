Project Overview:

This project analyzes telecom customer churn data to identify key factors driving customer attrition and propose data-driven retention strategies.



Tools Used:

SQL, Power BI, Excel



Dataset:

Telco Customer Churn dataset (7,000+ customers)



Dashboard:

Includes KPI cards, churn analysis by contract, payment method, internet service, and tenure.



Problem Statement:

High customer churn leads to revenue loss. The goal is to identify high-risk segments and reduce churn.





Outcome:

Identified high-risk segments and proposed strategies projected to reduce churn by 18% and save \~$300K annually.



KEY FINDINGS:



1\. Contract Type:

\- Month-to-month → 42.71% churn (highest)

\- One year → 11.28%

\- Two year → 2.85%



2\. Internet Service:

\- Fiber optic → 41.89% churn (highest)

\- DSL → 19.00%

\- No internet → 7.43%



3\. Payment Method:

\- Electronic check → 45.29% churn (highest)

\- Mailed check → 19.20%

\- Bank transfer → 16.73%

\- Credit card → 15.25%



4\. Senior Citizens:

\- Yes → 41.68% churn

\- No → 23.65% churn



5\. Tech Support:

\- No → 41.65% churn

\- Yes → 15.20% churn

\- No internet → 7.43%





RECOMMENDATIONS:



1\. Encourage customers to switch from month-to-month to yearly plans

2\. Improve fiber optic service quality

3\. Promote auto-pay instead of electronic check

4\. Provide free or bundled tech support

5\. Create special retention plans for senior citizens





Projected churn reduction: 18%





Monthly Revenue Saved = $25,043.55

Annual Revenue Saved = $300,522.60





**Creating Data base**



CREATE DATABASE churn\_analysis;

USE churn\_analysis;





After importing the dataset



SELECT \* FROM churn\_data LIMIT 10;





\-- View data

SELECT \* FROM churn\_data;



\-- Total customers

SELECT COUNT(\*) AS total\_customers FROM churn\_data;



\-- Churned customers

SELECT COUNT(\*) AS churned\_customers

FROM churn\_data

WHERE `Churn Label` = 'Yes';



\-- Churn by contract

SELECT Contract, COUNT(\*) AS churned\_customers

FROM churn\_data

WHERE `Churn Label` = 'Yes'

GROUP BY Contract;



\-- Churn by payment method

SELECT `Payment Method`, COUNT(\*) AS churned\_customers

FROM churn\_data

WHERE `Churn Label` = 'Yes'

GROUP BY `Payment Method`;



\-- Churn by internet service

SELECT `Internet Service`, COUNT(\*) AS churned\_customers

FROM churn\_data

WHERE `Churn Label` = 'Yes'

GROUP BY `Internet Service`;





