# Credit Risk Portfolio Analytics Dashboard

An interactive Power BI dashboard analysing credit risk patterns across a loan portfolio. Built to explore how credit grade, interest rate, and loan volume interact to drive default risk and expected portfolio loss.

## Dashboard Preview
![Credit Risk Dashboard](Dashboard.png)

### What is this project?
Imagine you are a bank manager. You have lent out millions of dollars. Your biggest fear isn't just people not paying you back; it is not knowing **which** groups of people are most likely to fail. 

**LendGuard** is an interactive risk audit I built to hunt for patterns in loan defaults. It transforms raw financial data into a strategic map that tells a bank exactly where their money is safe and where it is at high risk.

### The Strategic Discovery: Where is the Money at Risk?
After auditing 454 loans totaling $7.06M, I identified a massive "Risk Gap" in the portfolio:

**The Grade D Danger Zone**
While Grade A and B loans are stable, **Grade D loans** show the highest default probability. Even though they represent a smaller portion of the total volume, they contribute the most to **Expected Portfolio Loss.**

**The Interest Rate Trap**
There is a clear "Breaking Point" where higher interest rates no longer compensate for the risk. My analysis shows that as interest rates cross a certain threshold, the default probability spikes aggressively, leading to a net loss for the bank.

**Concentration Risk**
Grade C carries the largest **Exposure Concentration.** If the economy dips, the bank’s stability relies almost entirely on the performance of this one specific group.

### How I Measured the Risk
I used Financial Analytics logic to calculate the **Expected Loss (EL)** for the portfolio:

$$Expected Loss = Exposure \times Probability of Default \times Loss Given Default$$

By mapping these variables, I created a **Risk Prioritization Map** that allows managers to see "at a glance" which loan categories need immediate policy changes.

### Tools & Methodology
* **Power BI & DAX:** I used DAX to create "Self-Healing" measures for Default Rates and Expected Loss.
* **Data Visualization:** Built with a "Mobile-First" executive layout to ensure a 5-second "Time-to-Insight."
* **Risk Categorization:** Developed a custom logic to sort loans into High, Medium, and Low risk buckets based on historical default patterns.

### Why this matters for a Financial Analyst?
In banking, data is money. This project proves I can do more than just build charts; I can analyze a portfolio to find **Systemic Risks** and provide the insights needed to protect a bank's capital.

### How to Explore the Audit
1. **Download the .pbix file** from this repository.
2. **Open in Power BI Desktop** to interact with the filters.
3. **Toggle Credit Grades** to see how the Expected Loss shifts in real-time.

## Author
Rithika Harikrishna
[LinkedIn](https://linkedin.com/in/rithika-harikrishna) · [GitHub](https://github.com/rithikahaha)
