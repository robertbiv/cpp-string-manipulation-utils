# Loan Calculator

A simple C++ console application that calculates monthly payments, total amount paid, and interest cost for a loan.

## Description

This program helps users calculate various aspects of a loan repayment plan. Given a loan amount, yearly interest rate, and number of monthly payments, it computes:

- Monthly interest rate
- Monthly payment amount
- Total amount to be paid back
- Total interest cost

## Features

- User-friendly console interface
- Precise calculations using standard C++ math library
- Output formatted to two decimal places for currency
- Supports various loan amounts, interest rates, and payment terms

## Prerequisites

- C++ compiler with C++11 support or later (e.g., g++, MSVC, clang++)
- Standard C++ library

## Building the Project

### Using g++ (Linux/macOS/Windows with MinGW)

```bash
g++ -o loan_calculator Source.cpp -lm
```

### Using Visual Studio

1. Open the `homework1.vcxproj` file in Visual Studio
2. Build the project (F7 or Build > Build Solution)
3. The executable will be in the Debug or Release folder

### Using MSVC Command Line

```bash
cl Source.cpp /Fe:loan_calculator.exe
```

## Usage

Run the compiled executable and follow the prompts:

```bash
./loan_calculator
```

### Example Session

```
How much is the loan?: $10000
What is the yearly interest rate? (decimal form): 0.05
How many monthly payments do you have?: 36
Loan Amount: 				$ 10000.00
Monthly Interest Rate:			  0%
Number of Payments:			  36
Monthly Payment: 			$ 299.71
Amount Paid Back: 			$ 10789.52
Interest Paid: 				$ 789.52
```

### Input Parameters

1. **Loan Amount**: The principal amount of the loan in dollars (e.g., 10000)
2. **Yearly Interest Rate**: The annual interest rate in decimal form (e.g., 0.05 for 5%)
3. **Number of Monthly Payments**: The total number of monthly payments (e.g., 36 for a 3-year loan)

## Calculation Formula

The program uses the standard loan payment formula:

```
M = (r * (1 + r)^N) / ((1 + r)^N - 1) * L
```

Where:
- M = Monthly payment
- L = Loan amount
- r = Monthly interest rate (yearly rate / 12)
- N = Number of payments

## Author

**Robert Bennethum**
- Email: rmb6287@psu.edu
- Class: CMPSC 121
- Project #19
- Due Date: September 17, 2021

## Project Structure

```
.
├── Source.cpp                  # Main source code file
├── homework1.vcxproj          # Visual Studio project file
├── homework1.vcxproj.filters  # Visual Studio filters
├── homework1.vcxproj.user     # Visual Studio user settings
└── Debug/                     # Debug build output (generated)
```

## License

This is a class project and is provided as-is for educational purposes.

## Notes

- The program uses `cout.setf()` and `cout.precision()` to format currency output to two decimal places
- Interest rate should be entered in decimal form (e.g., 0.05 for 5%, not 5)
- The program calculates all values based on the standard amortization formula
