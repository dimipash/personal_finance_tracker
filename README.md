# Personal Finance Tracker

This Python application helps you track your personal finances by allowing you to add income and expense transactions, view transaction summaries, and visualize your financial data.

## Features

- Add new income and expense transactions
- View transactions and summaries within a specified date range
- Visualize income and expenses over time with a plot
- Data persistence using CSV file storage
- User-friendly data entry with input validation

## Requirements

- Python 3.x
- pandas
- matplotlib

## Installation

1. Clone this repository or download the source code.
2. Install the required packages:

pip install pandas matplotlib

## Usage

Run the application by executing the main.py file:

python main.py

The application will present a menu with the following options:

1. Add a new transaction
2. View transactions and summary within a date range
3. Exit

### Adding a Transaction

When adding a new transaction, you'll be prompted to enter:

- Date (format: dd-mm-yyyy)
- Amount
- Category (Income or Expense)
- Description

The `data_entry.py` module handles user input with validation:

- `get_date()`: Ensures the date is in the correct format (dd-mm-yyyy).
- `get_amount()`: Validates that the amount is a positive number.
- `get_category()`: Allows users to input 'I' for Income or 'E' for Expense.
- `get_description()`: Captures an optional description for the transaction.

### Viewing Transactions

To view transactions:

1. Enter a start date and end date when prompted.
2. The application will display all transactions within the specified date range.
3. A summary of total income, total expenses, and net savings will be shown.
4. You'll have the option to view a plot of income and expenses over time.

## Data Storage

Transaction data is stored in a CSV file named `finance_data.csv` in the same directory as the script.

## Project Structure

- `main.py`: The main application file containing the CSV class and program logic.
- `data_entry.py`: Module for handling user input with validation.
