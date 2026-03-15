# Credit Risk Portfolio Analytics Dashboard

An interactive Power BI dashboard analysing credit risk patterns across a loan portfolio. Built to explore how credit grade, interest rate, and loan volume interact to drive default risk and expected portfolio loss.

## Dashboard Preview
![Credit Risk Dashboard](Dashboard.png)

## What It Shows

KPI Cards — 454 total loans, $7.06M total loan amount, 13.40% avg interest rate, 1.54% overall default rate.

Default Rate by Credit Grade — bar chart showing default rates across grades A to G. Grade D carries the highest default probability.

Total Loan Amount by Grade — Grade C has the largest loan exposure, followed by B and A.

Default Rate by Risk Category — breakdown across High Risk, Medium Risk, and Low Risk categories.

Interest Rate vs Default Probability by Credit Grade — scatter plot showing the relationship between interest rate and default probability per grade.

Expected Portfolio Loss by Grade — Grade D and B carry the highest expected losses.

Interactive Filters — filter the entire dashboard by Credit Grade (A–G) and Risk Category (High / Medium / Low Risk).

## Key Insight
Grade D exhibits the highest default probability and expected loss, while Grade C carries the largest exposure concentration. Risk is driven by both probability and loan volume distribution.

## Dataset
Sourced from Kaggle. Contains loan-level data including credit grade, loan amount, interest rate, and default status.

## How to Run
1. Download the `.pbix` file
2. Open in Power BI Desktop
3. Use the Credit Grade and Risk Category filters to explore the data

## Built With
Power BI, DAX

## Author
Rithika Harikrishna
[LinkedIn](https://linkedin.com/in/rithika-harikrishna) · [GitHub](https://github.com/rithikahaha)
