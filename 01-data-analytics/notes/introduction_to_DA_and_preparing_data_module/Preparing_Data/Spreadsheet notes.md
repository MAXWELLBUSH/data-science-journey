1. What is a Spreadsheet?

A spreadsheet is a software application used to store, organize, calculate, analyze, and visualize data in a grid of rows and columns.

Examples:

Microsoft Excel
Google Sheets
LibreOffice Calc

A spreadsheet looks like:

        A          B          C          D
    ┌────────┬──────────┬──────────┬─────────┐
1   │ Name   │ Product  │ Quantity │ Price   │
    ├────────┼──────────┼──────────┼─────────┤
2   │ John   │ Laptop   │ 2        │ 80000   │
3   │ Mary   │ Phone    │ 3        │ 30000   │
4   │ Peter  │ Tablet   │ 1        │ 25000   │
    └────────┴──────────┴──────────┴─────────┘
2. The Basic Spreadsheet Structure

You need to understand these terms.

Workbook

The entire Excel file.

Example:

Sales_Analysis.xlsx
Worksheet

An individual sheet inside a workbook.

Sales_Analysis.xlsx
│
├── Sales
├── Customers
└── Summary
Row

Horizontal.

1
2
3
4
Column

Vertical.

A
B
C
D
Cell

The intersection of a row and column.

For example:

B4

means:

Column B, Row 4.

Range

A group of cells.

A1:D10

means cells from A1 through D10.

3. Types of Data in Spreadsheets

You'll commonly encounter:

Text
Kenya
John
Laptop
Numbers
100
2500
45.6
Dates
23/08/2026
Boolean
TRUE
FALSE
Formulas
=A2+B2
4. Formulas

A spreadsheet formula normally starts with:

=

Example:

=A2+B2

If:

A2 = 10
B2 = 20

the result is:

30
5. Basic Arithmetic Operators
Operator	Meaning
+	Addition
-	Subtraction
*	Multiplication
/	Division
^	Power

Example:

=B2*C2

If B2 is quantity and C2 is price:

Total = Quantity × Price

6. Your First Practical Exercise

Open Excel or Google Sheets.

Create:

Product	Quantity	Price
Laptop	2	80000
Phone	3	30000
Tablet	4	25000
Monitor	5	15000
Keyboard	10	3000

Add another column:

Total Sales

Your table should become:

Product	Quantity	Price	Total Sales
Laptop	2	80000	?
Phone	3	30000	?
Tablet	4	25000	?
Monitor	5	15000	?
Keyboard	10	3000	?

In D2 enter:

=B2*C2

Then drag the formula down.

Your task

Calculate:

Total Sales = Quantity × Price

7. SUM

SUM adds numbers.

=SUM(D2:D6)

This calculates total sales.

Example:

D2:D6
↓
160,000
90,000
100,000
75,000
30,000
↓
SUM
↓
455,000
8. AVERAGE

Calculates the mean.

=AVERAGE(D2:D6)
9. MIN and MAX
Minimum
=MIN(D2:D6)
Maximum
=MAX(D2:D6)
10. COUNT

Counts cells containing numbers.

=COUNT(D2:D6)

Result:

5
11. COUNTA

Counts non-empty cells.

=COUNTA(A2:A6)

This is useful when the cells contain text.

12. COUNTIF

Counts values that meet a condition.

Suppose you have:

Product	Sales
Laptop	160000
Phone	90000
Tablet	100000
Monitor	75000
Keyboard	30000

To count products with sales greater than 80,000:

=COUNTIF(B2:B6,">80000")
13. SUMIF

Adds values that meet a condition.

=SUMIF(B2:B6,">80000",B2:B6)
14. IF

One of the most important functions for data analysis.

Syntax:

=IF(condition, value_if_true, value_if_false)

Example:

=IF(B2>=50000,"High","Low")

If B2 is 80,000:

High

If B2 is 30,000:

Low
15. Practical Exercise — Customer Classification

Create:

Customer	Spending
John	120000
Mary	45000
Peter	75000
Jane	20000
David	150000

Create a column:

Category

Use:

=IF(B2>=100000,"High",IF(B2>=50000,"Medium","Low"))

You should get:

Customer	Spending	Category
John	120000	High
Mary	45000	Low
Peter	75000	Medium
Jane	20000	Low
David	150000	High

This is directly connected to the conditional statements you've been learning

SORTING

Absolutely. Let's do a real spreadsheet exercise using SORT.

📊 Practical Example: Employee Salaries

Imagine you have this data in Excel:

A — Employee	B — Department	C — Salary
John	IT	75,000
Mary	Finance	95,000
Peter	HR	60,000
Jane	IT	120,000
David	Finance	85,000
🎯 Task 1: Sort employees by salary from lowest to highest

In an empty area, enter:

=SORT(A2:C6,3,1)

You should get:

Employee	Department	Salary
Peter	HR	60,000
John	IT	75,000
David	Finance	85,000
Mary	Finance	95,000
Jane	IT	120,000
🎯 Task 2: Sort from highest salary to lowest

Use:

=SORT(A2:C6,3,-1)

Result:

Employee	Department	Salary
Jane	IT	120,000
Mary	Finance	95,000
David	Finance	85,000
John	IT	75,000
Peter	HR	60,000
🎯 Task 3: Sort alphabetically by employee name

Since Employee is column 1:

=SORT(A2:C6,1,1)

Result starts with:

David → Jane → John → Mary → Peter


Option 1 — Best method: put the header separately

Suppose your original data is:

A	B	C
Employee	Department	Salary
Alex	IT	80,000
Brian	HR	55,000
Carol	Finance	110,000
Diana	IT	70,000
Eric	Finance	95,000

In an empty area, for example E1, enter:

=SORT(A2:C6,3,-1)

Then type the headers manually in E1:G1:

Employee | Department | Salary

Your sorted table becomes:

Employee	Department	Salary
Carol	Finance	110,000
Eric	Finance	95,000
Alex	IT	80,000
Diana	IT	70,000
Brian	HR	55,000
Option 2 — Include the headers in the formula

You can also use:

=VSTACK(A1:C1,SORT(A2:C6,3,-1))

What happens?

A1:C1 → takes your headers
SORT(A2:C6,3,-1) → sorts the actual data
VSTACK → puts the headers on top of the sorted data

So the whole result is created automatically. 👍

Important: Don't use =SORT(A1:C6,3,-1) because Excel may treat the header row as part of the data being sorted.


🔎 FILTERING IN SPREADSHEETS

Filtering means showing only the rows that meet a specific condition, while temporarily hiding the rows that don't.

Think of it like:

Sorting = rearrange the data
Filtering = show only the data I want

Practical example

Suppose you have:

Employee	Department	Salary
Alex	IT	80,000
Brian	HR	55,000
Carol	Finance	110,000
Diana	IT	70,000
Eric	Finance	95,000
🎯 Task: Show only employees in IT

You can use the FILTER formula:

=FILTER(A2:C6,B2:B6="IT")

The result will be:

Employee	Department	Salary
Alex	IT	80,000
Diana	IT	70,000
🔍 Breaking down the formula
=FILTER(A2:C6,B2:B6="IT")

A2:C6 → the data you want returned.

B2:B6="IT" → the condition Excel checks.

So Excel asks each row:

Is the Department equal to IT?

Alex → IT → ✅
Brian → HR → ❌
Carol → Finance → ❌
Diana → IT → ✅
Eric → Finance → ❌

Only Alex and Diana are returned.

🎯 Another example: Salary greater than 80,000
=FILTER(A2:C6,C2:C6>80000)

Result:

Employee	Department	Salary
Carol	Finance	110,000
Eric	Finance	95,000

Notice that Alex (80,000) isn't included because the condition is >80000, not >=80000.

🧠 Remember
SORT   → rearrange
FILTER → select/show

And the basic FILTER structure is:

=FILTER(data,condition)

So:

"Give me this data WHERE this condition is TRUE."


18. Removing Duplicates

Removing duplicates means finding repeated records or values and keeping only one copy of each.

📊 Practical example

Suppose you have this list of departments:

Department
IT
Finance
HR
IT
Finance
IT

Here, IT appears 3 times and Finance appears 2 times.

Method 1: Excel's Remove Duplicates tool
Select your data.
Go to Data.
Click Remove Duplicates.
Select the column(s) you want Excel to check.
Click OK.

You'll get:

Department
IT
Finance
HR

Excel removes the repeated entries and keeps the first occurrence.

Method 2: Using a formula

In newer versions of Excel, you can use:

=UNIQUE(A2:A7)

This creates a new list containing only unique values.

For the example above:

IT
Finance
HR
🔑 Difference

Remove Duplicates → permanently removes duplicates from the selected data.

UNIQUE() → creates a new list without duplicates while leaving the original data unchanged.

🧠 Why is this important in data analysis?

Duplicates can give you incorrect results.

For example, if a customer appears twice when they should appear only once, calculating the number of customers could give you an inflated number.

Removing duplicates = cleaning your dataset by eliminating repeated records


19. Missing Data

Missing data means some values in your dataset are empty, unavailable, or not recorded.

📊 Practical example

Imagine you have this employee dataset:

Employee	Department	Salary	Age
Alex	IT	80,000	25
Brian	HR	55,000	28
Carol	Finance	110,000	—
Diana	IT	—	30
Eric	Finance	95,000	27

Here:

Carol's Age is missing.
Diana's Salary is missing.

These are examples of missing data.

🔎 How do you find missing data in Excel?

You can use:

=COUNTBLANK(A2:A10)

This counts the empty cells in a range.

For example:

=COUNTBLANK(C2:C6)

If one salary is missing, the result is:

1

🛠️ What can you do with missing data?

There are several approaches:

1. Leave it blank

If the missing value isn't important for your analysis.

2. Remove the row

If a record has too much missing information.

3. Replace the missing value

For numerical data, you might use the average or median.

Example:

80,000
90,000
[MISSING]
100,000

You could replace the missing value with the average of the available values.

4. Investigate the source

Sometimes the best solution is to find out why the data is missing and obtain the correct value.

⚠️ Important

Don't automatically replace every missing value with 0.

For example:

Employee	Salary
Alex	80,000
Brian	blank

A blank salary does not necessarily mean Brian earns 0. It could simply mean the salary wasn't recorded.

🧠 Remember

Missing data = information that should be there but isn't available.

In data cleaning, you need to identify → understand → decide how to handle missing values.

20. Text Cleaning in Spreadsheets

Text cleaning means correcting and standardizing text so that your data is consistent and easier to analyze.

For example, these may look like different departments to Excel:

IT
it
 IT
IT 

But they all mean the same thing: IT.

🔹 1. Remove extra spaces — TRIM

Suppose A2 contains:

   Alex   Smith

Use:

=TRIM(A2)

Result:

Alex Smith

TRIM removes unnecessary spaces.

🔹 2. Change text to uppercase — UPPER
=UPPER(A2)

alex → ALEX

Useful when you want consistent formatting.

🔹 3. Change text to lowercase — LOWER
=LOWER(A2)

ALEX → alex

🔹 4. Capitalize names — PROPER
=PROPER(A2)

alex smith → Alex Smith

🔹 5. Replace unwanted text — SUBSTITUTE

Suppose:

Kenya - Nairobi
Kenya - Mombasa

You want to remove "Kenya - ".

=SUBSTITUTE(A2,"Kenya - ","")

Result:

Nairobi
🔹 6. Remove unwanted characters — CLEAN
=CLEAN(A2)

CLEAN removes certain non-printing characters that can appear when data is copied from other systems.

21. Text Concatenation

Text concatenation means joining two or more pieces of text together to create one text value.

📊 Practical example

Suppose you have:

A — First Name	B — Last Name
John	Kamau
Mary	Wanjiku
Peter	Otieno

You want to create a Full Name column.

Method 1: Using &

In C2:

=A2&" "&B2

Result:

John Kamau

The " " adds a space between the first and last name.

Then drag the formula down:

First Name	Last Name	Full Name
John	Kamau	John Kamau
Mary	Wanjiku	Mary Wanjiku
Peter	Otieno	Peter Otieno
Method 2: Using CONCAT
=CONCAT(A2," ",B2)

This also produces:

John Kamau

Method 3: Using TEXTJOIN

This is especially useful when joining many pieces of text.

=TEXTJOIN(" ",TRUE,A2,B2)

Meaning:

" " → put a space between values
TRUE → ignore empty cells
A2,B2 → text to join
🧪 Practical exercise

Create this table:

First Name	Last Name	Email
Alex	Mwangi	
Brian	Otieno	
Carol	Kamau	

Suppose you want to create an email like:

alex.mwangi@gmail.com

You could use:

=LOWER(A2&"."&B2&"@gmail.com")

For Alex Mwangi → alex.mwangi@gmail.com

🧠 Remember

Concatenation = joining text together.

Common methods:

&          → join text
CONCAT()   → join text
TEXTJOIN() → join multiple pieces with a separator

Data-analysis use: Concatenation is useful for creating full names, IDs, email addresses, product codes, addresses, and labels from separate columns.

Your formula is:

=LOWER(A2&"."&B2&"@gmail.com")

Let's break it apart:

Step 1: A2

Suppose A2 contains:

Alex
Step 2: &"."

We join a dot to Alex:

Alex.
Step 3: &B2

Suppose B2 contains:

Mwangi

Now:

Alex.Mwangi
Step 4: &"@gmail.com"

Now we need to join @gmail.com to what we already have:

Alex.Mwangi@gmail.com

That's why we need another & after B2.

Think of & as "PLUS" for text
A2 & "." & B2 & "@gmail.com"
 ↓      ↓      ↓
Alex   .      Mwangi   @gmail.com

The result before LOWER():

Alex.Mwangi@gmail.com

Then LOWER() converts everything to lowercase:

alex.mwangi@gmail.com
🧠 Very important

The & always goes between the things you want to join.

A2 & "." & B2 & "@gmail.com"

There are 4 things being joined:

A2
"."
B2
"@gmail.com"

Therefore, you need 3 & operators between them.


22. Dates in Spreadsheets

Dates are very important in data analysis because they allow you to track time, calculate durations, sort records, and filter information by date.

1. Entering dates

You can enter a date like:

23/08/2026

Excel recognizes it as a date.

For example:

Employee	Start Date
Alex	10/01/2025
Brian	15/03/2025
Carol	20/06/2026
2. Getting today's date — TODAY()
=TODAY()

This automatically gives you today's date.

The important thing is that it updates automatically when the date changes.

3. Getting the current date AND time — NOW()
=NOW()

For example:

23/08/2026 10:30

TODAY() → date only

NOW() → date + time

4. Calculating the difference between dates

Suppose:

A	B
Start Date	End Date
01/01/2026	23/08/2026

You can subtract the dates:

=B2-A2

This gives the number of days between them.

5. Finding someone's age

Suppose:

A2 = 15/05/2000

You can use:

=DATEDIF(A2,TODAY(),"Y")

The "Y" means complete years.

So Excel calculates the person's age.

6. Extracting parts of a date

Suppose A2 contains:

23/08/2026

You can extract:

Year:

=YEAR(A2)

Result:

2026

Month:

=MONTH(A2)

Result:

8

Day:

=DAY(A2)

Result:

23
🧪 Practical exercise

Create this:

Employee	Start Date
Alex	10/01/2025
Brian	15/03/2025
Carol	20/06/2026
Diana	05/08/2026

Now try:

1. Today's date

=TODAY()

2. Extract the year from Alex's start date

=YEAR(B2)

3. Extract the month

=MONTH(B2)

4. Calculate how many days Alex has been employed

=TODAY()-B2
🧠 Remember these
Formula	What it does
TODAY()	Today's date
NOW()	Current date + time
YEAR()	Gets the year
MONTH()	Gets the month
DAY()	Gets the day
DATEDIF()	Calculates date differences

Key idea: Excel stores dates as values, which is why you can perform calculations such as TODAY()-B2.


23. Absolute vs Relative References

This is very important.

Suppose:

=A2*B2

When you drag it down, it becomes:

=A3*B3
=A4*B4
=A5*B5

That's a relative reference.

Absolute Reference

Suppose you have a tax rate:

F1 = 16%

You want every row to use F1.

Use:

=B2*$F$1

The $ locks the cell.

When dragged down:

=B3*$F$1
=B4*$F$1
=B5*$F$1

F1 remains fixed.


24. VLOOKUP / XLOOKUP

These are lookup functions. They are used when you want to find information in a table based on a matching value.

Think of it as:

"I know this person's ID. Find me their name/salary/department."

🔹 Practical Example

Imagine you have this table:

A — ID	B — Employee	C — Department	D — Salary
101	Alex	IT	80,000
102	Brian	HR	55,000
103	Carol	Finance	110,000
104	Diana	IT	70,000
105	Eric	Finance	95,000

Now suppose you enter an ID in F2:

103

You want Excel/Google Sheets to automatically find the employee's name.

1. VLOOKUP

The formula is:

=VLOOKUP(F2,A2:D6,2,FALSE)

This returns:

Carol

Break it down:
=VLOOKUP(what to find, where to search, column to return, exact match)

So:

F2 → 103, the ID we're looking for
A2:D6 → the table
2 → return the value from the 2nd column
FALSE → look for an exact match
What happens?

Sheets searches the first column:

101
102
103 ← FOUND!
104
105

Then it moves across to column 2:

Carol

🔹 Get the department

Change 2 to 3:

=VLOOKUP(F2,A2:D6,3,FALSE)

Result:

Finance

Get the salary:

=VLOOKUP(F2,A2:D6,4,FALSE)

Result:

110,000

2. XLOOKUP

XLOOKUP is a newer and more flexible lookup function.

For the same example:

=XLOOKUP(F2,A2:A6,B2:B6)

Result:

Carol

Break it down
=XLOOKUP(what to find, where to look, what to return)

So:

F2 → 103
A2:A6 → search the ID column
B2:B6 → return the Employee column
Get Department
=XLOOKUP(F2,A2:A6,C2:C6)

Result:

Finance

Get Salary
=XLOOKUP(F2,A2:A6,D2:D6)

Result:

110,000

🆚 VLOOKUP vs XLOOKUP
VLOOKUP	XLOOKUP
Older function	Newer function
Uses column number	Uses return range
2, 3, 4 specify columns	You directly specify the column
Usually searches from left to right	Can search left or right
More restrictive	More flexible
🧠 Easy way to remember

VLOOKUP:

"Find this value in the first column and go VERTICALLY → across the table."

XLOOKUP:

"Find this value here, and return the corresponding value there."