# TaxCalculator GUI

Modern **CustomTkinter** desktop app for instant tax calculations.

## 🚀 Features
- ✅ Sleek CustomTkinter interface
- ✅ Real-time `Tax = Income × (Rate/100)` calculation
- ✅ Input validation & error handling
- ✅ Formatted output (€12,500.00)
- ✅ Fixed-size modern window (280x200)

## 📋 Quick Start

`bash
pip install customtkinter
python tax_calculator.py

🎮 Demo
Income:  50,000  | Percent: 25%  →  Tax: €12,500.00
Income:  1,234.56| Percent: 18.5% →  Tax: €228.39
Income:  abc      | Percent: 20%  →  Invalid input

📁 Screenshot Preview
[Income:     ] 
[Percent:    ] [25   ]
[Tax:        ] [€12,500.00] [Calculate]


🛠️ Technical Details
Formula: income * (tax_rate / 100)

Error Handling:
try:
    income = float(self.income_entry.get())
    tax_rate = float(self.tax_rate_entry.get())
except ValueError:
    self.update_result('Invalid input')


Layout: 2-column grid with consistent padding {padx: 20, pady: 10}

📊 Test Cases

| Input Valid? | Income  | Rate | Output        |
| ------------ | ------- | ---- | ------------- |
| ✅ Valid      | 50000   | 25   | €12,500.00    |
| ✅ Valid      | 1234.56 | 18.5 | €228.39       |
| ❌ Invalid    | abc     | 20   | Invalid input |
| ❌ Invalid    | 1000    | xyz  | Invalid input |


🔧 Customization
# Change currency
self.update_result(f'${income * (tax_rate / 100):,.2f}')

# Add tax brackets
if income > 100000: tax_rate *= 1.2  # Progressive tax


📦 Requirements
pip install customtkinter
Python 3.7+


🎯 Perfect For
Portfolio GUI projects

Tax calculation demos

CustomTkinter learning

Desktop app prototypes

📄 License
MIT License

