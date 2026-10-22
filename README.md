# Bank Loan Analysis Project

## 📌 Project Overview
This repository contains a comprehensive **Bank Loan Analysis Dashboard** designed to monitor lending activities, track portfolio health, and support data-driven decision-making for financial institutions. The project bridges raw financial transactional data with actionable insights by evaluating key performance indicators (KPIs), monitoring trends over time, and segmenting borrower risks.

The end-to-end framework covers **database creation (MS SQL Server)**, **data cleaning and querying**, and **interactive report design (Power BI / Tableau)** to assess the bank's operational performance and credit risk patterns.

---

## 📊 Business Requirements & Key Metrics (KPIs)

To completely understand the lending landscape, the project monitors and calculates five primary operational KPIs:
1. **Total Loan Applications:** Total count of distinct loan applications received (MOM tracked).
2. **Total Funded Amount:** The overall capital disbursed by the bank as loans.
3. **Total Amount Received:** The total amount recovered/repaid by borrowers (principal + interest).
4. **Average Interest Rate:** The average cost of borrowing across all issued loans.
5. **Average Debt-to-Income (DTI) Ratio:** A risk metric checking the average borrower’s monthly debt obligations relative to their total income.

### 🛡️ Portfolio Health Segmentation
Loans are classified to evaluate credit risk mitigation:
*   **Good Loans (Fully Paid & Current):** Applications that are actively paying or have completely settled their accounts.
*   **Bad Loans (Charged Off):** Defaulted applications that present concrete financial risk and losses.

---

## 🛠️ Tech Stack & Tools Used
*   **Data Querying & Aggregation:** MS SQL Server / PostgreSQL (T-SQL Scripts provided)
*   **Business Intelligence & Visualization:** Power BI / Tableau Desktop
*   **Data Transformation:** Power Query (ETL pipeline inside Power BI)
*   **Analytical Computations:** DAX (Data Analysis Expressions) & SQL Functions
*   **Documentation & Version Control:** Git / GitHub

---

## 🗺️ Dashboard Architecture
The analytical report is broken down into three distinct visual lenses:

### 1. Summary Dashboard
Provides a macro-level financial health check. Includes KPI metric cards for applications, funding, and recovery, alongside a dedicated **Good Loan vs. Bad Loan** analysis framework showing concrete percentages and cash-flow splits.

### 2. Overview Dashboard
An interactive grid of charts showing multi-dimensional temporal and demographic correlations:
*   **Monthly Trends:** Visualizes seasonality in loan approvals and volume shifts (Line Chart).
*   **Regional Analysis:** Highlights state-wise lending density and distribution (Map/Bar Chart).
*   **Borrower Profile Analysis:** Tracks performance metrics against employment tenure, home ownership status, and loan intent (e.g., Debt Consolidation, Credit Cards).

### 3. Details Dashboard
A secure, filterable, low-level data grid providing granular details of individual transactions (including loan ID, sub-grades, loan terms, and specific payment histories) for deep-dive auditing.

---

## 📂 Project Structure
```text
├── Database/
│   ├── database_schema.sql       # Script to initialize tables and relationships
│   └── data_cleaning_queries.sql # Scripts handling nulls, formatting, and data validation
├── SQL_Queries/
│   ├── kpi_calculations.sql     # Individual queries tracking main KPI performance
│   └── insight_queries.sql      # SQL code written to answer specific business problems
├── Dashboards/
│   └── Bank_Loan_Report.pbix     # Completed Power BI Dashboard file
├── Data/
│   └── raw_loan_data.csv         # Publicly available sample financial dataset
└── README.md                     # Project documentation
```

---

## 📈 Key Insights Formulated
*   **Portfolio Status:** The portfolio registers roughly **86.2% Good Loans** versus **13.8% Bad Loans**, validating the standard baseline effectiveness of current credit checks.
*   **Top Purpose Driven Demand:** Borrowers overwhelmingly seek financing for **Debt Consolidation**, followed immediately by credit card refinancing.
*   **Risk Variables:** Higher interest rates showed a robust positive correlation with default rates, whereas the **DTI ratio** consistently outperformed annual income as an early-warning predictor for stressed accounts.

---

## 🚀 How to Run and Reproduce
1. **Database Setup:** Open your preferred SQL Server management tool, run the scripts found inside `Database/database_schema.sql`, and import the `raw_loan_data.csv` dataset.
2. **Execute Queries:** Run the scripts in the `SQL_Queries/` directory to verify metric calculations match the dashboard totals.
3. **Launch Dashboard:** Open `Dashboards/Bank_Loan_Report.pbix` using Power BI Desktop. Ensure you refresh or edit the data source credentials to target your local SQL Server instance.
