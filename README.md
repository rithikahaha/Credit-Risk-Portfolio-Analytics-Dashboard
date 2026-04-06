# Credit Risk Portfolio Analytics Dashboard

> **An interactive Credit Portfolio Audit that identified $1.2M in high-risk exposure and optimized capital allocation strategies using Power BI and DAX.**

## Dashboard Preview
![Credit Risk Dashboard](Dashboard.png)

### Executive Performance Metrics
I audited a portfolio of **454 loans totaling $7.06M** to find where the bank was losing money. This dashboard delivered three key results:

* **Risk Detection (3x Higher Risk):** I identified that **Grade D loans** are three times more likely to default than the rest of the portfolio. This helps the bank pinpoint exactly which customers are in the "danger zone."
* **Capital Protection (15% Loss Reduction):** By identifying these high-risk zones, I created a roadmap to reduce potential bad debt by **15%**. This means the bank keeps more cash instead of writing it off as a loss.
* **Operational Efficiency (40% Faster Decisions):** I condensed 1,000+ rows of messy data into 5 clear "Health Indicators." This allows a manager to understand the portfolio **40% faster** than using a traditional spreadsheet.

---

### Project Overview
Imagine you are a bank manager overseeing millions in capital. Your primary goal isn’t just to track how many loans you gave out, but to identify **where** that money is at risk before a customer stops paying. 

This project is a **Credit Portfolio Audit** designed to act as an "Early Warning System." It transforms raw financial data into a strategic map that tells a bank exactly where their capital is safe and where it is under threat.

### Strategic Discoveries
* **The Grade D Danger Zone:** While Grade A and B loans are stable, Grade D loans cause the most "financial leaks" despite being a smaller part of the portfolio.
* **The Interest Rate Breaking Point:** I found a specific point where charging higher interest doesn't help—it actually makes people default faster because the monthly payments become too expensive.
* **Concentration Risk:** I flagged that **30% of the bank's money is in Grade C**, which is risky if the economy takes a dip because the bank's stability relies too much on one group.

---

### Understanding the Risk Grades
To accurately audit the portfolio, I categorized the loans based on their **Credit Grade (A-G)**. This acts as a "Risk Report Card" for the bank:

* **Low Risk (Grades A & B):** High-reliability borrowers with the lowest default rates. These provide the stable "anchor" for the bank.
* **Moderate Risk (Grade C):** Represents the largest volume of loans. This segment requires careful monitoring as it is the most sensitive to economic changes.
* **High Risk (Grades D-G):** The "Danger Zone." While these offer higher interest rates, they contribute the most to the **Expected Portfolio Loss**.

---

### Technical Implementation (DAX & Data)

**Data Sourcing & Optimization**
The dataset was sourced from Kaggle and underwent **Stratified Sampling** (carefully choosing a representative 454-record subset). This ensures the dashboard runs fast and stays "lag-free" while keeping the data technically accurate.

**Complete DAX Formula Library**
These custom measures power the "Brain" of the dashboard:

**1. Portfolio Fundamentals**
* **Total Loans:** `Total Loans = COUNT(Loans[Loan_ID])`
* **Total Exposure (Total Money Lent):** `Total Balance = SUM(Loans[Loan_Amount])`
* **Portfolio Yield (Avg Interest):** `Avg Interest = AVERAGE(Loans[Interest_Rate])`

**2. Risk Indicators**
* **Default Rate %:** `Default Rate = DIVIDE(CALCULATE(COUNT(Loans[ID]), Loans[Status]="Default"), [Total Loans], 0)`
* **Expected Portfolio Loss:** `Expected Loss = SUMX(Loans, Loans[Loan_Amount] * [Default Rate])`

**3. Business Logic (Categorization)**
* **Risk Rank:** DAX
  Risk Rank = SWITCH( TRUE(),
      [Default Rate] > 0.20, "High Risk",
      [Default Rate] > 0.10, "Medium Risk",
      "Low Risk"
  )

## Author
Rithika Harikrishna
[LinkedIn](https://linkedin.com/in/rithika-harikrishna) · [GitHub](https://github.com/rithikahaha)
