# BUDGET TRACKING

### Video Demo: [Watch the Demo](https://youtu.be/ZN55d1cl-cQ?si=vkP9xh4kLOf52jHw)

This is my final project for CS50. It is a budget tracking application that helps users manage their expenses. The application allows users to add expenses, save them to a CSV file, and provides summaries including the total expenses and remaining budget.

## App Features
- User Input: Allows the user to input their expenses.
- Save Expenses: Stores the entered expenses in a CSV file.
- Summarize Expenses: Displays a summary of all expenses, including total expenses and remaining budget.
- Expense Categories: Categorizes expenses for better organization.
- Daily Budget Estimate: Shows an estimate of how much the user can spend per day based on their remaining budget.

## File Structure
- `expense.py`: Defines the `Expense` class with attributes such as `name`, `category`, and `amount`.
- `expense_tracker.py`: The main application file that handles user input, saving expenses, and showing summaries.

## How the App Works

### Adding an Expense:
```python
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

# Read file and summarize expenses.
summarize_expenses(expense_file_path, budget)

# Show expenses by category.
show_expense_by_category(expenses)

# Show the user a rough estimate of how much they have left to spend per day.
show_budget(total_expenses)


