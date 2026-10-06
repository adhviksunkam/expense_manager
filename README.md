# Expense Manager

A desktop expense tracking application built with **Python** and **Tkinter**, developed as a first-semester team project at **PES University** (Python "Jackfruit" project).

The app helps users record daily expenses, review them in a table, calculate annual savings, and visualize spending by category with a pie chart.

> 📄 **For the full technical report** (architecture, design decisions, challenges faced, and sample screenshots), please refer to [`document.pdf`](document.pdf) in this repository.

---

## Features

- **Add expenses** with date, item name, amount, and category
- **Category dropdown** (Rent, Food, Transportation, Fees, Personal, Medicines, Clothes, Other) to keep entries consistent
- **View all expenses** in a table (Treeview) with a refresh option
- **Delete** selected expenses
- **Annual savings calculator** that compares annual income with total expenses, showing savings in green (positive) or red (negative)
- **Expense pie chart** showing percentage spending by category, built with Matplotlib
- **Input validation** with user-friendly error messages for empty or invalid fields
- **Persistent storage** in a CSV file, so data is saved between sessions

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| Language | Python 3 |
| GUI | Tkinter / ttk |
| Charts | Matplotlib |
| Storage | CSV file |

---

## Project Structure

```
expense_manager/
├── main.py         # App controller: manages screens and navigation
├── backend.py      # Data layer: initialize, save, load, and delete expenses
├── add_ui.py       # "Add New Expense" screen
├── view_ui.py      # "View, Delete & Analyze" screen (table, savings, pie chart)
├── expenses.csv    # Stored expense data
└── document.pdf    # Full project report
```

**Design approach:** The backend is kept separate from the user interface, so data handling is independent of the screens. The UI uses a stacked-frame pattern, where all screens are created at startup and switched using `tkraise()`.

---

## How to Run

1. Make sure **Python 3** is installed.
2. Install the required library:
```bash
   pip install matplotlib
```
3. Clone or download this repository, then run:
```bash
   python main.py
```

Tkinter comes bundled with most Python installations.

---

## How It Works

1. **Home screen:** choose Add New Expense, View Expenses, or Exit.
2. **Add screen:** enter the date (YYYY-MM-DD), item, amount, and pick a category. Click Save Expense.
3. **View screen:** see all expenses, delete selected ones, enter your annual income to calculate savings, or click Show Expense Chart for the category-wise pie chart.

Sample screenshots of each screen are included in [`document.pdf`](document.pdf).

---

## Team

This project was built collaboratively by:

- S. Adhvik
- Preetam R C
- Rohitsamartha B
- Rohan C H

**Guided by:** Teja I ma'am, PES University

### My Contributions
Worked on the view and delete screen and the CSV handling in backend.py

---

## Challenges and Learnings

- Handling CSV reads, appends, and deletions without corrupting data
- Keeping the table in sync with the file after every change
- Validating user input to prevent crashes
- Aggregating transactions by category for meaningful charts
- Working as a team and dividing a project into modules

More detail on each of these is in [`document.pdf`](document.pdf).

---





## References

- Python Software Foundation, *Tkinter, csv, and os documentation*
- J. D. Hunter, *Matplotlib: A 2D Graphics Environment*, 2007
