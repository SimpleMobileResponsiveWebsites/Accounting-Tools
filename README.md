# 📊 Financial Statements Explorer

**Learn, edit, and visualize the three core financial statements in one interactive Streamlit app.**

[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)](https://streamlit.io)
[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)](https://matplotlib.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#-license)

</div>

---

## 📖 Overview

**Financial Statements Explorer** is a hands-on teaching and planning tool. It walks you through the **Balance Sheet**, **Income Statement**, and **Cash Flow Statement**. Each one comes with a plain-English explanation, editable sample figures, an auto-generated table, and a chart that updates as you type.

It's a good fit for students, small-business owners, and anyone who wants to *see* how financial statements work instead of just reading about them.

---

## ✨ Features

- 🧾 **Three statements, three tabs.** The Balance Sheet, Income Statement, and Cash Flow Statement each get a clean tab.
- ✏️ **Fully editable sample data.** Change any number and every total, table, and chart recalculates instantly.
- ⚖️ **Automatic balance check.** The app confirms whether **Assets = Liabilities + Equity** and flags it if not.
- 💰 **Profitability status.** Net income is labeled as **Profit**, **Loss**, or **Break-even**.
- 💵 **Cash flow breakdown.** Operating, investing, and financing activities roll up to a net cash flow and an ending cash balance.
- 📅 **Custom dates and periods.** Set an "as of" date for the balance sheet and start/end periods for the other statements.
- 📈 **Color-coded bar charts.** Every statement gets a Matplotlib visualization.
- 🔗 **"How They Connect" section.** A short explanation shows how the three statements tie together.
- 🖥️ **Wide layout.** A roomy, dashboard-style page.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| [Streamlit](https://streamlit.io) | Interactive web UI, tabs, and inputs |
| [pandas](https://pandas.pydata.org) | Structuring statement data into tables |
| [Matplotlib](https://matplotlib.org) | Bar chart visualizations |
| Python `datetime` | Date and period inputs |

---

## 📁 Project Structure

financial-statements/ ├── app.py # The Streamlit application ├── requirements.txt # Python dependencies └── README.md # You are here

---

## ⚙️ Installation

**Prerequisites:** Python 3.9 or newer and `pip`.

```bash
# 1. Clone or download the project
git clone <your-repo-url> financial-statements
cd financial-statements

# 2. (Recommended) Create and activate a virtual environment
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# 3. Install dependencies
pip install streamlit pandas matplotlib

Or add a requirements.txt with the following:

text

…and install it with pip install -r requirements.txt.

🚀 Running the App
bash

streamlit run streamlit run app.py

Streamlit opens the app in your browser automatically, usually at http://localhost:8501.

🧭 Usage Guide
1️⃣ Balance Sheet
Pick an As of Date.
Enter Assets: Cash, Accounts Receivable, Inventory, Equipment.
Enter Liabilities: Accounts Payable, Loans.
Enter Equity: Owner's Capital, Retained Earnings.
Check the banner: ✅ green if the sheet balances, ❌ red if it doesn't.
2️⃣ Income Statement
Choose a Period Start and Period End.
Enter Revenue: Sales Revenue, Other Income.
Enter Expenses: Cost of Goods Sold, Rent, Salaries.
See whether the period shows a Profit, Loss, or Break-even result.
3️⃣ Cash Flow Statement
Set the cash flow period.
Enter Operating cash: sales received, payments to suppliers, operating expenses.
Enter Investing cash: equipment purchases.
Enter Financing cash: loans received, dividends paid.
Add a Beginning Cash Balance to see the Net Cash Flow and Ending Cash.
💡 Tip: The default values are set up so the sample Balance Sheet balances exactly ($26,000 = $10,000 + $16,000). Change one number and watch the balance check react.

🧮 Key Formulas
Statement	Formula
Balance Sheet	Assets = Liabilities + Equity
Income Statement	Net Income = Total Revenue − Total Expenses
Cash Flow	Net Cash Flow = Operations + Investing + Financing
Cash Flow	Ending Cash = Beginning Cash + Net Cash Flow
🔗 How the Statements Interconnect
mermaid
flowchart LR
    IS[Income Statement] -- Net Income --> RE[Retained Earnings]
    RE --> BS[Balance Sheet]
    CF[Cash Flow Statement] -- Ending Cash --> CASH[Cash]
    CASH --> BS
    BS -- Changes in assets & liabilities --> CF
Net Income from the Income Statement increases Retained Earnings on the Balance Sheet.
Ending Cash from the Cash Flow Statement matches Cash on the Balance Sheet.
Changes in assets and liabilities on the Balance Sheet often show up as cash flows on the Cash Flow Statement.
📸 Screenshots
Add your screenshots to a screenshots/ folder and update the paths below.

Balance Sheet	Income Statement	Cash Flow Statement
[Image blocked: Balance Sheet]	[Image blocked: Income Statement]	[Image blocked: Cash Flow Statement]
What you'll see: a tabbed page with editable number inputs grouped by section, a summary table for each statement, a colored status banner, and a bar chart (green, orange, blue, and purple) that updates live.

🗺️ Roadmap Ideas
 Link Net Income automatically into Retained Earnings
 Link Ending Cash automatically into Balance Sheet Cash
 Export statements to CSV, Excel, or PDF
 Save and load scenarios
 Ratio analysis (current ratio, profit margin, debt-to-equity)
