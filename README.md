# Data Wrangling, Profiling, Cleaning, and Preparation

## Introduction

Data is rarely available in a perfect format. Real-world datasets often contain missing values, duplicate records, inconsistent formats, incorrect data types, and other quality issues. Before performing data analysis, visualization, or machine learning, data must be prepared properly.

Data wrangling, profiling, and cleaning are essential processes that help transform raw data into a reliable and analysis-ready dataset. These activities improve data quality, increase accuracy, and ensure trustworthy business decisions.

---

# 1. Data Wrangling

## What is Data Wrangling?

Data wrangling (also called data munging) is the process of collecting, organizing, cleaning, transforming, and preparing data for analysis.

The primary objective of data wrangling is to convert raw, unstructured, or inconsistent data into a structured format that can be easily analyzed.

### Why Data Wrangling is Important

- Improves data quality.
- Removes inconsistencies and errors.
- Makes datasets suitable for analysis and machine learning.
- Improves accuracy of reports and predictions.
- Reduces time spent handling data issues.
- Ensures reliable decision-making.

### Common Data Quality Problems

| Problem | Description |
|----------|-------------|
| Missing Values | Data is absent in some records. |
| Duplicate Records | Same information appears multiple times. |
| Inconsistent Data | Different formats for the same value. |
| Invalid Values | Values outside acceptable limits. |
| Incorrect Data Types | Numeric values stored as text. |
| Outliers | Extremely high or low values. |
| Formatting Issues | Mixed date or text formats. |

---

## Data Wrangling Process

### 1. Discover

The first step is understanding the dataset.

Activities include:
- Reviewing columns and attributes.
- Understanding business meaning.
- Identifying quality issues.
- Examining patterns and distributions.

### 2. Structure

Data is reorganized into a consistent format.

Examples:
- Splitting combined columns.
- Reshaping data.
- Converting data into tabular form.

### 3. Clean

Errors and inconsistencies are corrected.

Tasks include:
- Handling missing values.
- Removing duplicates.
- Correcting spelling mistakes.
- Standardizing formats.

### 4. Enrich

Additional information is added.

Examples:
- Creating new features.
- Merging datasets.
- Deriving useful attributes.

### 5. Validate

Checks are performed to ensure data quality.

Examples:
- Validating data types.
- Checking business rules.
- Ensuring consistency.

### 6. Publish

The cleaned dataset is saved and shared for analysis or machine learning.

---

# 2. Data Semantics

## What is Data Semantics?

Data semantics refers to the meaning and interpretation of data.

Understanding semantics helps analysts determine:
- What each field represents.
- Valid value ranges.
- Relationships between attributes.
- Business significance of data.

### Example

| Field | Data Type | Meaning |
|---------|-----------|---------|
| Student_ID | Integer | Unique identifier |
| Student_Name | String | Student name |
| Marks | Integer | Exam score |
| DOB | Date | Date of birth |

### Importance of Data Semantics

- Prevents incorrect interpretation.
- Supports data validation.
- Improves dataset consistency.
- Helps identify invalid records.
- Enables effective data governance.

---

# 3. Data Profiling

## What is Data Profiling?

Data profiling is the process of examining a dataset to understand its structure, content, quality, and relationships.

It helps identify problems before cleaning and analysis.

### Objectives of Data Profiling

- Understand data quality.
- Identify missing values.
- Detect duplicates.
- Discover relationships.
- Evaluate consistency.
- Support decision-making.

---

## Set-Based Profiling

Set-based profiling examines columns as collections of values.

### Distinct Values and Cardinality

Cardinality measures the number of unique values in a column.

**Low Cardinality Examples**
- Gender
- Department
- Category

**High Cardinality Examples**
- Employee ID
- Customer ID
- Email Address

### Frequency Distribution

Frequency distribution shows how often each value occurs.

| Department | Frequency |
|------------|-----------|
| IT | 40 |
| HR | 20 |
| Finance | 15 |
| Sales | 25 |

### Completeness Analysis

Determines how much data is available.

Completeness (%) = Available Values ÷ Total Values × 100

### Uniqueness Analysis

Determines whether a column can uniquely identify records.

Examples:
- Employee_ID → Unique
- Department → Not Unique

### Domain Validation

Verifies whether values belong to an allowed set.

Example:

Valid values for Gender:
- Male
- Female
- Other

Any other value is invalid.

---

# 4. Summary Statistics

Summary statistics provide a quick understanding of numerical data.

## Measures of Central Tendency

### Mean

Arithmetic average of all values.

### Median

Middle value after sorting the data.

### Mode

Most frequently occurring value.

### Comparison

| Measure | Best Used When |
|----------|----------------|
| Mean | Data is normally distributed |
| Median | Data contains outliers |
| Mode | Categorical data |

---

## Measures of Dispersion

### Range

Difference between maximum and minimum values.

### Variance

Measures spread around the mean.

### Standard Deviation

Indicates how far observations typically deviate from the mean.

### Quartiles

Divide data into four equal parts.

| Quartile | Meaning |
|----------|---------|
| Q1 | 25% of values below |
| Q2 | Median |
| Q3 | 75% of values below |

### Interquartile Range (IQR)

IQR = Q3 − Q1

Used for outlier detection.

---

## Skewness

Skewness measures asymmetry in a distribution.

### Positive Skew

Long tail on the right side.

### Negative Skew

Long tail on the left side.

### Symmetric Distribution

Left and right sides are approximately equal.

---

# 5. Profiling Missing Data

## What is Missing Data?

Missing data occurs when expected values are unavailable.

### Causes

- Manual entry errors.
- Device failures.
- Survey non-response.
- Data integration issues.

### Metrics Used

| Metric | Description |
|----------|-------------|
| Missing Count | Total missing records |
| Missing Percentage | Percentage missing |
| Column Completeness | Available values percentage |

### Impact of Missing Data

- Reduced accuracy.
- Biased analysis.
- Poor model performance.
- Incorrect conclusions.

---

# 6. Profiling Inconsistent Data

## What is Inconsistent Data?

Inconsistent data occurs when the same information appears in multiple formats.

### Examples

| Value Variations |
|------------------|
| Delhi |
| DELHI |
| delhi |

These values represent the same city but are stored differently.

### Common Causes

- Manual data entry.
- Different systems.
- Lack of standards.
- Data migration issues.

### Standardization Techniques

- Convert to uppercase.
- Convert to lowercase.
- Remove extra spaces.
- Replace abbreviations.
- Use reference dictionaries.

---

# 7. Correlation and Redundancy

## Correlation

Correlation measures the relationship between variables.

| Correlation Value | Interpretation |
|------------------|----------------|
| +1 | Perfect Positive |
| 0 | No Relationship |
| -1 | Perfect Negative |

### Benefits

- Identifies related variables.
- Supports feature selection.
- Helps in predictive modeling.

## Redundancy

Redundancy occurs when multiple columns contain similar information.

Problems:
- Increased storage.
- Unnecessary complexity.
- Multicollinearity issues in models.

---

# 8. Data Cleaning and Preparation

## What is Data Cleaning?

Data cleaning is the process of identifying and correcting errors, inconsistencies, duplicates, and missing values.

## What is Data Preparation?

Data preparation extends cleaning by transforming data into a format suitable for analysis and machine learning.

### Benefits

- Better analytical accuracy.
- Improved model performance.
- Consistent reporting.
- Faster data processing.

---

# 9. Missing Data Handling

## Types of Missing Data

### MCAR (Missing Completely at Random)

Missing values occur randomly and are unrelated to any variable.

### MAR (Missing at Random)

Missing values depend on other observed variables.

### MNAR (Missing Not at Random)

Missing values depend on the missing value itself.

---

## Hidden Missing Values

Missing values may be represented as:

- NA
- NULL
- Blank cells
- ?
- -999
- N/A

These should be converted into proper null values.

---

# 10. Removing Missing Data

Records with missing values can be removed when appropriate.

### Row Deletion

Remove rows containing missing values.

### Column Deletion

Remove columns with excessive missing data.

### Filter-Based Removal

Remove records that fail completeness requirements.

### Advantages

- Easy implementation.
- Improves data quality.

### Disadvantages

- Loss of information.
- Smaller dataset size.

---

# 11. Imputation Techniques

Imputation replaces missing values with estimated values.

| Technique | Description |
|------------|-------------|
| Mean | Replace with average value |
| Median | Replace with middle value |
| Mode | Replace with most frequent value |
| Constant | Replace with fixed value |
| Forward Fill | Use previous value |
| Backward Fill | Use next value |
| Interpolation | Estimate between nearby values |

### Choosing the Right Method

| Data Type | Recommended Method |
|------------|-------------------|
| Numeric without outliers | Mean |
| Numeric with outliers | Median |
| Categorical | Mode |
| Time Series | Forward Fill / Interpolation |

---

# 12. Duplicate Detection and Removal

## What are Duplicates?

Duplicates are records repeated one or more times in a dataset.

### Effects of Duplicates

- Inflated counts.
- Incorrect aggregations.
- Misleading trends.
- Poor data quality.

### Removal Process

1. Identify duplicate records.
2. Define comparison criteria.
3. Retain correct records.
4. Remove redundant entries.

---

# 13. Data Transformation Techniques

## Renaming Columns

Creates readable and standardized column names.

## Data Type Conversion

Converts data into suitable formats.

Examples:
- Text to Numeric
- Text to Date
- Numeric to Category

## Date Transformation

Useful derived attributes:

- Year
- Month
- Quarter
- Day
- Week Number

## Text Standardization

Common operations:

- Trim spaces.
- Convert case.
- Remove special characters.
- Correct spellings.

---

# Key Takeaways

- Data wrangling converts raw data into usable data.
- Data profiling helps understand quality and structure before analysis.
- Data semantics provides meaning to data attributes.
- Summary statistics describe data distributions.
- Missing values, duplicates, and inconsistencies are major data quality issues.
- Appropriate cleaning techniques improve business insights and machine learning performance.
- Imputation helps preserve data while handling missing values.
- Data preparation is a critical step in every analytics and AI project.
