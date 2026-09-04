Approaches in Data Analysis
1. Overview of Data Analysis & Data Science Processes

Structured frameworks provide a systematic approach to investigating, cleaning, transforming, and analyzing data to discover meaningful patterns, relationships, and trends.

The Data Analysis Process

The typical data analysis process consists of:

Problem Statement
       ↓
Data Collection
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis (EDA)
       ↓
Gather Insights
1. Problem Statement

Define the problem, question, or hypothesis that needs to be investigated.

2. Data Collection

Find and acquire the relevant data needed to answer the question.

3. Data Cleaning

Identify and fix errors, missing values, duplicates, and inconsistencies in the raw data.

4. Exploratory Data Analysis (EDA)

Explore the dataset using statistics and visualizations to understand:

Distributions
Trends
Patterns
Relationships
Outliers
5. Gather Insights

Summarize the important findings and communicate them to stakeholders to support decision-making.

The Data Science Process

The data science process extends beyond traditional data analysis by including model building and deployment.

Problem Statement
       ↓
Data Collection
       ↓
Data Cleaning
       ↓
EDA
       ↓
Model Building
       ↓
Model Deployment
Model Building

The process of:

Selecting relevant features
Choosing an appropriate algorithm
Training the model
Evaluating model performance
Improving the model iteratively
Model Deployment

Integrating a trained model into a production environment, application, or business system so that it can make predictions or provide useful outputs using new data.

Common frameworks for organizing the data science process include OSEMN and CRISP-DM.

2. Types of Data Analysis

There are two broad approaches to analyzing data: quantitative and qualitative analysis.

Type	Definition	Examples / Uses
Quantitative Analysis	Analyzes numerical data using mathematical and statistical techniques	Hypothesis testing, measuring relationships, identifying patterns, statistical modeling
Qualitative Analysis	Analyzes non-numerical data to identify themes, meanings, and patterns	Understanding opinions, attitudes, experiences, and human behavior
Quantitative Analysis

Quantitative analysis works primarily with numbers.

For example:

Age: 25
Salary: 50,000
Sales: 1,250
Temperature: 24.5°C

A data analyst might calculate:

Mean
Median
Standard deviation
Correlation
Percentages
Statistical significance
Qualitative Analysis

Qualitative analysis focuses on information that isn't naturally represented as numerical measurements.

Examples include:

Interview responses
Customer reviews
Written feedback
Images
Videos
Open-ended survey responses

The goal is often to identify themes, opinions, attitudes, or underlying reasons.

3. Detailed Process Steps & Key Concepts
A. Problem Statement

A problem statement identifies the gap between the current state and the desired state.

A good problem statement should be:

Specific
Clear
Concise
Unbiased
Measurable
Forms of a Problem Statement

A problem can be expressed as:

General statement:

Sales have decreased significantly.

Specific question:

Why did sales decrease during the third quarter?

Hypothesis:

A decrease in marketing expenditure caused the decline in sales.

A hypothesis is a proposed explanation or relationship that can be tested using data.

B. Data Collection

Data collection involves acquiring the data required to investigate the problem.

Data can come from internal or external sources.

Surveys

Used to collect information directly from people.

Examples:

Customer satisfaction surveys
Employee surveys
Market research
Databases & APIs

Data can be retrieved from:

Organizational databases
Sales systems
Customer management systems
APIs

For example, a data analyst might use SQL to query a company's sales database.

Open Sources

Data can also come from publicly available sources such as:

Public datasets
Government databases
Census data
Cloud repositories
Research datasets
C. Data Cleaning / Data Wrangling

Data cleaning is the process of transforming raw data into a usable, consistent, and high-quality dataset.

Common problems include:

Missing values
Duplicate records
Incorrect data types
Inconsistent formatting
Irrelevant observations
Outliers
Structural problems
Example

Raw data:

Name      Age    Salary
John      25     50000
Mary      ?      60000
John      25     50000
Peter     30     70000

There is a missing age and a duplicate John record.

After cleaning:

Name      Age    Salary
John      25     50000
Mary      27     60000
Peter     30     70000
Tools

Common tools and techniques include:

Python
Pandas
SQL
Spreadsheets
Power BI
Regular expressions (regex)

Regex can be particularly useful for identifying and cleaning patterns in text data.

D. Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) is the process of examining a dataset to understand its main characteristics, patterns, distributions, and relationships.

EDA uses both statistics and visualizations.

There are two important approaches:

Univariate analysis
Multivariate analysis
Univariate Analysis

Univariate analysis examines one variable at a time.

For example:

What is the distribution of customer ages?

Non-Graphical Analysis

Common statistical measures include:

Measures of central tendency:

Mean
Median
Mode

Measures of dispersion/distribution:

Range
Variance
Standard deviation
Kurtosis
Graphical Analysis

Common visualizations include:

Histograms
Density plots
Box plots

Example:

Age
│
│       ███
│    ███████
│  ███████████
│██████████████
└────────────────
  20  30  40  50
Multivariate Analysis

Multivariate analysis examines relationships between two or more variables.

For example:

Is there a relationship between advertising expenditure and sales?

Non-Graphical Analysis

A common technique is correlation analysis.

For example, the Pearson correlation coefficient measures the strength and direction of a linear relationship between two numerical variables.

Its value ranges from:

-1 ───────── 0 ───────── +1
+1 → Perfect positive linear relationship
0 → No linear relationship
-1 → Perfect negative linear relationship
Graphical Analysis

Common visualizations include:

Scatter plots
Heatmaps
Pair plots
Violin plots
E. Gathering & Reporting Insights

After analyzing the data, the findings need to be communicated to stakeholders.

Common methods include:

Dashboards
Reports
Presentations
Charts
Data visualizations

For example:

Raw Data
   ↓
Analysis
   ↓
Findings
   ↓
Visualization
   ↓
Business Insight
   ↓
Decision

The goal isn't simply to produce charts. The goal is to communicate useful insights that can support decisions.

4. The 4 Levels of Analytics

The four major levels of analytics describe how organizations move from understanding the past to deciding what to do next.

Descriptive
    ↓
Diagnostic
    ↓
Predictive
    ↓
Prescriptive
1. Descriptive Analytics — "What happened?"

Descriptive analytics summarizes historical data.

Example:

Sales decreased by 15% in July.

Common tools:

Reports
Dashboards
Historical summaries
Charts

Purpose: Understand what has already happened.

2. Diagnostic Analytics — "Why did it happen?"

Diagnostic analytics investigates the causes behind an observed outcome.

Example:

Sales decreased because product availability fell by 20% and marketing expenditure was reduced.

Common techniques:

Data mining
Drill-down analysis
Root-cause analysis
Correlation analysis

Purpose: Understand why something happened.

3. Predictive Analytics — "What will happen?"

Predictive analytics uses historical data, statistics, and machine learning to estimate future outcomes.

Example:

Based on historical patterns, sales are expected to increase by 10% next month.

Common techniques:

Statistical models
Machine learning
Regression
Time-series forecasting

Purpose: Predict what is likely to happen.

4. Prescriptive Analytics — "What should we do?"

Prescriptive analytics goes one step further by recommending actions that could produce the best outcome.

Example:

Increase inventory by 15% and increase advertising expenditure by 10% to maximize expected revenue.

Common techniques:

Optimization algorithms
Decision models
Simulation
Recommendation systems

Purpose: Determine what action should be taken.

The Four Levels Together
Level	Question	Main Purpose
Descriptive	What happened?	Understand the past
Diagnostic	Why did it happen?	Find causes
Predictive	What will happen?	Forecast the future
Prescriptive	What should we do?	Recommend actions

A useful way to remember them:

Descriptive → Diagnostic → Predictive → Prescriptive
What → Why → What next → What should we do?

5. Modeling Frameworks & Libraries

Data scientists use specialized libraries and frameworks to perform statistical analysis, machine learning, and deep learning.

Machine Learning

Scikit-learn

Used for traditional machine learning tasks such as:

Linear regression
Logistic regression
Decision trees
Random forests
Clustering
Feature preprocessing
Model evaluation

TensorFlow

A machine learning framework that can be used for building and training neural networks and other machine learning models.

Deep Learning

PyTorch

A deep learning framework commonly used for:

Neural networks
Computer vision
Natural language processing
Research and machine learning applications

Keras

A high-level deep learning API commonly used to build and train neural networks.

The Complete Data Analysis Picture
                    PROBLEM
                       ↓
                 DATA COLLECTION
                       ↓
                  DATA CLEANING
                       ↓
                      EDA
                       ↓
              ┌────────┴────────┐
              ↓                 ↓
       DESCRIPTIVE         DIAGNOSTIC
       What happened?      Why?
              ↓                 ↓
              └────────┬────────┘
                       ↓
                  PREDICTIVE
                 What next?
                       ↓
                 PRESCRIPTIVE
              What should we do?
                       ↓
                 DECISION / ACTION

Key idea: Data analysis primarily helps us understand data and discover insights, while data science can go further by using statistical and machine-learning models to predict outcomes and deploy solutions into real-world systems.