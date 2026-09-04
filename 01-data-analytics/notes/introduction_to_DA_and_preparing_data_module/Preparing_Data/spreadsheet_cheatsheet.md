# Spreadsheet Cheat Sheet — Data Analysis

## 1. Basic Spreadsheet Concepts

| Concept | Meaning                       |
| ------- | ----------------------------- |
| Cell    | A single box in a spreadsheet |
| Row     | Horizontal line of cells      |
| Column  | Vertical line of cells        |
| Range   | Group of cells, e.g. `A1:D10` |
| Header  | Name describing a column      |
| Dataset | Collection of organized data  |

---

## 2. Essential Data Operations

### Sorting

**Data → Sort**

* A → Z = ascending
* Z → A = descending

### Filtering

**Data → Filter**

Use filters to show only records matching a condition.

Example:

> Show only `Nairobi` records.

### Removing Duplicates

**Data → Remove Duplicates**

Useful when the same record appears more than once.

### Missing Data

Look for:

* Blank cells
* `N/A`
* `NULL`
* `-`

Possible actions:

* Fill with an appropriate value
* Remove the record
* Leave blank
* Investigate the source

---

# 3. Important Formulas

## SUM

Adds numbers.

```excel
=SUM(D2:D10)
```

## AVERAGE

Calculates the mean.

```excel
=AVERAGE(D2:D10)
```

## COUNT

Counts cells containing numbers.

```excel
=COUNT(D2:D10)
```

## COUNTA

Counts non-empty cells.

```excel
=COUNTA(A2:A10)
```

## MAX

Finds the largest value.

```excel
=MAX(D2:D10)
```

## MIN

Finds the smallest value.

```excel
=MIN(D2:D10)
```

---

# 4. Conditional Formulas

## IF

```excel
=IF(D2>=50,"Pass","Fail")
```

Meaning:

> If D2 is 50 or higher → Pass; otherwise → Fail.

## AND

All conditions must be TRUE.

```excel
=AND(A2="Yes",B2>=50)
```

## OR

At least one condition must be TRUE.

```excel
=OR(A2="Yes",B2>=50)
```

---

# 5. Conditional Aggregation

## SUMIF

Adds values that meet one condition.

```excel
=SUMIF(C2:C10,"Nairobi",D2:D10)
```

Meaning:

> Add Sales where Region is Nairobi.

## COUNTIF

Counts values matching a condition.

```excel
=COUNTIF(C2:C10,"Nairobi")
```

## AVERAGEIF

Calculates the average for values meeting a condition.

```excel
=AVERAGEIF(C2:C10,"Nairobi",D2:D10)
```

---

# 6. Text Functions

## LOWER

Converts text to lowercase.

```excel
=LOWER(A2)
```

## UPPER

Converts text to uppercase.

```excel
=UPPER(A2)
```

## PROPER

Capitalizes the first letter of each word.

```excel
=PROPER(A2)
```

## TRIM

Removes unnecessary spaces.

```excel
=TRIM(A2)
```

## CONCAT

Combines text.

```excel
=CONCAT(A2," ",B2)
```

## `&`

Another way to combine text.

```excel
=A2&" "&B2
```

Example:

`John` + `Smith`

becomes:

`John Smith`

---

# 7. Text Cleaning

Common cleaning functions:

```excel
=TRIM(A2)
=LOWER(A2)
=UPPER(A2)
=PROPER(A2)
```

Use them to standardize inconsistent text.

Example:

```text
"  NAIROBI "
```

can become:

```text
"nairobi"
```

using:

```excel
=LOWER(TRIM(A2))
```

---

# 8. Dates

Useful functions:

```excel
=TODAY()
```

Returns today's date.

```excel
=YEAR(A2)
```

Extracts the year.

```excel
=MONTH(A2)
```

Extracts the month.

```excel
=DAY(A2)
```

Extracts the day.

---

# 9. Absolute vs Relative References ⭐

### Relative reference

```excel
=A2*B2
```

When copied down, it changes:

```excel
=A3*B3
=A4*B4
```

### Absolute reference

```excel
=A2*$F$1
```

`$F$1` stays fixed when the formula is copied.

### Remember:

**A2 → moves**

**$A$2 → stays fixed**

Shortcut:

**F4** → toggle reference types.

---

# 10. VLOOKUP

Finds information from another table.

```excel
=VLOOKUP(F2,A2:D10,2,FALSE)
```

Structure:

```text
VLOOKUP(
lookup_value,
table,
column_number,
exact_match
)
```

`FALSE` means:

> Find an exact match.

---

# 11. XLOOKUP ⭐

Modern alternative to VLOOKUP.

```excel
=XLOOKUP(F2,A2:A10,B2:B10)
```

Meaning:

> Find F2 in A2:A10 and return the corresponding value from B2:B10.

---

# 12. Pivot Tables ⭐

A Pivot Table summarizes large datasets.

### Four main areas

| Area    | Purpose                   |
| ------- | ------------------------- |
| Rows    | Categories down the side  |
| Columns | Categories across the top |
| Values  | Numbers being calculated  |
| Filters | Restrict the data shown   |

Example:

```text
Rows     → Salesperson
Columns  → Region
Values   → Sales → SUM
Filters  → Product
```

### Common calculations

* Sum
* Count
* Average
* Maximum
* Minimum

### Main idea

> **Pivot Table = quickly summarize data.**

---

# 13. Charts 📊

| Chart     | Use it for                                   |
| --------- | -------------------------------------------- |
| Column    | Compare categories                           |
| Bar       | Compare categories, especially long names    |
| Line      | Trends over time                             |
| Pie       | Parts of a whole                             |
| Scatter   | Relationship between two numerical variables |
| Histogram | Distribution of numerical data               |

### Quick memory

```text
Compare categories → Bar/Column
Time → Line
Parts of whole → Pie
Two numerical variables → Scatter
Distribution → Histogram
```

---

# 14. Conditional Formatting ⭐

Automatically formats cells when a condition is met.

### Greater than

**Home → Conditional Formatting → Highlight Cells Rules → Greater Than**

Example:

> Highlight Sales > 5,000.

### Less than

> Highlight Sales < 3,000.

### Duplicate values

> Find repeated values.

### Data Bars

Shows the size of values visually.

### Color Scales

Shows low-to-high values using different formatting.

### Icon Sets

Shows performance/status using icons.

### Main idea

> **Conditional Formatting = identify and visualize patterns/problems.**

---

# 15. Data Validation ⭐

Controls what users can enter.

### Dropdown list

**Data → Data Validation → Allow: List**

Example:

```text
Nairobi
Mombasa
Kisumu
Nakuru
```

### Number validation

Allow:

```text
18–60
```

for an Age column.

### Main idea

> **Data Validation = control/prevent invalid data entry.**

---

# 16. Excel Tables ⭐

Convert a dataset into a structured Excel Table.

### Shortcut

**Ctrl + T**

Then make sure:

**My table has headers**

is checked.

### Benefits

* Automatic filters
* Automatically expands
* Formulas can automatically fill
* Structured references
* Easier Pivot Tables
* Easier analysis

### Rename a Table

**Table Design → Table Name**

Example:

```text
SalesData
```

Then:

```excel
=SUM(SalesData[Sales])
```

---

# 17. Important Excel Shortcuts

| Shortcut           | Action                     |
| ------------------ | -------------------------- |
| `Ctrl + C`         | Copy                       |
| `Ctrl + V`         | Paste                      |
| `Ctrl + X`         | Cut                        |
| `Ctrl + Z`         | Undo                       |
| `Ctrl + Y`         | Redo                       |
| `Ctrl + S`         | Save                       |
| `Ctrl + F`         | Find                       |
| `Ctrl + H`         | Find and Replace           |
| `Ctrl + T`         | Create Table               |
| `Ctrl + A`         | Select data                |
| `Ctrl + Shift + L` | Turn filters on/off        |
| `F4`               | Toggle absolute references |
| `Alt + =`          | AutoSum                    |

---

# 18. The Data Analysis Workflow ⭐⭐⭐

A common spreadsheet workflow is:

```text
1. Collect data
       ↓
2. Enter/import data
       ↓
3. Check data quality
       ↓
4. Remove duplicates
       ↓
5. Handle missing data
       ↓
6. Clean text
       ↓
7. Format dates/numbers
       ↓
8. Validate data
       ↓
9. Create Excel Table
       ↓
10. Sort & Filter
       ↓
11. Analyze with formulas
       ↓
12. Create Pivot Tables
       ↓
13. Create Charts
       ↓
14. Present insights
```

---

# 19. Formula Memory Trick 🧠

When you forget a formula, don't try to memorize everything blindly.

Ask:

### "What am I trying to do?"

**Add numbers?**

```excel
=SUM()
```

**Find an average?**

```excel
=AVERAGE()
```

**Count numbers?**

```excel
=COUNT()
```

**Count based on a condition?**

```excel
=COUNTIF()
```

**Add based on a condition?**

```excel
=SUMIF()
```

**Make a decision?**

```excel
=IF()
```

**Find information in another table?**

```excel
=XLOOKUP()
```

**Combine text?**

```excel
=A2&" "&B2
```

---

# 20. Most Important Concepts to Remember

### Data Cleaning

```text
Sort
Filter
Remove duplicates
Missing data
Text cleaning
Date cleaning
```

### Data Analysis

```text
SUM
AVERAGE
COUNT
COUNTIF
SUMIF
IF
XLOOKUP
Pivot Tables
```

### Data Quality

```text
Data Validation
Consistent formats
No unnecessary duplicates
Correct data types
```

### Data Visualization

```text
Column
Bar
Line
Pie
Scatter
Histogram
```

### Spreadsheet Structure

```text
Excel Table
Headers
Rows
Columns
Ranges
Structured References
```

---

# 21. ⭐ The Big Picture

Think of Excel data analysis as:

```text
              RAW DATA
                  ↓
           CLEAN THE DATA
                  ↓
          ORGANIZE THE DATA
                  ↓
         ANALYZE THE DATA
                  ↓
          PIVOT TABLES
                  ↓
             CHARTS
                  ↓
             INSIGHTS
```

The goal isn't just to make a spreadsheet look good.

> **The goal of data analysis is to turn raw data into useful information that can support decisions.**
