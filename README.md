---

# 📌 README.md

````markdown
# 🐍 Python for Data Science Cheat Sheet  
## 📊 Python Pandas  

---

## 📌 What is Pandas?  
Pandas is a Python library that provides **easy-to-use data structures** and **data analysis tools** for the Python programming language.  

---

## 📌 Import Convention
```python
import pandas as pd   # Import pandas
````

---

## 📌 Pandas Data Structures

### ✅ Series

```python
s = pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])
```

### ✅ DataFrame

```python
data_mobile = {
    'Mobile': ['iPhone', 'Samsung', 'Redmi'],
    'Color': ['Red', 'White', 'Black'],
    'Price': ['High', 'Medium', 'Low']
}

df = pd.DataFrame(data_mobile, columns=['Mobile', 'Color', 'Price'])
```

---

## 📌 Importing Data

```python
pd.read_csv(filename)
pd.read_table(filename)
pd.read_excel(filename)
pd.read_sql(query, connection_object)
pd.read_json(json_string)
```

---

## 📌 Exporting Data

```python
df.to_csv(filename)
df.to_excel(filename)
df.to_sql(table_name, connection_object)
df.to_json(filename)
```

---

## 📌 Create Test / Fake Data

```python
import numpy as np

# Create a DataFrame with random floats
pd.DataFrame(np.random.rand(4, 3))

# Create a Series
pd.Series([10, 20, 30, 40])
```

---

## 📌 Operations

### 🔹 View DataFrame Contents

```python
df.head(n)      # First n rows
df.tail(n)      # Last n rows
df.shape        # Rows & columns
df.info()       # Index, Datatype & Memory info
df.describe()   # Summary statistics for numerical columns
```

---

### 🔹 Selection

#### Using `.iloc` (index-based)

```python
df.iloc[0]      # First row
df.iloc[1]      # Second row
df.iloc[-1]     # Last row
df.iloc[:, 0]   # First column
df.iloc[:, 1]   # Second column
```

#### Using `.loc` (label-based)

```python
df.loc[0, "column_name"]                # Select single value
df.loc['row1':'row3', 'column1':'column3']   # Slice by labels
```

---

### 🔹 Sorting

```python
df.sort_index()                                      # Sort by index
df.sort_values(by='column1')                         # Sort ascending
df.sort_values(by='column2', ascending=False)        # Sort descending
```

---

### 🔹 GroupBy

```python
df.groupby("column")                  # Group by one column
df.groupby(["col1", "col2"])          # Group by multiple columns
df.groupby("col1")["col2"].mean()     # Mean of col2 grouped by col1
df.groupby("col1")["col2"].median()   # Median of col2 grouped by col1
```

---

## 📌 Plotting

```python
# Histogram
df.plot.hist()

# Scatter Plot
df.plot.scatter(x="column1", y="column2")
```

---

## 📌 Functions

* **Mean**

```python
df.mean()     # Mean of all columns
```

* **Median**

```python
df.median()   # Median of all columns
```

* **Standard Deviation**

```python
df.std()      # Standard deviation of each column
```

* **Max**

```python
df.max()      # Highest value in each column
```

* **Min**

```python
df.min()      # Lowest value in each column
```

* **Count**

```python
df.count()    # Number of non-null values in each column
```

* **Describe**

```python
df.describe() # Summary statistics for numerical columns
```

---

## 📌 Reference

📘 *Python for Data Science Certification Training Course*

---

```

---

  

Do you also want me to add a **table of contents with clickable links** (for quick navigation inside the README)?
```
