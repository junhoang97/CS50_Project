#### BUDGET TRACKING
#### Video Demo: https://youtu.be/ZN55d1cl-cQ?si=RBXk43OYCdkp0zpr
This is my final project for CS50. It is a budget tracking application designed to help users manage their finances more efficiently. With this app, users can input various expenses, save them to a CSV file, and get a summary of their spending. The application provides useful features such as categorizing expenses, calculating the total expenses, estimating the remaining budget, and offering a daily spending limit based on the remaining funds.

App Features:
The main features of the app are focused on simplifying budget management. Here are the key aspects of the app:

User Input: Users can easily input their expenses. The application allows them to provide details such as the name of the expense (e.g., "Groceries"), the category (e.g., "Food"), and the amount spent (e.g., "$50.00").
Save Expenses: After the user inputs the expense, the app automatically saves it to a CSV file. This ensures that all expenses are securely stored and can be accessed at any time.
Summarize Expenses: The app provides a summary of the total expenses entered by the user. This summary includes the total amount spent, along with the remaining budget, which helps users keep track of their financial situation.
Expense Categories: Expenses are categorized to provide users with better organization. Categories like "Food", "Entertainment", "Transportation", and "Utilities" allow users to easily see where their money is going.
Daily Budget Estimate: Based on the remaining budget, the app estimates how much the user can spend per day in order to stay within their budget limits.
File Structure:
The application is organized into two main files:

expense.py: This file defines the Expense class. The class includes attributes like name, category, and amount to capture the essential details of an expense. Methods within the class allow users to create and manage individual expenses.
expense_tracker.py: This is the main application file. It handles user input, saving expenses, and generating summaries. It also includes logic to read data from the CSV file, categorize expenses, and provide the daily budget estimate.
How the App Works:
Adding an Expense:
When the user starts the application, they are prompted to add an expense. The application will ask for the following inputs:

Expense Name: A short description of the expense (e.g., "Groceries").
Expense Category: The category to which the expense belongs (e.g., "Food").
Expense Amount: The amount of money spent on the expense (e.g., "$50.00").
Once the user provides this information, the application will automatically save the expense to a CSV file for future reference. Here is an example of how the app processes this information:

python
Copy code
# Ask the user to add an expense.
expense = get_expense()
print(f"You've added {expense} to your expenses.")

# Get user input for expense.
expense = get_user_expense()
# Save the expense to a file.
expenses = save_expense(expense)

# Write the expense to a file.
save_expense_to_file(expense, expense_file_path)
# Show the user the current expense breakdown.
number_of_expenses = len(expenses)
total_expenses = sum([expense.amount for expense in expenses])
print(f"You have {number_of_expenses} expenses totalling ${total_expenses:.2f}.")
Summarizing Expenses:
After adding expenses, the app provides a detailed summary. The summary includes:

The total amount of expenses entered so far.
A breakdown of the expenses by category.
An estimation of how much money remains in the budget.
python
Copy code
# Read file and summarize expenses.
summarize_expenses(expense_file_path, budget)

# Show expenses by category.
show_expense_by_category(expenses)
Daily Budget Estimate:
The application calculates the remaining budget and estimates how much the user can spend per day. This helps the user manage their finances effectively by ensuring they don’t overspend before the end of the month.

python
Copy code
# Show the user a rough estimate of how much they have left to spend per day.
show_budget(total_expenses)
Installation and Setup:
To get the application running on your local machine, follow these steps:

Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/budget-tracking.git
Install dependencies (if applicable): If your project has any external dependencies (e.g., third-party libraries), you can install them by running:

bash
Copy code
pip install -r requirements.txt
Run the application: You can now run the application by executing:

bash
Copy code
python expense_tracker.py
Conclusion:
The Budget Tracking app provides a simple yet effective way to manage your finances. Whether you're trying to cut back on spending or just stay within your budget, this app helps by tracking your expenses, categorizing them, and offering a daily spending estimate. By saving expenses to a CSV file, you can easily access and review your spending patterns anytime.
