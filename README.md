# Lotus Banking System

A Java-based banking application with GUI interface for managing customer accounts, transactions, and banking operations.

## Features

- **User Authentication**: Secure login system with username/password validation
- **Account Management**: View and manage multiple customer accounts
- **Deposit Operations**: Add funds to customer accounts
- **Withdrawal Operations**: Withdraw funds with balance validation
- **Transfer Operations**: Transfer funds between accounts
- **Data Persistence**: CSV-based storage for account information
- **GUI Interface**: User-friendly Swing-based graphical interface

## System Requirements

- Java 11 or higher
- Java Swing library (included in JDK)

## Project Structure

```
BankingSystem/
├── src/
│   └── com/assignment/main/
│       ├── Main.java          # Main application entry point with all classes
│       └── GUI.java           # GUI components and interface
├── Accounts.csv               # Account data storage
└── Lotus_Logo.png            # Application logo
```

## Classes Overview

### Customer
Base class for storing customer information:
- First Name
- Last Name

### Account
Extends Customer class with banking functionality:
- Account Number
- Balance
- Deposit method
- Withdraw method (with exception handling)

### Transaction
Handles fund transfers between accounts:
- Transfer method with validation
- Exception handling for insufficient funds

### LoginGUI
Authentication interface:
- Username/password validation
- Default credentials: Admin/Admin
- Loads account data from CSV

### GUI
Main banking interface with:
- Account overview table
- Deposit panel
- Withdrawal panel
- Transfer panel
- Real-time balance updates

### ReadAccounts
CSV file reader for loading account data:
- Reads first names, last names
- Reads account numbers and balances
- Returns LinkedList collections

### CSVUpdater
Updates account information in CSV file:
- Writes updated balances
- Maintains data integrity
- Finds accounts by number

### InsufficientFundsException
Custom exception for handling insufficient balance scenarios

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Lotus-Banking-System
```

2. Compile the Java files:
```bash
javac -d bin src/com/assignment/main/*.java
```

3. Run the application:
```bash
java -cp bin com.assignment.main.Main
```

## Usage

### Login
1. Launch the application
2. Enter credentials (Default: Admin/Admin)
3. Click "Login" button

### Deposit Funds
1. Enter account number
2. Enter deposit amount
3. Click "Deposit" button

### Withdraw Funds
1. Enter account number
2. Enter withdrawal amount
3. Click "Withdraw" button
4. System validates sufficient balance

### Transfer Funds
1. Enter source account number
2. Enter destination account number
3. Enter transfer amount
4. Click "Transfer" button

### View All Accounts
1. Click "Show All" button
2. View account details in table format

## CSV File Format

The `Accounts.csv` file should follow this format:
```
FirstName,LastName,AccountNumber,Balance
John,Doe,1001,5000
Jane,Smith,1002,3000
```

## Error Handling

- **Insufficient Funds**: Displays error message when withdrawal/transfer exceeds balance
- **Invalid Input**: Validates numeric input for amounts and account numbers
- **Empty Fields**: Prevents operations with missing information
- **Account Not Found**: Alerts user when account number doesn't exist

## Security Features

- Password field masking
- Login validation
- Transaction validation
- Balance verification before withdrawals

## GUI Components

- **Window Size**: 1920x1080 (Full HD)
- **Custom Logo**: Lotus Bank branding
- **Color Scheme**: 
  - Deposit: Green
  - Withdraw: Red
  - Transfer: Orange
  - Show All: Blue

## Known Limitations

- Single admin user authentication
- CSV-based storage (not suitable for production)
- No encryption for sensitive data
- No transaction history logging
- No concurrent user support

## Future Enhancements

- Database integration (MySQL/PostgreSQL)
- Multiple user roles and permissions
- Transaction history and reporting
- Account statement generation
- Email notifications
- Password encryption
- Multi-factor authentication
- Responsive design for different screen sizes

## Developer Information

- **Developer**: Kamal Dhital
- **University Student ID**: 2407046

## License

This project is developed for educational purposes.

## Support

For issues or questions, please contact the developer or create an issue in the repository.
