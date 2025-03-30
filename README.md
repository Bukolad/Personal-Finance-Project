# Personal-Finance-Project
This project is a PowerBI dashboard analyzing financial transaction from an OPay Bank statement . The dashboard help track income , expenses, saving trends, and spending patterns to improve financial decison-making.
## Key Insights & KPIs
- Total Expenses : Breakdown of spending across different categories
- Net Savings : Differennce between income and expenses
- Top Expense Categories : Identifies major spending areas
- Income vs Expenses Trends : Monthly analysis of financial health
- Airtime & Data Spending : Airtime accounts 60.42%, while Data takes 39,58% of telecom expenses
- Saving Trends : Flunctuation in savings across different months
## Data Cleaning & Preparation 
- Step 1: Extracted from an OPay Bank Statement (PDF), Converted to Excel
- Step 2: Used Excel Power Query to structure and append multiple sheets
- Step 3: Load the dataset into PowerBI Power Query
- Step 4 : Seperated Debit and Credit transactions to ensure consistency
- Step 5 : Split Description column by Delimeter
- Step 6: Renamed Opay to ATM
- Step 7: New Measures were created to find Total Expenses
        Total Expenses : Total Debit = sum(Financial[Debit])
         Net Savings = [Total Credit] - [Total Debit]
          Total Transactions = COUNTROWS(filter(Financial,Financial[Debit] <> 0 || Financial[Credit] <> 0 ))
          Debit Transaction = countrows(FILTER(Financial,Financial[Debit] <> 0 ))
- Step 8
