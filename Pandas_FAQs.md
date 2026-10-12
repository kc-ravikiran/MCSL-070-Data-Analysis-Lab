**1. What is Pandas in Python?**

Pandas is an open-source Python library used for data manipulation and analysis. 
It provides flexible data structures like Series and DataFrame to handle structured data efficiently.

**2. What are the key data structures in Pandas?**
- Series: One-dimensional labeled array.
- DataFrame: Two-dimensional table-like structure.
- Panel (deprecated): Three-dimensional data structure.

**3.How do you install Pandas?**

Use the following command: `pip install pandas`

**4.How do you import Pandas in a Python script?**

`import pandas as pd`

**5.How do you create a Pandas Series?**

```python
import pandas as pd
data = pd.Series([10, 20, 30, 40])
print(data)
```
**6.How do you create a Pandas DataFrame from a dictionary?**

A Pandas DataFrame can be created from a dictionary using the pd.DataFrame() function. 
The dictionary keys become the column names, and the values, typically lists, become the data in those columns. 

For example:
```
df = pd.DataFrame(data)
```
This converts the dictionary into a tabular DataFrame structure that can be used for data analysis and manipulation.

```python
import pandas as pd

data = {
        'Name': ['Kartik', 'Bob', 'ravi'],
        'Age': [25, 30, 25],
        'Area': ['Shimoga', 'Srilanka', 'Anjananagara']
       }
df = pd.DataFrame(data)
print(df)
```

**7. How do you read a CSV file into a DataFrame?**
```
df = pd.read_csv("data.csv")
```

**8. How do you write a DataFrame to a CSV file?**

We can write a Pandas DataFrame to a CSV file using the to_csv() method. For example:
```
df.to_csv("output.csv", index=False)
```
Example:
```python
import pandas as pd

data = {
    'Name': ['Kartik', 'Bob', 'Ravi'],
    'Age': [25, 30, 25]
}

df = pd.DataFrame(data)

df.to_csv("output.csv", index=False)

print("CSV file created successfully!")
```

**9. How do you display the first 5 rows of a DataFrame?**

`df.head()`

**10. How do you check the shape of a DataFrame?**
```
df.shape
```

**11. What does `df.info()` do?**

Displays metadata about the DataFrame, including data types and non-null values.

**12.What does `df.describe()` return?**

Provides summary statistics of numerical columns.

**13. How do you select a specific column in a DataFrame?**
```
df["column_name"]
```
**14. How do you filter rows based on a condition?**
```
df[df['Age'] > 25]
```
Example:
```python
import pandas as pd

data = {
    'Name': ['Kartik', 'Bob', 'Ravi'],
    'Age': [25, 30, 28],
    'Area': ['Shimoga', 'Srilanka', 'Anjananagara']
}

df = pd.DataFrame(data)

filtered_df = df[df['Age'] > 28]

print(filtered_df)
```
```Output
  Name  Age      Area
1  Bob   30  Srilanka
```

**15. How do you add a new column to a DataFrame?**

A new column can be added to a Pandas DataFrame by assigning values to a new column name.
For example:
```
df['Salary'] = [50000, 60000]
```
```Python
import pandas as pd

data = {
    'Name': ['Kartik', 'Bob', 'Ravi'],
    'Age': [25, 30, 28]
}

df = pd.DataFrame(data)

# Add a new column
df['Salary'] = [50000, 60000, 55000]

print(df)
```

```output
     Name  Age  Salary
0  Kartik   25   50000
1     Bob   30   60000
2    Ravi   28   55000
```

**16. How do you delete a column from a DataFrame?**

In Pandas, you can remove a column using the drop() method.
```
df.drop(columns=['Salary'], inplace=True)
```

```python
import pandas as pd

data = {
    'Name': ['Kartik', 'Bob', 'Ravi'],
    'Age': [25, 30, 28],
    'Salary': [50000, 60000, 55000]
}

df = pd.DataFrame(data)

print("Before deleting:")
print(df)

df.drop(columns=['Salary'], inplace=True)

print("\nAfter deleting:")
print(df)
```
```Output
Before deleting:
     Name  Age  Salary
0  Kartik   25   50000
1     Bob   30   60000
2    Ravi   28   55000

After deleting:
     Name  Age
0  Kartik   25
1     Bob   30
2    Ravi   28
```

**17. What is the difference between loc[] and iloc[]?**

loc[] and iloc[] are used for data selection in Pandas. 
loc[] selects rows and columns using labels (index names and column names), 
whereas iloc[] selects rows and columns using integer positions(row and column numbers). 
For example, df.loc['B', 'Name'] accesses data using labels, while df.iloc[1, 0] accesses the same data using row and column positions.

```python
import pandas as pd

data = {
    'Name': ['Kartik', 'Bob', 'Ravi'],
    'Age': [25, 30, 28]
}

df = pd.DataFrame(data, index=['A', 'B', 'C'])

print("Original")

print(df)
print("Example of loc")

print(df.loc['B'])

print("Example of iloc")

print(df.iloc[0])
```

```output
Original
     Name  Age
A  Kartik   25
B     Bob   30
C    Ravi   28
Example of loc
Name    Bob
Age      30
Name: B, dtype: object
Example of iloc
Name    Kartik
Age         25
Name: A, dtype: object
```

**18. How do you reset the index of a DataFrame?**
```python
df.reset_index(drop=True, inplace=True)
```
