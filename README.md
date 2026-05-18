# 🚓 Police Data Analysis using Python Pandas

## 📌 Project Introduction

This project is based on performing data analysis and preprocessing operations on a Police Dataset using Python and the Pandas library inside Jupyter Notebook. The dataset contains information related to traffic stops such as driver gender, age, violations, search conducted, stop duration, and other police stop details.

The main objective of this project is to understand how Python and Pandas are used in real-world police data analysis for cleaning, exploring, filtering, and analyzing structured datasets efficiently.

In this project, different data analysis techniques were implemented such as:

- Data Cleaning
- Handling Missing Values
- Data Filtering
- Statistical Analysis
- GroupBy Operations
- Traffic Violation Analysis
- Exploratory Data Analysis (EDA)

This project provides practical exposure to working with police datasets and understanding how data analysts use Python for extracting meaningful insights from real-world traffic stop data.

---

# 📂 Dataset Information

The dataset contains records of police traffic stops and driver-related information.

### Dataset Features:

- Driver Gender
- Driver Age
- Violation Type
- Search Conducted
- Stop Duration
- Speeding Details
- Traffic Stop Information

Each record in the dataset represents a specific police stop observation.

---

# 🛠️ Tools & Technologies Used

## 🐍 Python
Python was used as the programming language for performing data analysis and dataframe operations.

## 📊 Pandas
Pandas library was used for:
- Data Cleaning
- Data Manipulation
- Handling Missing Values
- Filtering Data
- Statistical Analysis
- GroupBy Operations

## 📓 Jupyter Notebook
Jupyter Notebook was used to execute Python code interactively and visualize outputs step-by-step.

---

# 🔍 Pandas Functions Implemented

## 🔹 import pandas as pd
Used to import the Pandas library.

### Syntax:
```python
import pandas as pd
```

---

## 🔹 pd.read_csv()
Used to import the CSV dataset into Jupyter Notebook.

### Syntax:
```python
data = pd.read_csv("Police_Data.csv")
```

---

## 🔹 head()
Displays the first 5 rows of the dataset.

### Syntax:
```python
data.head()
```

---

## 🔹 isnull().sum()
Detects missing/null values from each column.

### Syntax:
```python
data.isnull().sum()
```

---

## 🔹 drop()
Used to remove unnecessary columns from the dataset.

### Syntax:
```python
data.drop('column_name', axis=1)
```

---

## 🔹 value_counts()
Displays unique values along with their occurrence count.

### Syntax:
```python
data['violation'].value_counts()
```

---

## 🔹 groupby()
Groups data according to a specific column.

### Syntax:
```python
data.groupby('driver_gender')['search_conducted'].sum()
```

---

## 🔹 map()
Used to map and replace values in a column.

### Syntax:
```python
data['stop_duration'] = data['stop_duration'].map({
    '0-15 Min': 7.5,
    '16-30 Min': 23,
    '30+ Min': 45
})
```

---

## 🔹 mean()
Calculates the average value of a column.

### Syntax:
```python
data['stop_duration'].mean()
```

---

## 🔹 describe()
Displays statistical summary of grouped data.

### Syntax:
```python
data.groupby('violation').driver_age.describe()
```

---

# 📊 Tasks Performed in the Project

## ✅ Q1) Data Cleaning

### Task:
Remove the column that only contains missing values.

### Code Used:
```python
data.drop(columns=['country_name'], inplace=True)
```

### Explanation:
- Removes unnecessary columns
- Improves data quality
- Helps in better analysis

---

# 📊 Q2) Filtering & Value Counts Analysis

### Task:
For Speeding, were Men or Women stopped more often?

### Code Used:
```python
data[data.violation == 'Speeding'].driver_gender.value_counts()
```

### Explanation:
- Filters speeding violation records
- Counts male and female drivers separately
- Helps analyze traffic stop patterns

---

# 📊 Q3) GroupBy Analysis

### Task:
Does gender affect who gets searched during a stop?

### Code Used:
```python
data.groupby('driver_gender').search_conducted.sum()
```

### Explanation:
- Groups records by gender
- Calculates total searches conducted
- Useful for comparison analysis

---

# 📊 Q4) Mapping & Data Type Casting

### Task:
What is the mean stop duration?

### Code Used:
```python
data['stop_duration'] = data['stop_duration'].map({
    '0-15 Min': 7.5,
    '16-30 Min': 23,
    '30+ Min': 45
})

data['stop_duration'].mean()
```

### Explanation:
- Converts categorical duration into numeric values
- Calculates average stop duration
- Helps perform statistical analysis

---

# 📊 Q5) Age Distribution Analysis

### Task:
Compare the age distributions for each violation.

### Code Used:
```python
data.groupby('violation').driver_age.describe()
```

### Explanation:
- Groups records based on violation type
- Displays statistical summary of driver ages
- Helps understand age patterns across violations

---

# 📌 Important Insights

✔️ Pandas makes police data analysis simple and efficient.

✔️ GroupBy operations help compare driver and violation data.

✔️ Filtering records allows targeted traffic stop analysis.

✔️ Statistical analysis helps identify trends and patterns.

✔️ Missing values can be detected and handled easily using Pandas.

✔️ Real-world police datasets can be analyzed efficiently using Python.

---

# 📁 Project Structure

```text
├── Police_Data_Analysis.ipynb
├── Police_Data.csv
├── README.md
```

---

# 🎯 Final Conclusion

This project demonstrates how Python and Pandas can be used for real-world police data analysis and preprocessing tasks. Different operations such as handling missing values, filtering records, statistical analysis, grouping data, and extracting meaningful insights were successfully implemented.

Through this project, practical understanding was gained in:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Manipulation using Pandas
- Statistical Analysis
- GroupBy Operations
- Python-based Data Analytics

Overall, this project serves as a strong beginner-friendly foundation for learning Data Analysis and Data Science using Python.
