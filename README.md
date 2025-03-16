# SQLite3 Commands Guide

## Introduction
SQLite3 ek lightweight aur self-contained database hai jo command-line interface (CLI) par operate karta hai. Yeh guide SQLite3 ke basic commands ko step-by-step define karti hai.

---

## Step-by-Step Commands

### 1. SQLite3 Start Karna
Sabse pehle, SQLite3 start karne ke liye terminal ya command prompt open karein aur yeh command likhein:
```sh
sqlite3
```
**Output:**
```
SQLite version 3.39.2 2022-07-21 15:24:47
Enter ".help" for usage hints.
sqlite>
```
Yeh SQLite3 shell open karega.

### 2. Database Open ya Create Karna
Agar aapke paas pehle se ek database hai, toh usko open karein. Agar nahi hai, toh yeh command ek naya database create kar dega:
```sh
.open mydatabase.db
```
**Output:** (Koi visible output nahi hoga, lekin database open ho jayega)
```
sqlite>
```

### 3. Available Tables Check Karna
Database ke andar jitni tables mojood hain, unko dekhne ke liye yeh command use karein:
```sh
.tables
```
**Output (Agar koi table nahi hai):**
```
sqlite>
```
**Output (Agar tables mojood hain):**
```
users   orders   products
```

### 4. Table Ki Data Check Karna
Kisi bhi table ke andar mojood data ko check karne ke liye yeh command use karein:
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

### 5. Output Formatting Improve Karna
Default output readable nahi hota, isliye formatting improve karne ke liye yeh commands use karein:
```sh
.mode column
.headers on
```
Phir dobara data dekhne ke liye:
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

### 6. Data Ko CSV Format Mein Export Karna
Agar aap table ka data CSV format mein export karna chahte hain, toh yeh commands use karein:
```sh
.mode csv
.output users.csv
SELECT * FROM users;
.output stdout
```
**Output (Terminal pe koi response nahi milega, lekin `users.csv` file create ho jayegi):**
```
sqlite>
```
Agar aap CSV file ko manually check karna chahein toh kisi text editor ya spreadsheet software mein open karein.

---

## Conclusion
Yeh basic SQLite3 commands hain jo kisi bhi beginner ke liye kaafi madadgaar ho sakti hain. Agar aap aur advance queries ya indexing seekhna chahein toh SQLite3 ki official documentation bhi check kar sakte hain.

Happy Coding! 🎉

