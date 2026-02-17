
<h1 align="center">loan-defaulter-dashboard_and_data</h1>


<img src="loan.jpg" alt="Project Screenshot" width="1100" height="200">

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
<p>
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
</p>

