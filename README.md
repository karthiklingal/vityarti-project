# python-project
Daily Expense Tracker
A simple, interactive command-line application to track your daily expenses. Add, view, and categorize your expenses, all stored in a text file for easy access.

Features
Add new expenses with date, amount, category, and description.

View all recorded expenses in a readable format.

How to Run
Make sure you have Python installed on your system.

Save the provided Python script as expense_tracker.py.

Open your terminal, navigate to the script location, and run:
python expense_tracker.py
Usage
Add Expense: Choose option 1, then follow prompts for date, amount, category, and description.

View Expenses: Choose option 2 to see a table of all expenses.

Exit: Choose option 3 to close the application.

How it Works
Expenses are saved to daily_expenses.txt in the script's directory.

File operations use the context manager (with open(...)) for safety and reliability.​

Error handling notifies the user if the expense file is missing.​

Notes
If the file daily_expenses.txt does not exist, it will be created automatically when you add your first expense.

You can always clear your expense history by deleting daily_expenses.txt.

        
       
        
