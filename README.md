# SQLite3 Commands Guide

## Introduction
SQLite3 is a lightweight and self-contained database that operates via the command-line interface (CLI). This guide provides a step-by-step explanation of basic SQLite3 commands.

---

## Step-by-Step Commands

### 1. Starting SQLite3
First, open the terminal or command prompt and enter the following command:
```sh
sqlite3
```
**Output:**
```
SQLite version 3.39.2 2022-07-21 15:24:47
Enter ".help" for usage hints.
sqlite>
```
This will open the SQLite3 shell.

### 2. Opening or Creating a Database
If you already have a database, you can open it. If not, this command will create a new one:
```sh
.open mydatabase.db
```
**Output:** (No visible output, but the database will be opened)
```
sqlite>
```

### 3. Checking Available Tables
To see the tables present in the database, use the following command:
```sh
.tables
```
**Output (If no tables exist):**
```
sqlite>
```
**Output (If tables exist):**
```
users   orders   products
```

### 4. Checking Table Data
To view the data inside a specific table, use this command:
```sh
SELECT * FROM users;
```
**Output:**
```
id  | name     | age
--------------------
1   | Ali      | 25
2   | Sara     | 22
3   | Ahmed    | 30
```

### 5. Improving Output Formatting
By default, the output may not be easily readable. To improve formatting, use these commands:
```sh
.mode column
.headers on
```
Then, check the data again:
```sh
SELECT * FROM users;
```
**Output (Formatted Table View):**
```
id  name   age  
--- ------ ---- 
1   Ali    25   
2   Sara   22   
3   Ahmed  30   
```

### 6. Exporting Data to CSV Format
If you want to export the table data to a CSV file, use the following commands:
```sh
.mode csv
.output users.csv
SELECT * FROM users;
.output stdout
```
**Output (No terminal response, but `users.csv` file will be created):**
```
sqlite>
```
To check the CSV file, open it in a text editor or spreadsheet software.

---

## Conclusion
These are the basic SQLite3 commands that are useful for beginners. If you want to learn more about advanced queries or indexing, refer to the official SQLite3 documentation.

Happy Coding! 🎉

**Written by: Muzaffar Ahmed**

