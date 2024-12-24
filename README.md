# BUDGET TRACKING
### Video Demo: https://youtu.be/ZN55d1cl-cQ?si=vkP9xh4kLOf52jHw

Final project of CS50
This repository contains the code examples for the expense tracker
App requirements :
  user enters expense
  save expenses to CSV file
  summarise expense in total
  Show remaining budget


  "Expense" class: expense.py
    name
    category
    amount
  expense.py >> import >> App(expense_tracker.py)
**Ask for input**
      # Ask the user to add an expense.
    expense = get_expense()
    print(f"You've added {expense} to your expenses.")
    # Get user input for expense.
    expense = get_user_expense()
**Write to file**
      # Save the expense to a file.
    expenses = save_expense(expense)
    # Write their expense to a file.
    save_expense_to_file(expense, expense_file_path)
**Show Summary**
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
  
