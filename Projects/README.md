📌 Project Title
Personal Budget Tracker (Python)

1️⃣ Purpose & Scope
The system tracks income and expenses, categorizes expenses, and calculates totals and remaining budget for a given period (monthly by default).
The program should:

-Record expenses with categories
-Calculate totals per category
-Track income
-Show remaining balance
-Generate simple summaries

2️⃣ Functional Requirements
2.1 Add Income

-User can add income entries
-Each income has:
    -Amount
    -Source (e.g., Salary, Freelance)
    -Date
###
Example
Add income: R12,000 from Salary on 2026-02-01
###
2.2 Add Expense
-User can add an expense
-Each expense has:
    -Amount
    -Category
    -Description
    -Date
###
Example Categories
-Food
-Transport
-Rent
-Utilities
-Entertainment
-Education
-Health
-Other
###

2.3 Categorize Expenses
-Each expense must belong to exactly one category
-Categories should be predefined but extendable
-System automatically groups expenses by category

2.4 Budget Limits (Optional but Recommended)
-User can set a monthly limit per category
###
Example
Food: R3,000
Transport: R1,200
###

-System warns user when:
    -80% of limit is reached
    -Limit is exceeded

2.5 Calculations
The system must calculate:
-Total income
-Total expenses
-Remaining balance
-Total spending per category
-Percentage spent per category

2.6 Reports / Output
The program should be able to display:
-Summary report
-Category breakdown
-Over-budget categories
###
Example Output
Total Income: R12,000
Total Expenses: R7,450
Remaining Balance: R4,550

Food: R2,300 (76%)
Transport: R900 (75%)
Rent: R3,500 (100%)
###

3️⃣ Non-Functional Requirements
3.1 Usability
-Command-line interface (CLI)
-Clear prompts and error messages
-Input validation (no negative amounts)

3.2 Performance
-Must handle at least 1,000 expense records efficiently

3.3 Maintainability
-Modular design (separate files or classes)
-Clear function naming and docstrings

4️⃣ Data Model (Suggested)
4.1 Expense Object
Expense:
    amount: float
    category: str
    description: str
    date: datetime

4.2 Income Object
Income:
    amount: float
    source: str
    date: datetime


5️⃣ System Architecture
5.1 Core Modules
budget_tracker/
│
├── main.py                 # Program entry point
├── expense.py              # Expense class
├── income.py               # Income class
├── budget_manager.py       # Core logic
├── reports.py              # Summaries & analytics
└── data_storage.py         # File handling (CSV / JSON)


6️⃣ Data Storage Requirements
Option 1: JSON (Beginner-Friendly)
{
  "income": [],
  "expenses": [],
  "budgets": {}
}

Option 2: CSV (Simple, Spreadsheet Compatible)
-income.csv
-expenses.csv

7️⃣ Key Functions (Minimum)
add_income(amount, source, date)
add_expense(amount, category, description, date)
get_total_income()
get_total_expenses()
get_expenses_by_category()
get_remaining_balance()
generate_summary_report()


8️⃣ Error Handling Rules
-Reject negative values
-Reject unknown categories
-Handle empty datasets gracefully
-Validate date format (YYYY-MM-DD)


9️⃣ Future Extensions (Optional)
-Monthly filtering
-Graphs using matplotlib
-Export reports to CSV/PDF
-GUI using Tkinter or web app using Flask


🔟 Success Criteria
The system is considered complete if:
-Expenses are correctly categorized
-Totals and balances are accurate
-Reports clearly show spending behavior
-Code is modular and readable


<!-- If you want, I can:


Turn this into pseudocode


Design OOP class diagrams


Write a starter implementation


Help you add data visualization


Just tell me what level you want 🚀 -->