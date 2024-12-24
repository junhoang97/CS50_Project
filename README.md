BUDGET TRACKING
Video Demo: [https://youtu.be/ZN55d1cl-cQ?si=RBXk43OYCdkp0zpr](https://youtu.be/ZN55d1cl-cQ?si=XmKcOsJ6fqO6mbAZ)
Cause: Managing personal finances is a crucial aspect of financial well-being, but it’s something that many people struggle with. The ability to keep track of where money is spent, budget appropriately, and set goals for saving is vital to achieving long-term financial health. In today's fast-paced world, many individuals fail to track their spending effectively due to busy schedules or lack of proper tools. That’s where my Budget Tracking application comes in. The goal of this project is to help people better manage their money and stay on top of their financial goals by offering a simple, easy-to-use tool for expense tracking.

Description: This is my final project for CS50, and it is a comprehensive budget tracking application designed to assist users in managing their expenses. The application provides a user-friendly interface for inputting expenses, storing them in a CSV file, and generating insightful reports on total expenses and remaining budgets. Additionally, the app categorizes expenses for easy tracking and provides users with an estimate of how much they can spend daily based on their remaining budget. The core objective of this project is to help users better understand their spending habits and gain control over their finances in a way that is both practical and accessible.

App Features
The Budget Tracking application is designed with several key features to provide users with an effective way to track and manage their expenses:

User Input: This feature allows users to input details of their expenses, including the name of the expense (e.g., "Groceries"), category (e.g., "Food"), and the amount spent (e.g., "$50.00"). The application provides an intuitive form for entering this information, making it simple for even those who are not tech-savvy to use. The goal is to make the process of expense tracking as straightforward as possible so that users are encouraged to enter their expenses regularly.

Save Expenses: Once the user enters an expense, the app saves it to a CSV file, ensuring that all data is preserved for future reference. This feature helps users keep an accurate and up-to-date record of their financial activity. The CSV format is widely supported and can be opened with various programs, making it a convenient way to store data.

Summarize Expenses: The app generates summaries that include the total amount of money spent and the remaining budget. These summaries are calculated automatically, providing the user with instant feedback on their financial situation. By looking at these summaries, users can easily see whether they are staying within their budget and adjust their spending habits accordingly.

Expense Categories: One of the key features of this application is its ability to categorize expenses into different groups. Categories such as "Food", "Entertainment", "Transportation", "Bills", and "Others" allow users to quickly see how much money they are spending in each area. This categorization provides better organization and helps users identify areas where they may need to cut back on spending.

Daily Budget Estimate: Another useful feature is the daily budget estimate. Based on the user’s remaining budget, the app calculates how much they can spend per day to stay on track. This is particularly useful for users who struggle with overspending or those who want to ensure they don’t deplete their budget too early in the month. By providing a daily estimate, the app helps users pace their spending and make informed financial decisions.

File Structure
The application is divided into two main files, each with specific responsibilities:

expense.py: This file defines the Expense class, which encapsulates all the attributes related to an expense. The class includes attributes such as the name, category, and amount of the expense, as well as methods for interacting with expense data. The Expense class is central to the application, as it stores and manages the data entered by the user.

expense_tracker.py: This is the main file that runs the application. It contains the core logic for interacting with the user, saving expenses, and summarizing the data. This file handles tasks such as asking the user for input, writing expenses to the CSV file, reading the file to generate summaries, and displaying the results. It also interacts with the Expense class to create and manage individual expense objects.

How the App Works
Here is a step-by-step breakdown of how the app works:

Adding an Expense: The user is prompted to enter details of an expense. The app asks for the name of the expense, the category, and the amount spent. The user can easily input this information, and the app will create an Expense object to store the data.
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
Summarizing Expenses: Once the user has added a few expenses, the app generates a summary of the data, including the total amount spent and the remaining budget. It helps users understand their financial situation at a glance.
python
Copy code
# Read file and summarize expenses.
summarize_expenses(expense_file_path, budget)

# Show expenses by category.
show_expense_by_category(expenses)
Daily Budget Estimate: The app calculates how much the user can spend each day to stay within their budget. This estimate is updated regularly to reflect the remaining balance.
python
Copy code
# Show the user a rough estimate of how much they have left to spend per day.
show_budget(total_expenses)
Why This Project Was Chosen
The decision to develop this budget tracking application stemmed from a desire to create something that is both practical and beneficial to users. Financial literacy and budget management are essential skills, but many individuals do not have access to simple tools to help them track their spending effectively. By creating this application, I hoped to provide a solution that is easy to use, yet powerful enough to help individuals manage their personal finances.

This project also allowed me to apply the skills I have learned in CS50, including Python programming, file handling, and object-oriented programming. The project helped me solidify my understanding of these concepts while providing a tangible product that can be used in everyday life.

Challenges Faced and Solutions
During the development of the application, I faced several challenges, including ensuring the accuracy of the expense summaries and managing file I/O operations. However, I was able to overcome these challenges by carefully structuring the code and using Python’s built-in libraries for file handling. Additionally, I had to implement a method for handling multiple categories of expenses, which required modifying the Expense class to allow for flexible categorization.

Installation and Setup
To install and run the Budget Tracking application, follow these steps:

Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/budget-tracking.git
Install dependencies: If the project requires additional dependencies, install them using:

bash
Copy code
pip install -r requirements.txt
Run the application: To run the app, use the following command:

bash
Copy code
python expense_tracker.py
Conclusion
The Budget Tracking app is a useful tool for individuals looking to take control of their finances. With its simple interface and powerful features, it allows users to track their expenses, stay within budget, and gain valuable insights into their spending habits. This project not only helped me apply what I’ve learned in CS50 but also provided a solution to a real-world problem that many people face. By continuing to improve the app and adding new features, I hope to make it even more useful for users in the future.

