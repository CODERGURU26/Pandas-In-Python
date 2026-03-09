# 🐼 Pandas-In-Python

A comprehensive collection of Jupyter notebooks demonstrating essential Pandas operations and techniques for data analysis in Python.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

---

## 📑 Table of Contents

- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Topics Covered](#topics-covered)
- [Installation](#installation)
- [Usage](#usage)
- [Module Details](#module-details)
- [Prerequisites](#prerequisites)
- [Learning Path](#learning-path)
- [Key Concepts](#key-concepts)
- [Contributing](#contributing)
- [Author](#author)

---

## 🎯 Project Overview

This repository serves as a complete learning resource for mastering Pandas, Python's most powerful library for data manipulation and analysis. Whether you're a beginner starting your data science journey or an experienced analyst looking to refine your skills, this collection covers everything from basic operations to advanced techniques.

**What is Pandas?**
Pandas is a fast, powerful, flexible, and easy-to-use open-source data analysis and manipulation tool built on top of Python. It provides data structures like DataFrame and Series that make working with structured data intuitive and efficient.

---

## 📂 Repository Structure

```
Pandas-In-Python/
│
├── Data Cleaning In Pandas/
│   └── Techniques for handling missing data, duplicates, and data quality issues
│
├── EDA in Pandas/
│   └── Exploratory Data Analysis techniques and statistical summaries
│
├── Filtering rows & columns in pandas/
│   └── Boolean indexing, loc, iloc, and advanced filtering methods
│
├── Group By & Aggregations In Pandas/
│   └── Grouping data and performing aggregate operations
│
├── Indexing In Pandas/
│   └── Working with indexes, multi-indexing, and index operations
│
├── Merging DataFrames in Pandas/
│   └── Joining, merging, and concatenating datasets
│
├── Reading files in pandas/
│   └── Loading data from CSV, Excel, JSON, SQL, and other formats
│
├── Visualization In Pandas/
│   └── Creating plots and charts directly from DataFrames
│
└── README.md
    └── Project documentation (this file)
```

---

## 📚 Topics Covered

### 1. 📖 **Reading Files in Pandas**
Learn to import data from various sources:
- CSV files (`pd.read_csv()`)
- Excel files (`pd.read_excel()`)
- JSON files (`pd.read_json()`)
- SQL databases (`pd.read_sql()`)
- HTML tables (`pd.read_html()`)
- Clipboard data (`pd.read_clipboard()`)

### 2. 🔍 **Filtering Rows & Columns**
Master data selection and filtering:
- Boolean indexing
- `.loc[]` - label-based indexing
- `.iloc[]` - integer-based indexing
- `.query()` method
- Conditional filtering
- Column selection techniques

### 3. 📊 **Indexing in Pandas**
Understand index operations:
- Setting and resetting indexes
- Multi-level indexing (MultiIndex)
- Index alignment
- Reindexing
- Index-based operations

### 4. 🧹 **Data Cleaning**
Essential data cleaning techniques:
- Handling missing values (`dropna()`, `fillna()`)
- Removing duplicates (`drop_duplicates()`)
- Data type conversions (`astype()`)
- String operations and cleaning
- Outlier detection and handling
- Data validation

### 5. 🔗 **Merging DataFrames**
Combine datasets effectively:
- `merge()` - SQL-style joins
- `concat()` - concatenation
- `join()` - index-based joining
- Inner, outer, left, right joins
- Handling merge conflicts

### 6. 📈 **Group By & Aggregations**
Powerful grouping and aggregation:
- `groupby()` operations
- Aggregation functions (sum, mean, count, etc.)
- Multiple aggregations
- Custom aggregation functions
- Transform and filter operations
- Pivot tables and crosstabs

### 7. 🔬 **Exploratory Data Analysis (EDA)**
Statistical analysis and exploration:
- Descriptive statistics (`describe()`)
- Data profiling
- Correlation analysis
- Distribution analysis
- Summary statistics
- Data insights extraction

### 8. 📉 **Visualization in Pandas**
Create visualizations directly from DataFrames:
- Line plots
- Bar charts
- Histograms
- Scatter plots
- Box plots
- Pie charts
- Integration with Matplotlib

---

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Required Libraries

```bash
# Install Pandas
pip install pandas

# Install additional dependencies
pip install numpy matplotlib jupyter openpyxl xlrd

# Or install all at once
pip install pandas numpy matplotlib jupyter openpyxl xlrd seaborn
```

### Clone the Repository

```bash
git clone https://github.com/CODERGURU26/Pandas-In-Python.git
cd Pandas-In-Python
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

---

## 💻 Usage

### Quick Start

1. **Navigate to a topic folder**
   - Choose the concept you want to learn (e.g., "Data Cleaning In Pandas")

2. **Open the Jupyter Notebook**
   - Double-click the `.ipynb` file

3. **Run the cells**
   - Execute cells sequentially using `Shift + Enter`
   - Experiment with the code
   - Modify examples to reinforce learning

4. **Practice with your own data**
   - Apply techniques to your datasets
   - Combine multiple concepts

---

## 📖 Module Details

### 📖 Reading Files in Pandas

**What you'll learn:**
- Loading different file formats
- Handling encoding issues
- Parsing dates
- Dealing with large files
- Optimizing data loading

**Example:**
```python
import pandas as pd

# Read CSV file
df = pd.read_csv('data.csv')

# Read Excel with specific sheet
df = pd.read_excel('data.xlsx', sheet_name='Sheet1')

# Read JSON
df = pd.read_json('data.json')

# Read from SQL database
import sqlite3
conn = sqlite3.connect('database.db')
df = pd.read_sql('SELECT * FROM table', conn)
```

---

### 🔍 Filtering Rows & Columns

**What you'll learn:**
- Selecting specific columns
- Filtering rows based on conditions
- Complex boolean operations
- Query syntax

**Example:**
```python
# Select columns
df[['Name', 'Age']]

# Filter rows
df[df['Age'] > 25]

# Multiple conditions
df[(df['Age'] > 25) & (df['City'] == 'New York')]

# Using loc
df.loc[df['Age'] > 25, ['Name', 'Salary']]

# Using iloc
df.iloc[0:10, 0:3]

# Using query
df.query('Age > 25 and City == "New York"')
```

---

### 📊 Indexing in Pandas

**What you'll learn:**
- Setting custom indexes
- Multi-level indexes
- Index operations
- Resetting and reindexing

**Example:**
```python
# Set index
df.set_index('ID', inplace=True)

# Reset index
df.reset_index(inplace=True)

# Multi-index
df.set_index(['Year', 'Month'])

# Access by index
df.loc['index_label']

# Sort by index
df.sort_index()
```

---

### 🧹 Data Cleaning

**What you'll learn:**
- Identifying missing values
- Handling null data
- Removing duplicates
- Data type corrections
- String cleaning

**Example:**
```python
# Check for missing values
df.isnull().sum()

# Drop missing values
df.dropna()

# Fill missing values
df.fillna(0)
df.fillna(df.mean())

# Remove duplicates
df.drop_duplicates()

# Convert data types
df['Age'] = df['Age'].astype(int)

# String operations
df['Name'] = df['Name'].str.upper()
df['Name'] = df['Name'].str.strip()
```

---

### 🔗 Merging DataFrames

**What you'll learn:**
- Different types of joins
- Merging on columns
- Concatenating DataFrames
- Handling merge conflicts

**Example:**
```python
# Inner join
pd.merge(df1, df2, on='ID', how='inner')

# Left join
pd.merge(df1, df2, on='ID', how='left')

# Outer join
pd.merge(df1, df2, on='ID', how='outer')

# Concatenate vertically
pd.concat([df1, df2], axis=0)

# Concatenate horizontally
pd.concat([df1, df2], axis=1)

# Join on index
df1.join(df2)
```

---

### 📈 Group By & Aggregations

**What you'll learn:**
- Grouping data
- Aggregation functions
- Multiple aggregations
- Custom functions
- Pivot tables

**Example:**
```python
# Simple groupby
df.groupby('Category')['Sales'].sum()

# Multiple aggregations
df.groupby('Category').agg({
    'Sales': ['sum', 'mean', 'count'],
    'Profit': 'sum'
})

# Custom aggregation
df.groupby('Category')['Sales'].agg(lambda x: x.max() - x.min())

# Pivot table
df.pivot_table(
    values='Sales',
    index='Category',
    columns='Year',
    aggfunc='sum'
)

# Transform
df['Sales_Pct'] = df.groupby('Category')['Sales'].transform(lambda x: x / x.sum())
```

---

### 🔬 Exploratory Data Analysis (EDA)

**What you'll learn:**
- Statistical summaries
- Data profiling
- Correlation analysis
- Distribution analysis
- Identifying patterns

**Example:**
```python
# Basic info
df.info()
df.describe()

# Value counts
df['Category'].value_counts()

# Correlation matrix
df.corr()

# Unique values
df['Category'].nunique()

# Cross-tabulation
pd.crosstab(df['Category'], df['Region'])

# Statistical measures
df['Sales'].mean()
df['Sales'].median()
df['Sales'].std()
df['Sales'].quantile([0.25, 0.5, 0.75])
```

---

### 📉 Visualization in Pandas

**What you'll learn:**
- Creating plots from DataFrames
- Different plot types
- Customizing visualizations
- Integration with Matplotlib

**Example:**
```python
import matplotlib.pyplot as plt

# Line plot
df.plot(x='Date', y='Sales', kind='line')

# Bar chart
df.groupby('Category')['Sales'].sum().plot(kind='bar')

# Histogram
df['Age'].plot(kind='hist', bins=20)

# Scatter plot
df.plot(x='Age', y='Salary', kind='scatter')

# Box plot
df.boxplot(column='Sales', by='Category')

# Pie chart
df['Category'].value_counts().plot(kind='pie')

# Multiple plots
df.plot(subplots=True, figsize=(10, 8))
plt.show()
```

---

## 🎓 Key Concepts

### DataFrame vs Series

**DataFrame:**
- 2-dimensional labeled data structure
- Think of it as a spreadsheet or SQL table
- Columns can have different data types

**Series:**
- 1-dimensional labeled array
- Single column of a DataFrame
- Homogeneous data type

```python
# Create Series
s = pd.Series([1, 2, 3, 4, 5])

# Create DataFrame
df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6],
    'C': [7, 8, 9]
})
```

### Common Pandas Operations Cheat Sheet

| Operation | Syntax | Description |
|-----------|--------|-------------|
| **Selection** | `df['column']` | Select single column |
| | `df[['col1', 'col2']]` | Select multiple columns |
| | `df.loc[row, col]` | Label-based selection |
| | `df.iloc[row, col]` | Integer-based selection |
| **Filtering** | `df[df['col'] > 5]` | Filter rows |
| | `df.query('col > 5')` | Query method |
| **Sorting** | `df.sort_values('col')` | Sort by column |
| | `df.sort_index()` | Sort by index |
| **Grouping** | `df.groupby('col')` | Group by column |
| **Joining** | `pd.merge(df1, df2)` | Merge DataFrames |
| | `pd.concat([df1, df2])` | Concatenate |
| **Missing Data** | `df.dropna()` | Drop missing values |
| | `df.fillna(value)` | Fill missing values |
| **Apply** | `df.apply(func)` | Apply function |
| | `df.applymap(func)` | Apply to each element |

---

## 📚 Learning Path

### Beginner Level (Start Here)
1. ✅ Reading files in pandas
2. ✅ Filtering rows & columns in pandas
3. ✅ Indexing In Pandas

### Intermediate Level
4. ✅ Data Cleaning In Pandas
5. ✅ Merging DataFrames in Pandas
6. ✅ Group By & Aggregations In Pandas

### Advanced Level
7. ✅ EDA in Pandas
8. ✅ Visualization In Pandas

**Recommended Study Plan:**
- Spend 2-3 days on each module
- Complete all exercises in each notebook
- Practice with your own datasets
- Build a mini-project combining multiple concepts

---

## 🛠️ Prerequisites

### Required Knowledge
- Basic Python programming (variables, loops, functions)
- Understanding of data structures (lists, dictionaries)
- Basic command line usage

### Helpful (but not required)
- SQL basics (for understanding joins)
- Basic statistics
- Excel experience

### System Requirements
- **OS**: Windows, macOS, or Linux
- **RAM**: Minimum 4GB (8GB+ recommended)
- **Python**: 3.7 or higher
- **Disk Space**: 500MB+ for libraries and datasets

---

## 🎯 Practical Applications

### Data Science & Analytics
- Data preprocessing and cleaning
- Statistical analysis
- Feature engineering
- Data visualization
- Reporting and dashboards

### Business Intelligence
- Sales analysis
- Customer segmentation
- Financial reporting
- Performance metrics
- Trend analysis

### Machine Learning
- Data preparation
- Feature extraction
- Train/test splitting
- Data transformation
- Model evaluation

---

## 💡 Best Practices

### Performance Tips
```python
# Use vectorized operations instead of loops
# Bad
for i in range(len(df)):
    df.loc[i, 'new_col'] = df.loc[i, 'col1'] + df.loc[i, 'col2']

# Good
df['new_col'] = df['col1'] + df['col2']

# Use appropriate data types
df['category'] = df['category'].astype('category')

# Use chunks for large files
for chunk in pd.read_csv('large_file.csv', chunksize=10000):
    process(chunk)
```

### Memory Optimization
```python
# Check memory usage
df.memory_usage(deep=True)

# Optimize dtypes
df['int_col'] = pd.to_numeric(df['int_col'], downcast='integer')
df['float_col'] = pd.to_numeric(df['float_col'], downcast='float')

# Use categorical for repeated strings
df['category'] = df['category'].astype('category')
```

---

## 🐛 Common Issues & Solutions

### Issue 1: Memory Error
**Problem:** `MemoryError` when loading large files

**Solution:**
```python
# Read in chunks
chunks = []
for chunk in pd.read_csv('large_file.csv', chunksize=10000):
    chunks.append(chunk)
df = pd.concat(chunks)

# Or specify columns and dtypes
df = pd.read_csv('file.csv', usecols=['col1', 'col2'], dtype={'col1': 'int32'})
```

### Issue 2: SettingWithCopyWarning
**Problem:** `SettingWithCopyWarning` when modifying DataFrame

**Solution:**
```python
# Use .loc for setting values
df.loc[df['Age'] > 25, 'Category'] = 'Senior'

# Or use .copy() when creating subset
df_subset = df[df['Age'] > 25].copy()
```

### Issue 3: Slow Performance
**Problem:** Operations taking too long

**Solution:**
```python
# Use vectorized operations
# Use categorical data types for string columns
# Use appropriate indexing
# Avoid iterating with .iterrows() when possible
```

---

## 🔮 Future Enhancements

- [ ] Add practice exercises for each module
- [ ] Include real-world datasets
- [ ] Create video tutorials
- [ ] Add quiz questions
- [ ] Build comprehensive projects
- [ ] Add time series analysis module
- [ ] Include advanced visualization techniques
- [ ] Create Pandas performance optimization guide

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/NewTopic
   ```
3. **Add your notebook**
   - Follow existing structure
   - Include clear explanations
   - Add practical examples
4. **Commit your changes**
   ```bash
   git commit -m 'Add new topic: Topic Name'
   ```
5. **Push and create Pull Request**

### Contribution Ideas
- Add new topics (e.g., Time Series, Advanced Merging)
- Include practice datasets
- Create challenge problems
- Improve existing notebooks
- Fix errors or typos
- Add more examples

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 📧 Contact & Connect

### Author

**Gururaj Krishna Sharma**

- 📧 Email: [guruuu2468@gmail.com](mailto:guruuu2468@gmail.com)
- 💼 LinkedIn: [Gururaj Krishna Sharma](https://www.linkedin.com/in/gururaj-krishna-sharma)
- 💻 GitHub: [@CODERGURU26](https://github.com/CODERGURU26)

---

## 🌟 Acknowledgments

- **Pandas Development Team** for creating this amazing library
- **NumPy Community** for the foundation
- **Jupyter Project** for the notebook environment
- **Python Community** for extensive documentation and support

---

## 📚 Additional Resources

### Official Documentation
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [10 Minutes to Pandas](https://pandas.pydata.org/docs/user_guide/10min.html)
- [Pandas Cookbook](https://pandas.pydata.org/docs/user_guide/cookbook.html)

### Recommended Books
- "Python for Data Analysis" by Wes McKinney (Pandas creator)
- "Pandas in Action" by Boris Paskhaver
- "Effective Pandas" by Matt Harrison

### Online Courses
- DataCamp: Data Manipulation with Pandas
- Coursera: Applied Data Science with Python
- Kaggle: Pandas Micro-Course

### Practice Platforms
- [Kaggle Datasets](https://www.kaggle.com/datasets)
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php)
- [Data.gov](https://data.gov/)

---

## 📊 Project Statistics

- **17 Commits** - Actively maintained
- **8 Modules** - Comprehensive coverage
- **100+ Examples** - Practical demonstrations
- **Beginner Friendly** - Start from basics

---

**⭐ If you find this repository helpful, please give it a star!**

**🔔 Watch this repository to get notified about new topics and updates!**

---

*Last Updated: February 2026*

**Happy Learning! 🐼📊**
