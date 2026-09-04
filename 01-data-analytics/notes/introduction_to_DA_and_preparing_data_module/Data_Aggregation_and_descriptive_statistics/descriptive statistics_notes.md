
# **Descriptive Statistics**

Descriptive statistics is the branch of statistics used to organize, summarize, and describe data.

Instead of looking at hundreds or thousands of individual values, descriptive statistics helps you answer questions like:

What is the average?
What is the middle value?
What is the most common value?
How spread out is the data?
What is the smallest and largest value?
The main areas
Descriptive Statistics
│
├── Measures of Central Tendency
│   ├── Mean
│   ├── Median
│   └── Mode
│
├── Measures of Dispersion
│   ├── Range
│   ├── Variance
│   └── Standard Deviation
│
└── Measures of Position
    ├── Percentiles
    └── Quartiles

## * Mean

The mean is the arithmetic average.

Suppose salaries are:

40,000, 50,000, 60,000

## Mean = (40,000 + 50,000 + 60,000) / 3
     = 50,000

In Excel:

=AVERAGE(A2:A4)

### 2. Median

The median is the middle value when data is arranged from smallest to largest.

Example:

20, 30, 40, 50, 60

Median = 40

If there are an even number of values:

20, 30, 40, 50

Median:

(30 + 40) / 2 = 35

Excel:

=MEDIAN(A2:A5)

## 3. Mode

The mode is the value that appears most frequently.

Example:

10, 20, 20, 30, 40

Mode = 20

Excel:

=MODE.SNGL(A2:A6)

## 4. Range

The range tells you the difference between the largest and smallest values.

Example:

20, 30, 40, 50, 80

Range = 80 - 20
      = 60

Excel:

=MAX(A2:A6)-MIN(A2:A6)

## 5. Variance

Variance measures how far values tend to spread from the mean.

A larger variance means the values are more spread out.

A smaller variance means the values are closer together.

For a sample:

=VAR.S(A2:A10)

For an entire population:

=VAR.P(A2:A10)
6. Standard Deviation

Standard deviation measures how spread out values are around the mean.

For example, imagine two groups:

Group A: 48, 49, 50, 51, 52
Group B: 20, 35, 50, 65, 80

Both have a mean of 50, but Group B is much more spread out.

Therefore, Group B has a larger standard deviation.

Excel:

=STDEV.S(A2:A10)

## 7. Quartiles

Quartiles divide ordered data into four parts.

Q1 → 25th percentile
Q2 → 50th percentile (median)
Q3 → 75th percentile

Excel:

=QUARTILE.INC(A2:A20,1)
=QUARTILE.INC(A2:A20,2)
=QUARTILE.INC(A2:A20,3)
Example using your salary dataset

Suppose your Base Pay is in C2:C21.

You could calculate:

=AVERAGE(C2:C21)
=MEDIAN(C2:C21)
=MODE.SNGL(C2:C21)
=MAX(C2:C21)
=MIN(C2:C21)
=MAX(C2:C21)-MIN(C2:C21)
=STDEV.S(C2:C21)
=VAR.S(C2:C21)

This gives you a statistical summary of the salary data without having to inspect every employee individually.

Easy memory trick

Central tendency → Where is the center?

Mean, Median, Mode

Dispersion → How spread out is it?

Range, Variance, Standard Deviation

Position → Where does a value fall in the distribution?

Percentiles, Quartiles


You need to know measures of central tendency because they help you quickly understand the "typical" or "central" value in a dataset.

Instead of looking at 1,000 salaries individually, you can use mean, median, or mode to summarize the dataset with a few numbers.

Example: Employee salaries

Imagine you have 1,000 employees.

You could look at every salary:

40,000
42,000
45,000
...
...
150,000

That's difficult to understand quickly.

Instead, you calculate:

Mean   = 65,000
Median = 55,000
Mode   = 50,000

Now you immediately have an idea of what salaries are typical.

Why each one matters

1. Mean → "What's the average?"

Useful when you want the overall average.

Example:

What is the average salary in this company?

Excel:

=AVERAGE(C2:C1001)

You might discover:

Average salary = KSh 65,000

2. Median → "What's the middle?"

This is especially useful when your data contains extreme values (outliers).

Suppose salaries are:

30,000
35,000
40,000
45,000
500,000

Mean:

130,000

That doesn't really represent what most employees earn because the KSh 500,000 salary pulls the average upward.

Median:

40,000

The median gives you a better idea of the typical employee's salary.

3. Mode → "What's most common?"

Useful when you want to know the most frequently occurring value/category.

For example:

Male
Female
Female
Male
Female
Female

The most common category is:

Female

For numerical data:

50,000
45,000
50,000
60,000
50,000

Mode:

50,000

Why this matters in data analysis

Imagine your manager says:

"Analyze the salaries of our employees."

You don't want to just say:

"Here are 1,000 salary values."

You want to extract meaning from the data.

You could say:

"The average salary is KSh 65,000, while the median salary is KSh 55,000. The difference suggests that some higher salaries are pulling the average upward."

That's data analysis.

The most important thing to remember

Don't think:

"I need to memorize Mean, Median, and Mode because statistics says so."

Think:

"I need these tools to summarize my data and understand what a typical observation looks like."

And you'll use them constantly in data analytics, data science, Excel, Python, SQL, dashboards, and machine learning.

Simple mental model
Lots of data
     ↓
Mean / Median / Mode
     ↓
Simple summary
     ↓
Understand the dataset
     ↓
Make better decisions

Mean = average

Median = middle

Mode = most common

That's the core idea you need first.




## Mode is especially useful for categorical data

This is important for your data analytics learning.

Suppose:

| Employee | Department |
| -------- | ---------- |
| John     | IT         |
| Mary     | HR         |
| Peter    | IT         |
| Jane     | Finance    |
| David    | IT         |

You can't calculate a meaningful average of:

<pre class="overflow-visible! px-0!" data-start="1502" data-end="1541"><div class="relative w-full mt-4 mb-1"><div class=""><div class="contents"><div class="relative"><div class="h-full min-h-0 min-w-0"><div class="h-full min-h-0 min-w-0"><div class="border border-token-border-light border-radius-3xl corner-superellipse/1.1 rounded-3xl"><div class="h-full w-full border-radius-3xl bg-(--code-block-surface) corner-superellipse/1.1 overflow-clip rounded-3xl [--code-block-surface:var(--bg-elevated-secondary)] dark:[--code-block-surface:var(--composer-surface-primary)] lxnfua_clipPathFallback"><div class="pointer-events-none absolute end-1.5 top-1 z-2 md:end-2 md:top-1"></div><div class="relative"><div class="pe-11 pt-3"><div class="relative z-0 flex max-w-full"><div id="code-block-viewer" dir="ltr" class="q9tKkq_viewer cm-editor z-10 light:cm-light dark:cm-light flex h-full w-full flex-col items-stretch ͼs ͼ16"><div class="cm-scroller"><pre class="cm-content q9tKkq_readonly m-0"><code><span>IT + HR + IT + Finance + IT</span></code></pre></div></div></div></div></div></div></div></div></div><div class=""><div class=""></div></div></div></div></div></div></pre>

But you  **can find the mode** .

Mode = **IT**

So mode is particularly useful for finding the  **most common category** 



You need to know measures of spread because knowing the average alone doesn't tell you the whole story.

They tell you how much the data varies or how far the values are spread out.

Think about it this way

Imagine two companies have the same average salary:

Company A:

48K, 49K, 50K, 51K, 52K

Company B:

10K, 30K, 50K, 70K, 90K

Both have:

Mean = 50K

But they are clearly very different.

Company A salaries are close together.
Company B salaries are widely spread out.

That's what measures of spread help you see.

The main measures of spread

1. Range → "How far apart are the extremes?"
   Range = Maximum - Minimum

Example:

20, 30, 40, 50, 80

Range = 80 - 20
      = 60

It gives you a quick idea of the overall spread.

Excel:

=MAX(A2:A6)-MIN(A2:A6)
2. Variance → "How much do values vary from the mean?"

Variance measures the overall variability of the data.

You don't necessarily need to calculate it manually at first. In Excel:

=VAR.S(A2:A20)
3. Standard deviation → "How far are values typically from the mean?"

This is probably the most important measure of spread for you to understand.

Suppose:

Mean salary = KSh 50,000
Standard deviation = KSh 5,000

You know that salaries generally aren't extremely far from KSh 50,000.

But if:

Mean salary = KSh 50,000
Standard deviation = KSh 30,000

the salaries are much more spread out.

Excel:

=STDEV.S(A2:A20)
Why does this matter in real data analysis?

Imagine you're analyzing employee salaries.

You report:

Average salary = KSh 60,000

Your manager might ask:

"Are most employees actually earning around KSh 60,000?"

You cannot answer that from the mean alone.

You need a measure of spread.

For example:

Mean = KSh 60,000
Standard deviation = KSh 3,000

This suggests salaries are relatively close to the mean.

But:

Mean = KSh 60,000
Standard deviation = KSh 25,000

This tells you salaries vary much more.

Another important use: spotting unusual values

Suppose most employees earn:

45K, 48K, 50K, 52K, 55K

but one employee earns:

500K

The average will be affected heavily.

Measures of spread help you recognize that the dataset has large variability and potentially outliers.

Central tendency vs spread

This is the connection you should remember:

                 DESCRIPTIVE STATISTICS
                         │
              ┌──────────┴──────────┐
              ↓                     ↓
       CENTRAL TENDENCY          SPREAD
       "What's typical?"       "How variable?"
              │                     │
       Mean                    Range
       Median                  Variance
       Mode                    Standard deviation
In simple terms:

Central tendency tells you where the data is centered.

Measures of spread tell you how scattered the data is around that center.

You need both to properly understand a dataset.

For your data analytics learning, I'd prioritize understanding mean, median, mode, range, and standard deviation first. Variance is important too, but once you understand standard deviation, variance becomes much easier to understand.

you have used examples using standard devaition, use variance

Yes — let's use variance itself so you understand what it actually tells you.

Example: Employee salaries

Suppose five employees earn:

40, 45, 50, 55, 60 (thousand KSh)

First find the mean:

Mean = 50K

Now look at how far each salary is from the mean:

Salary	Difference from mean	Squared difference
40K	-10K	100
45K	-5K	25
50K	0K	0
55K	+5K	25
60K	+10K	100

We square the differences because otherwise the negative and positive differences would cancel each other out.

\(Var(X) = E(X^2) - [E(X)]^2\)
Var(X)=(1.4)
2
=1.96
σ
σ
μ
-σ
+σ
Var(X) ≈ 1.96
Give feedback

Now add the squared differences:

100 + 25 + 0 + 25 + 100 = 250

For this example, treating these five employees as the entire population:

Variance = 250 / 5 = 50

So the variance is 50 when salary is expressed in thousands of KSh.

What does that actually mean?

The important idea is:

Variance tells you how much the values are spread around the mean.

Now compare another company.

Company A

Salaries:

48, 49, 50, 51, 52

Mean = 50K

Variance = 2

Company B

Salaries:

30, 40, 50, 60, 70

Mean = 50K

Variance = 200

Both companies have the same average salary: 50K.

But:

Company A → variance = 2 → salaries are close together.
Company B → variance = 200 → salaries are much more spread out.

That's why you need variance.

The key relationship

Low variance → values are close to the mean.

High variance → values are far from the mean.

In Excel

If your salaries are in B2:B6:

For a population:

=VAR.P(B2:B6)

For a sample:

=VAR.S(B2:B6)

For your data-analysis learning, remember:

Variance answers: "How much does my data vary around its mean?"


Yes. Quartiles and the Interquartile Range (IQR) are also measures that help you understand the spread and position of your data. They are especially useful when your dataset contains outliers.

## * What is a Quartile?

A quartile divides your ordered data into four parts.

Think of a dataset arranged from smallest to largest:

Smallest ─────────────────────────────── Largest
        25%       25%       25%       25%
          │         │         │
         Q1        Q2        Q3

There are three important quartiles:

Quartile	Meaning
Q1	25% of the data is below this value
Q2	50% of the data is below this value — the median
Q3	75% of the data is below this value

So:

Q2 = Median

2. Simple Example

Suppose employee salaries are:

20K, 25K, 30K, 35K, 40K, 45K, 50K, 55K, 60K

They're already arranged from smallest to largest.

You can think of the quartiles as dividing the dataset into four sections.

Q1 tells you roughly where the first 25% ends.
Q2 tells you where the middle 50% point is.
Q3 tells you where the first 75% ends.

The exact quartile values depend on the calculation method used by your software, so when you're working in Excel, use Excel's quartile function rather than trying to estimate from the visual division.

## * What is the Interquartile Range?

This is the really important part.

IQR = Q3 − Q1

It measures the spread of the middle 50% of your data.

For example, suppose:

Q1 = 30K
Q3 = 50K

Then:

IQR = 50K - 30K
    = 20K

So the middle 50% of employees' salaries are spread across a KSh 20,000 range.

### * Why Is IQR Important?

The biggest advantage of IQR is that it is less affected by extreme values (outliers).

Imagine salaries are:

30K
35K
40K
45K
50K
55K
60K
500K

That 500K is extremely high compared with the others.

If you use the range:

500K - 30K = 470K

It makes the dataset appear extremely spread out.

But IQR focuses on the middle 50%, so that extreme salary has much less influence.

That's why IQR is particularly useful for datasets with outliers or skewed distributions.

### * IQR vs Range

This distinction is important.

Range

Uses:

Maximum − Minimum

So if you have:

10, 20, 30, 40, 100

Range:

100 - 10 = 90

The extreme value 100 has a huge effect.

IQR

Uses:

Q3 − Q1

It focuses on the middle 50%.

So:

Range → spread of the entire dataset

IQR → spread of the middle 50%

### * IQR vs Standard Deviation

This is another important comparison.

Standard deviation

Tells you how much the data tends to vary around the mean.

It's useful when the data is reasonably well-behaved and you're interested in variation around the average.

IQR

Tells you how spread out the middle 50% of the data is.

It's particularly useful when there are outliers or skewness.

So if you're analyzing salaries:

Mean + Standard deviation

can be useful.

But if a few executives earn extremely high salaries, you may also want:

### Median + IQR

because these are more resistant to extreme values.

7. Excel

If your salaries are in B2:B21:

Q1
=QUARTILE.INC(B2:B21,1)
Q2 / Median
=QUARTILE.INC(B2:B21,2)

or simply:

=MEDIAN(B2:B21)
Q3
=QUARTILE.INC(B2:B21,3)
IQR
=QUARTILE.INC(B2:B21,3)-QUARTILE.INC(B2:B21,1)
8. Why You Need to Know Quartiles and IQR

As a data analyst, you might be given a dataset and asked:

"Are there unusual values?"

Quartiles and IQR help you investigate this.

A common rule is:

Lower bound = Q1 - 1.5 × IQR

Upper bound = Q3 + 1.5 × IQR

Values below the lower bound or above the upper bound are commonly flagged as potential outliers.

Notice the word potential — being outside the boundary doesn't automatically mean the value is an error.

9. The Big Picture

Now you have several ways of describing your data:

CENTRAL TENDENCY
"What is typical?"
│
├── Mean
├── Median
└── Mode

SPREAD
"How much does it vary?"
│
├── Range
├── Variance
├── Standard deviation
└── IQR

POSITION
"Where does a value sit in the dataset?"
│
├── Quartiles
└── Percentiles
The easiest way to remember IQR:

Q1 = 25% point

Q2 = 50% point / Median

Q3 = 75% point

IQR = Q3 − Q1

And most importantly:

IQR tells you how spread out the middle 50% of your data is and is useful when outliers could distort measures like the range or mean.




## IQR Method for Detecting Outliers

* **IQR (Interquartile Range)** measures the spread of the middle 50% of the data.
* Formula:

  **IQR = Q3 − Q1**

### Outlier Boundaries

* **Lower Bound = Q1 − 1.5 × IQR**
* Used to identify unusually **low** values.
* A value **below the lower bound** is a potential low outlier.
* **Upper Bound = Q3 + 1.5 × IQR**
* Used to identify unusually **high** values.
* A value **above the upper bound** is a potential high outlier.

### Example

For:

`10, 12, 15, 18, 20, 22, 25, 27, 30, 100`

* Q1 = 15
* Q3 = 27
* IQR = 27 − 15 = **12**
* Lower Bound = 15 − (1.5 × 12) = **−3**
* Upper Bound = 27 + (1.5 × 12) = **45**

Since  **100 > 45** , 100 is a  **potential high outlier** .

### Important Data Analyst Note

> **An outlier is not automatically an error. Investigate why it is unusual before removing it.**

It could be:

* A data-entry error
* A legitimate extreme value
* A different type of employee/customer/product
* A genuine unusual observation

**Remember:**

🔽 Below Lower Bound → **Low outlier**

🔼 Above Upper Bound → **High outlier**


# MY CHEETSHEET

| Business question                        | Measure            |
| ---------------------------------------- | ------------------ |
| What's the average?                      | **Mean**     |
| What's the middle?                       | **Median**   |
| What's most common?                      | **Mode**     |
| How far apart are min and max?           | **Range**    |
| How much does data vary around the mean? | **Variance** |
| How spread out is the middle 50%?        | **IQR**      |
| Are there potential outliers?            | **IQR**      |
| Data has extreme values; what's typical? | **Median**   |
