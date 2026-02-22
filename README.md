# FinSync
A one-stop solution for your finaical trascations, tracking expenses, and setting saving goals.

> This is a term project for a university course about fundamentals of OOP and Java.

# Functionality
- Create an account
- Perform transactions: deposit, withdrawal, transfer
- Own 2 different types of banking accounts (expense & savings)
- Generate & download account report

## Types of Accounts
1. **Expense**: Track where money is spent. User can use all types of transactions: withdraw, deposit and transfer money.

2. **Savings**: Set a goal and deposit money to reach that goal. User can only deposit money.

## Data Limitation
No database or external storage is used. All data is only stored during 1 run, rerunning resets any progress. However, a user can create multiple "user accounts" and login to any of them.

# UML 
Graphical representation of our Class structure. Graph elements key:

```
+  Public
-  Private
#  Protected
~  Default

*  Many instances
Subclass —————▷ Superclass
```

## Class Structure

<img width="5042" height="4446" alt="Blank diagram" src="https://github.com/user-attachments/assets/7e4a1af1-ce8c-4ac8-b770-87e769ebe40e" />

**Expense** and **Savings** are subclasses of **Account**.

## Running Loop

<img width="4296" height="3879" alt="Blank diagram (1)" src="https://github.com/user-attachments/assets/1048cb8c-b54f-4947-b7e0-421a1ccfc83d" />

> All loops run forever until terminated either by stopping the JVM or picking the "quit" (or equivalent) option

### Loop Order/structure
1. **Main** initiates all ArrayLists (Users, Accounts, Expenses, Savings) and starts the **Start Login Menu**.
2. When a user creates an account or logs in, **User Main Menu** is initialized.
3. In the **User Main Menu**, the user has a choice:
4. Savings account (which initializes and runs **Manage Savings**) or
5. Expense Account (which initializes and runs **Manage Expense**.
