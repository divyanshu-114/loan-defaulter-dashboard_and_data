
<h1 align="center">loan-defaulter-dashboard_and_data</h1>


<img src="./Images/loan.jpg" alt="Project Screenshot" width="1100" height="200">

<h3>Dataset Description</h3>

<p>Banks earn a major revenue from lending loans. But it is often associated with risk. The borrower's may default on the loan. To mitigate this issue, the banks have decided to use Machine Learning to overcome this issue. They have collected past data on the loan borrowers & would like you to develop a strong ML Model to classify if any new borrower is likely to default or not.

The dataset is enormous & consists of multiple deteministic factors like borrowe's income, gender, loan pupose etc. The dataset is subject to strong multicollinearity & empty values. Can you overcome these factors & build a strong classifier to predict defaulters?
</p>
<hr width="100%">


<h3>Acknowledgements</h3>
<p>This dataset has been referred from Kaggle</p>
<hr width="100%">

<h3>Objective</h3>
<ul>
  <li>Understand the Dataset & cleanup (if required).</li>
  <li>Build classification model to predict whether the loan borrower will default or not.</li>
  <li>Also fine-tune the hyperparameters & compare evaluation metrics of various classification algorithms.</li>
</ul>
<hr width="100%">

<h2>Dataset Analysis Screenshots</h2>

<h2> File Details</h2>

<h3>Data Dictionary</h3>


| Column Name               | Data Type    | Category        | Description                    | Business Relevance               |
| ------------------------- | ------------ | --------------- | ------------------------------ | -------------------------------- |
| ID                        | Numeric      | Identifier      | Unique loan record ID          | Used to uniquely track each loan |
| year                      | Numeric      | Time            | Loan issuance year             | Used for trend analysis          |
| Gender                    | Categorical  | Demographic     | Gender of borrower             | Used for segmentation            |
| age                       | Numeric      | Demographic     | Age of borrower                | Age-based risk analysis          |
| Region                    | Categorical  | Demographic     | Geographic location            | Regional default analysis        |
| income                    | Numeric      | Financial       | Annual borrower income         | Measures repayment ability       |
| Credit_Score              | Numeric      | Credit Risk     | Borrower’s credit score        | Primary default predictor        |
| Credit_Worthiness         | Categorical  | Credit Risk     | Internal credit classification | Bank risk grading                |
| credit_type               | Categorical  | Credit Risk     | Type of borrower credit        | Credit exposure analysis         |
| co-applicant_credit_type  | Categorical  | Credit Risk     | Co-applicant credit type       | Additional risk indicator        |
| dtir1                     | Numeric      | Financial Risk  | Debt-to-Income ratio           | Financial burden indicator       |
| LTV                       | Numeric      | Financial Risk  | Loan-to-Value ratio            | Collateral risk indicator        |
| loan_amount               | Numeric      | Loan Details    | Approved loan amount           | Principal exposure               |
| loan_type                 | Categorical  | Loan Details    | Type of loan                   | Product risk comparison          |
| loan_purpose              | Categorical  | Loan Details    | Loan usage purpose             | Behavioral risk insight          |
| loan_limit                | Categorical  | Loan Details    | Loan limit category            | Lending threshold                |
| term                      | Numeric      | Loan Details    | Loan repayment duration        | Risk over time                   |
| rate_of_interest          | Numeric      | Loan Pricing    | Interest rate applied          | Profitability driver             |
| Interest_rate_spread      | Numeric      | Loan Pricing    | Spread over benchmark          | Margin indicator                 |
| Upfront_charges           | Numeric      | Loan Pricing    | Initial loan fees              | Revenue component                |
| Neg_ammortization         | Categorical  | Loan Structure  | Negative amortization flag     | Higher structural risk           |
| interest_only             | Categorical  | Loan Structure  | Interest-only payment option   | Increased repayment risk         |
| lump_sum_payment          | Categorical  | Loan Structure  | Lump-sum payment option        | Impacts repayment pattern        |
| property_value            | Numeric      | Collateral      | Market value of property       | Used in LTV calculation          |
| construction_type         | Categorical  | Property        | Property construction type     | Risk classification              |
| occupancy_type            | Categorical  | Property        | Owner or rental property       | Rental risk comparison           |
| Secured_by                | Categorical  | Collateral      | Type of loan security          | Collateral strength              |
| total_units               | Numeric      | Property        | Number of units in property    | Residential vs commercial risk   |
| Security_Type             | Categorical  | Collateral      | Security classification        | Risk segmentation                |
| approv_in_adv             | Categorical  | Application     | Pre-approval indicator         | Underwriting pathway             |
| submission_of_application | Categorical  | Application     | Application submission type    | Operational analysis             |
| open_credit               | Categorical  | Credit Profile  | Existing open credit lines     | Credit exposure measure          |
| business_or_commercial    | Categorical  | Loan Category   | Business/commercial loan flag  | Different risk segment           |
| Status                    | Binary (0/1) | Target Variable | Loan default outcome           | 1 = Default, 0 = Non-default     |

<hr width="100%">

<h2>File Details</h2>

The project is structured with the following directories, each serving a specific purpose in the data analysis pipeline:

- **`dashboard/`**: Contains the Tableau/Excel dashboard source file (`.csv`) used for visualization.
- **`report/`**: Includes the comprehensive project report in PDF format (`Section_E_G-7_Loan-default-analytics_report.pdf`).
- **`cleaned_dataset/`**: Houses the processed and cleaned dataset (`.csv`) along with documentation of cleaning steps (`cleaned.md`).
- **`calculations_pivot-table/`**: Contains pivot tables (`.csv`) used for deriving intermediate statistics and calculations.
- **`presentation/`**: Stores the project presentation materials.
- **`Images/`**: Contains assets like `loan.jpg` used in this README.
- **`raw_dataset/`**: (Implicit) Contains the original, unmodified dataset.

<hr width="100%">

<h2>Key Insights and Statistics</h2>

Based on the analysis of the dataset, here are some critical statistics:

### Risk Distribution
- **Total Loan Amount Analyzed**: ~$6.6 Billion
- **High Risk Loans**:
    - **Count**: 2,007
    - **Value**: $675,075,500
- **Low Risk Loans**:
    - **Count**: 15,150
    - **Value**: ~$5.2 Billion
- **Medium Risk Loans**:
    - **Count**: 2,843
    - **Value**: $728,249,500

### Demographics & Occupancy
- **Age Groups**: The **35-44** age group commands the highest total loan amount (~$1.67 Billion), while the **<25** group has the lowest ($45 Million).
- **Occupancy Type**: The vast majority of applicants fall under **Professional Role** (18,622), compared to **Independent** (977) and **Salaried** (401).

### Credit Analysis
- **Credit Score Ranges**: The average Interest Rate is relatively stable (~4.01% - 4.04%) across all credit score ranges (500-900).
- **Loan-to-Value (LTV)**: The **Central** region exhibits the highest average LTV (76.69%), while the **North-East** has the lowest (68.88%).

<hr width="100%">

<h2>Analysis and Suggestions</h2>

1.  **Risk Mitigation for High-Risk Segment**: While the "High Risk" category is smaller in volume (2,007 loans) compared to "Low Risk", it still represents a substantial financial exposure (~$675M). Stricter approval criteria or higher interest rate buffers could be considered for this segment.
2.  **Target Demographic**: The **Professional Role** segment is the dominant borrower profile. Marketing strategies and loan products should be specifically tailored to this group's needs and financial behaviors.
3.  **Regional adjustments**: The **Central** region's high Loan-to-Value ratio suggests a need for more cautious property valuation or lower lending limits in that specific geography to mitigate collateral risk.
4.  **Credit Score & Interest Rates**: The lack of significant variation in Interest Rates across Credit Score ranges (approx 4.03% flat) is unusual. Typically, higher scores should command lower rates. This pricing strategy should be reviewed to ensure it aligns with risk-based pricing models.

<hr width="100%">

<h2>Data Cleaning Notes</h2>

The following steps were taken to clean and prepare the dataset for analysis:

1.  **Cleaned Loan Limit Type**: Standardized categories.
2.  **Cleaned Approved_In_Adv**: Verified and corrected pre-approval flags.
3.  **Cleaned Loan_Type_Risk**: Rationalized risk categories.
4.  **Edited Credit_Worthiness**: Corrected inconsistencies in credit worthiness fields.
5.  **Fixed Loan_Purpose**: Standardized loan purpose descriptions.
6.  **Fixed Negative_Ammortization**: Corrected formatting for negative amortization flags.
7.  **Calculated Debt_to_Income_Ratio**: Derived DTI where missing or inconsistent.
8.  **Added Pivot Table**: Created a default column to facilitate pivot table creation.
9.  **Removed Redundant Columns**: Dropped `loan_type_risk` as it was duplicative.
10. **Parsed Income**: Converted income from text/string text format to numeric.
11. **Imputed Income**: Filled empty income values with the median income.
12. **Standardized Casing**: Ensured consistent capitalization across all columns.
13. **Imputed Ratios**: Filled missing values for ROI, IRS, and Upfront Charges with their respective medians.
14. **Filtered LTV**: Removed rows with blank Loan-to-Value ratios.
15. **Edited Gender**: Standardized gender categories.

<hr width="100%">

<h2>Dashboard Summaries</h2>

**Loan Default and Distribution Dashboard**

The dashboard provides a visual overview of the loan portfolio, focusing on:
- **Default Probability**: Visualizing the likelihood of default across different segments.
- **Risk Segmentation**: Breaking down the portfolio by High, Medium, and Low risk categories.
- **Demographic Analysis**: Interactive slicers to filter data by Age, Gender, Income, and Region.
- **Financial Metrics**: Tracking key metrics like Loan Amount, LTV, and Interest Rate spreads.

The dashboard serves as a tool for quick decision-making and identifying trends in the loan applicant pool.


