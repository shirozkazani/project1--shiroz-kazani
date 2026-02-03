# Week 3 Assignment: Chronic Kidney Disease Dataset Analysis

## I 320D: Data Science for Biomedical Informatics | Spring 2026

### 📋 Assignment Version D

---

## 🎯 This Week's Mantra

> **"Every Column Tells a Story"**

In this assignment, you'll apply the 10-Point Data Inspection to a real-world healthcare dataset focused on chronic kidney disease (CKD) prediction. By the end, you'll understand not just *what* the data contains, but *why* each variable matters for clinical decision-making.

---

## Learning Objectives

By completing this assignment, you will be able to:

1. ✅ Apply the systematic 10-Point Inspection to a new healthcare dataset
2. ✅ Identify and classify feature types (continuous, discrete, categorical, ordinal)
3. ✅ Detect and document data quality issues (missing values, unexpected values)
4. ✅ Research and document clinical meaning for healthcare variables
5. ✅ Create meaningful data groupings based on clinical standards
6. ✅ Formulate answerable research questions about kidney disease risk factors

---

## About the Dataset

**Dataset:** Chronic Kidney Disease Dataset  
**Source:** UCI Machine Learning Repository  
**File:** `kidney_disease.csv`  
**Target Variable:** `classification` (whether the patient has chronic kidney disease - ckd or notckd)

### Clinical Context

Chronic Kidney Disease (CKD) affects approximately 15% of adults in the United States. It is a condition where the kidneys gradually lose function over time. Early detection is crucial because:

- CKD often has no symptoms until advanced stages
- It is a major risk factor for cardiovascular disease
- Early intervention can slow disease progression
- It helps in planning dialysis or transplant if needed

This dataset contains clinical measurements that healthcare professionals use to diagnose and monitor kidney function.

---

## Getting Started

First, load the dataset and import your libraries:

```python
# Import libraries


# Load the dataset


# Display first few rows to confirm it loaded

```

---

## Part 1: The 10-Point Data Inspection (40 points)

Complete each inspection step and document your findings.

### Step 1: Shape (4 points)

**Your Code:**
```python

```

**Your Findings:**
- How many rows (observations)? _______________
- How many columns (features)? _______________
- What does each row represent in clinical terms? _______________

---

### Step 2: Column Names (4 points)

**Your Code:**
```python

```

**Your Findings:**
- List all column names:

- Which columns use medical abbreviations that might need further research to understand?

---

### Step 3: Data Types (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns are numeric?

- Which columns are categorical (object/string)?

- Are there any data types that seem incorrect? (Hint: Look at columns that should be numeric but might be stored as objects)

---

### Step 4: First Look (4 points)

**Your Code:**
```python

```

**Your Findings:**
- What do the actual values look like?

- Do you notice any unusual or unexpected values?

- Are there any values that look like they might be placeholders for missing data?

---

### Step 5: Last Look (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Does the data end cleanly?

- Are the last rows consistent with the first rows?

- Do you notice any difference in the `classification` values between the beginning and end of the dataset?

---

### Step 6: Memory Usage (4 points)

**Your Code:**
```python

```

**Your Findings:**
- How much memory does the dataset use? _______________ KB
- Is this a "small" or "large" dataset by data science standards?

---

### Step 7: Missing Values (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns have the most missing values?

- What percentage of each column is missing?

- ⚠️ **IMPORTANT:** This dataset has many columns with missing values. Which clinical measurements seem to have the most missing data? Why might certain lab tests be missing more often than others?

---

### Step 8: Duplicates (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Are there any duplicate rows? _______________
- Are all patient IDs unique? _______________

---

### Step 9: Basic Statistics (4 points)

**Your Code:**
```python

```

**Your Findings:**
- What is the age range in the dataset? _______________ to _______________
- What is the range of blood pressure (bp) values? _______________ to _______________
- What is the range of hemoglobin (hemo) values? _______________ to _______________
- Do any min/max values seem impossible or clinically unlikely?

---

### Step 10: Unique Counts (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns have very few unique values (likely categorical)?

- Which columns have many unique values (likely continuous or IDs)?

- Does the number of unique IDs match the number of rows? _______________

---

## Part 2: Data Dictionary (20 points)

Complete the following data dictionary. For each column, you must:
1. **Research** the clinical meaning (many columns use medical abbreviations)
2. **Identify** the feature type (Continuous, Discrete, Categorical-Nominal, Categorical-Ordinal, Binary, Identifier)
3. **Document** the valid values/range you observe
4. **Note** any issues or questions

| Column | Full Name / Description | Feature Type | Valid Values/Range | Notes/Issues |
|--------|------------------------|--------------|-------------------|--------------|
| `id` | | | | |
| `age` | | | | |
| `bp` | Blood Pressure (mm Hg) | | | |
| `sg` | Specific Gravity (urine) | | | |
| `al` | Albumin (urine) | | | |
| `su` | Sugar (urine) | | | |
| `rbc` | Red Blood Cells (urine) | | | |
| `pc` | Pus Cells (urine) | | | |
| `pcc` | Pus Cell Clumps | | | |
| `ba` | Bacteria | | | |
| `bgr` | Blood Glucose Random (mg/dL) | | | |
| `bu` | Blood Urea (mg/dL) | | | |
| `sc` | Serum Creatinine (mg/dL) | | | |
| `sod` | Sodium (mEq/L) | | | |
| `pot` | Potassium (mEq/L) | | | |
| `hemo` | Hemoglobin (g/dL) | | | |
| `pcv` | Packed Cell Volume | | | |
| `wc` | White Blood Cell Count (cells/cumm) | | | |
| `rc` | Red Blood Cell Count (millions/cmm) | | | |
| `htn` | Hypertension | | | |
| `dm` | Diabetes Mellitus | | | |
| `cad` | Coronary Artery Disease | | | |
| `appet` | Appetite | | | |
| `pe` | Pedal Edema | | | |
| `ane` | Anemia | | | |
| `classification` | | | | |

### Clinical Research Questions for Version D

Answer these questions based on your research (you may need to use Google):

**1. What is blood glucose random (bgr) testing and how does it differ from fasting glucose? What do elevated random glucose levels indicate?**

Your answer:

---

**2. What is the relationship between sodium (sod) and potassium (pot) levels and kidney function? Why are electrolyte imbalances dangerous in CKD?**

Your answer:

---

**3. What is packed cell volume (pcv) and how does it relate to hemoglobin? Why might both be affected in CKD patients?**

Your answer:

---

**4. What does "appetite" (appet - good vs. poor) tell us about a CKD patient's condition? Why do kidney disease patients often experience appetite changes?**

Your answer:

---

## Part 3: Data Validation (15 points)

### 3.1 Age Validation (5 points)

Write code to check:
- How many ages are below 0?
- How many ages are above 120?
- What is the actual age range?
- How is age distributed across the dataset?

**Your Code:**
```python

```

**Your Findings:**

- Are there any impossible age values?

- What is the most common age range of patients in this dataset?

- Does the age distribution make clinical sense for a kidney disease dataset?

---

### 3.2 Blood Glucose Random (bgr) Validation (5 points)

Blood glucose random testing can be done at any time. Normal is typically <140 mg/dL. Values ≥200 mg/dL with symptoms suggest diabetes.

Write code to examine blood glucose values closely.

**Your Code:**
```python

```

**Your Findings:**

- What is the range of blood glucose values in this dataset?

- How many patients have extremely elevated glucose (>300 mg/dL)?

- What might extremely high blood glucose values indicate clinically?

- Are there any missing values? How might you handle them?

---

### 3.3 Classification Target Variable Validation (5 points)

Write code to see all unique values and their counts for the classification column.

**Your Code:**
```python

```

**Your Findings:**

- What are all the possible classification values?

- Are there any data quality issues with the classification values (look carefully at spacing, etc.)?

- How many patients have CKD vs. do not have CKD?

- Is the dataset balanced or imbalanced?

---

## Part 4: Create Clinical Blood Glucose Groups (10 points)

Create a new column called `glucose_category` that categorizes patients into clinically-meaningful blood glucose groups.

### Version D: Glycemic Status Classification

Use these categories based on random blood glucose levels:

| Glucose Category | Range (mg/dL) | Clinical Rationale |
|-----------------|---------------|-------------------|
| Hypoglycemic | <70 | Low blood sugar, potentially dangerous |
| Normal | 70-139 | Healthy glucose range |
| Prediabetic Range | 140-199 | Impaired glucose tolerance, increased diabetes risk |
| Diabetic Range | 200-299 | Suggests diabetes, confirmation testing needed |
| Severely Elevated | 300+ | Dangerous levels, urgent medical attention needed |

### Your Code:

```python
# First, handle any missing bgr values if present
# Then create the glucose_category column
# You can use a custom function with .apply() OR pd.cut()
# Remember: if using pd.cut(), you may need to handle NaN values first!


```

### Verify your groupings worked:

```python
# Show counts per glucose category

```

### Calculate CKD rate by glucose category:

```python
# Calculate the percentage of patients who have CKD in each glucose category
# Note: you may need to clean the classification column first!

```

### Analysis Questions:

**1. How many patients are in each glucose category?**

Your answer:

---

**2. What is the CKD rate (percentage) for each glucose category?**

Your answer:

---

**3. Is there a relationship between blood glucose levels and CKD prevalence? Does this match what you learned in your clinical research about diabetes and kidney disease?**

Your answer:

---

## Part 5: Research Questions (15 points)

### 5.1 Write Three Answerable Questions (9 points)

Write three questions that THIS dataset can answer. Remember: the data can show relationships and patterns, but cannot prove causation.

**Your questions must explore these specific areas:**

1. **A question about serum creatinine levels and CKD:**


---

2. **A question comparing patients with good appetite vs. poor appetite:**


---

3. **A question about the combination of diabetes AND coronary artery disease:**


---

### 5.2 Identify One Question the Data CANNOT Answer (3 points)

Write one question about **genetic or family history factors** that this dataset cannot answer, and explain why.

**Question:**


**Why it cannot be answered with this data:**


---

### 5.3 Grouping Analysis (3 points)

Answer this question using a groupby analysis:

**"What is the average blood glucose level for patients with CKD vs. patients without CKD?"**

(Note: You'll need to handle missing values and clean the classification column first!)

**Your Code:**
```python

```

**Your Interpretation:**

What is the difference in average blood glucose between CKD and non-CKD patients? Why does this make clinical sense given the relationship between diabetes and kidney disease?


---

## Part 6: Target Variable Analysis (Bonus - 5 points)

The `classification` column is our **target variable** - what we're trying to predict. Analyze its distribution.

**Your Code:**
```python
# Show the count and percentage of CKD vs non-CKD
# Make sure to clean any data quality issues first!

```

### Bonus Questions:

**1. What percentage of patients in this dataset have CKD?**

Your answer:

---

**2. Is this dataset balanced or imbalanced?**

Your answer:

---

**3. Why does class imbalance matter for machine learning? (You may need to research this)**

Your answer:

---

**4. In the real world, would you expect CKD rates to be this high or this low? What might this tell you about how this dataset was collected?**

Your answer:

---

## Submission Checklist

Before submitting, verify you have completed:

- [ ] **Part 1:** All 10 inspection steps with code AND written findings
- [ ] **Part 2:** Complete data dictionary with all 26 columns filled in
- [ ] **Part 2:** Answered all 4 clinical research questions
- [ ] **Part 3:** All 3 validation checks with code and answers
- [ ] **Part 4:** Created `glucose_category` column using the **Glycemic Status Classification**
- [ ] **Part 4:** Calculated CKD rate by glucose category with interpretation
- [ ] **Part 5:** Three research questions (serum creatinine, appetite, diabetes+CAD)
- [ ] **Part 5:** One unanswerable question about genetic/family history factors
- [ ] **Part 5:** Blood glucose groupby analysis
- [ ] **Bonus (Optional):** Target variable analysis

---

## Grading Rubric

| Component | Points | Requirements for Full Credit |
|-----------|--------|------------------------------|
| Part 1: 10-Point Inspection | 40 | All 10 steps complete with working code AND thoughtful written analysis |
| Part 2: Data Dictionary | 20 | All 26 columns documented with correct feature types and clinical research |
| Part 3: Data Validation | 15 | All validation checks complete with working code and insightful answers |
| Part 4: Blood Glucose Groups | 10 | Working code that creates correct groups AND meaningful interpretation |
| Part 5: Research Questions | 15 | Three good questions in specified areas, one clear limitation, groupby analysis complete |
| **Bonus:** Target Analysis | +5 | Thoughtful analysis of class imbalance with real-world connection |
| **Total** | 100 (+5 bonus) | |

---

## Hints (Read Before You Get Stuck!)

### ⚠️ Common Pitfalls:

1. **Many columns have missing values** - this dataset has significant missing data across multiple clinical measurements. Use `isnull().sum()` to get a complete picture.

2. **Some numeric columns may be stored as objects** - check your data types carefully. You may need to convert columns before doing calculations.

3. **The classification column has data quality issues** - look carefully at the unique values. You might see inconsistent spacing or formatting that needs cleaning.

4. **Categorical columns use abbreviations** - values like 'ckd', 'notckd', 'normal', 'abnormal' need to be understood in clinical context.

5. **Tab characters and whitespace** - some values may have hidden whitespace. Use `.str.strip()` when cleaning.

### 💡 Pro Tips:

- Use `value_counts()` liberally to understand categorical columns
- Use `value_counts(dropna=False)` to see if there are null values
- When something seems weird, investigate it—don't assume it's an error
- Use `.unique()` to see all possible values in a column
- Consider using `.str.strip()` to clean whitespace from string columns
- Always state what the data CAN tell you vs. what would require additional information

---

## Useful Resources

- **UCI Dataset Page:** https://archive.ics.uci.edu/ml/datasets/chronic_kidney_disease
- **National Kidney Foundation:** https://www.kidney.org/atoz/content/about-chronic-kidney-disease
- **American Diabetes Association:** https://diabetes.org/about-diabetes/diagnosis
- **Lab Test Interpretations:** https://labtestsonline.org/
- **Pandas Documentation:** https://pandas.pydata.org/docs/

---

*Remember: "Every Column Tells a Story" - your job is to figure out what that story is!*

---

**Due Date:** [See Canvas]

**Submission:** Upload your completed Jupyter notebook (.ipynb) to Canvas
