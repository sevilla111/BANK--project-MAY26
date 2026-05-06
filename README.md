# 🏦 Bank Management System

A simple command-line Bank Management System written in C that supports creating accounts, depositing and withdrawing money, and checking balances — all persisted to a local binary file.

---

## Features

- **Create Account** — Register a new bank account with a name and account number
- **Deposit Money** — Add funds to an existing account
- **Withdraw Money** — Withdraw funds with an insufficient balance check
- **Check Balance** — View the current balance for any account
- **Persistent Storage** — All account data is saved to a local file (`account.dat`) so it survives between sessions

---

## Getting Started

### Prerequisites

- A C compiler (e.g., `gcc`)

### Build

```bash
gcc BANK.C -o bank
```

### Run

```bash
./bank
```

---

## Usage

When launched, you'll see an interactive menu:

```
*** Bank Management System ***
1. Create Account
2. Deposit Money
3. Withdraw Money
4. Check Balance
5. Exit
Enter your choice:
```

Simply enter the number corresponding to the action you want to perform and follow the prompts.

### Example

```
Enter your choice: 1
Enter your name: John Doe
Enter your account number: 1001
Account created successfully!

Enter your choice: 2
Enter your account number: 1001
Enter amount to deposit: 5000
Successfully deposited Rs.5000.00 New balance is Rs.5000.00
```

---

## Data Storage

Account data is stored in a binary file called `account.dat` in the same directory as the executable. This file is created automatically on first use.

> ⚠️ Do not manually edit `account.dat` as it stores data in binary format.

---

## Project Structure

```
.
├── BANK.C        # Main source file
├── account.dat   # Auto-generated data file (created at runtime)
└── README.md
```

---

## Limitations

- Account numbers must be unique — the program does not enforce this on creation
- No PIN or password protection
- Single-user (no concurrent access support)
- Data is stored in a flat binary file with no indexing

---

## License

This project is open source and available under the [MIT License](LICENSE).
