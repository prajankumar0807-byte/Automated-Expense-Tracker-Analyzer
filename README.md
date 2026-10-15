# 💰 Personal Expense Tracker & Spending Insights

A Python-based personal finance analysis tool that automatically categorizes bank transactions, analyzes monthly spending, identifies potential recurring expenses, and compares expenses against a predefined budget. It uses **Pandas, NumPy, Matplotlib, and Seaborn** to process transaction data and generate visual spending insights.

## 📌 Project Overview

Managing personal expenses is essential for maintaining financial stability. This project simplifies expense tracking by processing bank transaction CSV files and converting raw transaction data into meaningful financial reports.

The application normalizes transaction data, categorizes expenses using keyword-based rules, calculates monthly spending totals, analyzes category-wise spending, detects potential recurring transactions, and visualizes spending patterns.

## ✨ Features

- **CSV Data Import:** Loads transaction data from CSV files.
- **Data Cleaning & Normalization:** Standardizes column names and converts dates and amounts into appropriate data types.
- **Automatic Categorization:** Categorizes transactions into groceries, utilities, dining, transportation, entertainment, income, and other categories.
- **Monthly Spending Analysis:** Calculates total expenses for each month.
- **Budget Tracking:** Compares monthly expenses against a predefined budget and calculates the remaining budget or overspending.
- **Category-Wise Analysis:** Calculates spending totals and percentage shares for each category.
- **Recurring Expense Detection:** Identifies transactions with matching descriptions and amounts that occur more than once.
- **Data Visualization:** Generates charts showing monthly spending trends and category-wise expense distribution.
- **Sample Dataset:** Creates a demonstration CSV file to test the complete workflow.

## 🛠️ Technologies Used

- **Python** – Core programming language
- **Pandas** – Data loading, cleaning, grouping, and analysis
- **NumPy** – Numerical computing support
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical charts and visual styling

## 📂 Project Structure

```text
Personal-Expense-Tracker/
│
├── expense_tracker.py       # Main Python application
├── sample_expenses.csv      # Generated sample transaction data
├── README.md                # Project documentation
└── requirements.txt         # Required Python libraries
```

*Note: Save your Python program as `expense_tracker.py`. The sample CSV is generated automatically when the program runs.*

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

Replace the URL with your actual GitHub repository URL.

### 2. Navigate to the Project Directory

```bash
cd Personal-Expense-Tracker
```

### 3. Install the Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

Alternatively, create a `requirements.txt` file containing:

```text
pandas
numpy
matplotlib
seaborn
```

Then install the dependencies:

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
python expense_tracker.py
```

The application generates `sample_expenses.csv`, processes the transactions, displays spending summaries in the terminal, and opens charts for monthly spending and category distribution.

## 📊 Sample Analysis

The project uses sample transactions from January and February 2026.

The following information is generated:

**1. Monthly Spending Summary**
- Total expenses for each month
- Monthly budget
- Remaining budget or overspending

**2. Category Distribution**
- Total amount spent in each category
- Percentage contribution of each category to overall spending

**3. Potential Recurring Expenses**
- Transaction descriptions
- Matching transaction amounts
- Frequency of repeated transactions

**4. Visual Reports**
- Bar chart comparing monthly expenses with the budget
- Pie chart displaying category-wise spending distribution

## 💡 Example Budget Calculation

Suppose the monthly budget is $500 and the total expenses are $400.

- Monthly Budget: $500
- Total Expenses: $400
- Remaining Budget: $100
- Budget Status: Within Budget

If expenses exceed the budget, the report shows a negative budget variance, indicating overspending.

## 🧠 How It Works

1. **Load Data:** Reads transaction records from a CSV file using Pandas.
2. **Normalize Columns:** Converts column names into a standardized format and maps common bank CSV fields to the required schema.
3. **Clean Transactions:** Converts transaction dates and amounts and removes rows with invalid dates or amounts.
4. **Categorize Transactions:** Matches transaction descriptions against predefined keyword rules.
5. **Calculate Insights:** Groups expenses by month and category, calculates budget variance, and identifies repeated transactions.
6. **Generate Visualizations:** Displays charts to help users understand their spending patterns.

## 🔧 Customization

### Change the Monthly Budget

Update the budget value in the main program:

```python
generate_expense_insights(df_normalized, monthly_budget=500)
```

### Add New Category Keywords

Modify the `DEFAULT_CATEGORIES` dictionary to include more merchants or transaction keywords:

```python
DEFAULT_CATEGORIES = {
    "groceries": ["walmart", "kroger", "target"],
    "utilities": ["electric", "water", "internet"],
    "dining": ["restaurant", "cafe", "pizza"],
    "income": ["salary", "paycheck"]
}
```

You can add additional categories and keywords to suit your transaction data.

## 🚀 Future Enhancements

- Interactive dashboards using Streamlit or Plotly
- Support for Excel files and multiple bank statement formats
- Improved transaction categorization using machine learning
- Monthly and yearly financial reports
- Income-versus-expense analysis
- Savings goals and budget alerts
- Exportable PDF reports
- Improved recurring payment detection
- Support for multiple currencies

## ⚠️ Limitations

- Transaction categorization depends on predefined keywords and may misclassify unfamiliar descriptions.
- The recurring expense detector identifies matching descriptions and amounts, but does not verify actual billing schedules.
- The current analysis uses absolute transaction amounts for non-income categories, so refunds and transfers may be counted as expenses.
- The application uses a manually configured budget and does not connect directly to bank accounts.

## 🔒 Privacy & Security

This project processes CSV files locally and does not require bank account credentials or direct bank integration. Use sample or anonymized transaction data when testing, and avoid uploading personal financial information to a public repository.

## 🎓 Learning Outcomes

Through this project, developers can practice:

- Python programming and modular function design
- Data preprocessing and cleaning
- Pandas DataFrame operations
- Rule-based classification
- Financial data analysis
- Data visualization
- CSV file handling
- Git and GitHub project documentation

## 👨‍💻 Author

**Prajan Kumar M**

B.Tech Information Technology Student  
Mahendra Engineering College, Namakkal, Tamil Nadu, India

## 📄 License

This project is available for educational and learning purposes. You may add an MIT License if you want to permit broader reuse and modification under its terms.

---

⭐ If you find this project useful, consider giving the repository a star on GitHub.
