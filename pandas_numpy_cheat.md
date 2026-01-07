# NumPy and Pandas Cheat Sheet

## NumPy Cheat Sheet

### Creating Arrays
```python
import numpy as np

# Array from a list
arr = np.array([1, 2, 3])

# Array of zeros, ones, or a range
zeros = np.zeros((2, 3))  # 2x3 matrix of zeros
ones = np.ones((2, 3))  # 2x3 matrix of ones
range_arr = np.arange(10)  # [0, 1, 2, ..., 9]
linspace_arr = np.linspace(0, 1, 5)  # [0. , 0.25, 0.5, 0.75, 1. ]

# Random arrays
rand_arr = np.random.rand(3, 2)  # Random values between 0 and 1
rand_int = np.random.randint(0, 10, (3, 3))  # Random integers from 0 to 9
```
## Array Operation
```python
arr1 + arr2  # Element-wise addition
arr1 - arr2  # Element-wise subtraction
arr1 * arr2  # Element-wise multiplication
arr1 / arr2  # Element-wise division

np.dot(arr1, arr2)  # Matrix multiplication

arr2 ** 2  # Element-wise squaring
```
## Statistics
```python
np.mean(arr)
np.median(arr)
np.std(arr)
np.var(arr)
np.sum(arr)
np.min(arr)
np.max(arr)
np.argmin(arr)  # Index of minimum value
np.argmax(arr)  # Index of maximum value
```
## Array Indexing and Slicing
```python
arr[0]  # Access first element
arr[1:4]  # Slice from index 1 to 3 (not 4)
arr[:2]  # Slice first 2 elements
arr[-1]  # Last element
arr2d[1, 2]  # Access element in 2D array

# Boolean indexing
arr[arr > 5]  # Elements greater than 5
```
## Reshaping and Transposing
```python
arr.reshape(2, 3)  # Reshape to 2x3
arr.T  # Transpose
arr.flatten()  # Flatten to 1D
```
## Broadcasting
```python
arr + 5  # Adding a scalar to all elements of the array
arr * np.array([1, 2, 3])  # Broadcasting array shapes
```
# Pandas Cheat Sheet
## Creating DataFrames and Series
```python
import pandas as pd

# From a dictionary
data = {'col1': [1, 2, 3], 'col2': [4, 5, 6]}
df = pd.DataFrame(data)

# From a list of lists (or tuples)
data2 = [[1, 2, 3], [4, 5, 6]]
df2 = pd.DataFrame(data2, columns=['A', 'B', 'C'])

# Series from a list
s = pd.Series([1, 2, 3, 4])

# From a CSV file
df_csv = pd.read_csv('file.csv')
```
## Inspecting Data 
```python
df.head()  # First 5 rows
df.tail()  # Last 5 rows
df.shape  # Dimensions of DataFrame (rows, columns)
df.info()  # Information about DataFrame
df.describe()  # Summary statistics
```
## Data selection And Manupulation
```python
# Selecting columns
df['col1']
df[['col1', 'col2']]

# Selecting rows by index position (iloc) or label (loc)
df.iloc[0]  # First row
df.loc[0]  # Row with index label 0

# Slicing rows and columns
df[1:3]  # Rows 1 to 2
df.loc[1:3, ['col1']]  # Rows 1 to 3, 'col1'

# Boolean indexing
df[df['col1'] > 2]  # Rows where col1 > 2
 ## Handling Missing Value
df.isna()  # Check for NaN values
df.dropna()  # Drop rows with NaN values
df.fillna(0)  # Replace NaN with 0

# Forward fill or backfill
df.fillna(method='ffill')  # Forward fill
df.fillna(method='bfill')  # Backward fill
## Operations on DataFrames
df['col1'] + df['col2']  # Column-wise addition
df['col3'] = df['col1'] * df['col2']  # Add new column

# Grouping
df.groupby('col1').sum()  # Sum after grouping by 'col1'

# Sorting
df.sort_values('col1', ascending=False)  # Sort by 'col1'
df.sort_index()  # Sort by index

# Apply a function to a column
df['col1'].apply(lambda x: x + 1)
```
## Merging And Joining
```python
# Merging DataFrames
df1.merge(df2, on='key', how='inner')  # Merge by column 'key'
df1.merge(df2, how='outer')  # Outer join

# Concatenating DataFrames
pd.concat([df1, df2], axis=0)  # Stack rows
pd.concat([df1, df2], axis=1)  # Stack columns
```
## Pivoting and Reshaping
```python
# Pivot table
df.pivot(index='col1', columns='col2', values='col3')

# Melt DataFrame (reverse of pivot)
pd.melt(df, id_vars=['col1'], value_vars=['col2', 'col3'])
```
## Date and Time Operations
```python
df['date'] = pd.to_datetime(df['date'])  # Convert to datetime
df['year'] = df['date'].dt.year  # Extract year from date
df['month'] = df['date'].dt.month  # Extract month

# Date range
pd.date_range('2021-01-01', periods=5, freq='D')
```
## Exporting Data
```python
df.to_csv('output.csv', index=False)  # Write DataFrame to CSV
df.to_excel('output.xlsx', index=False)  # Write DataFrame to Excel
```
df.to_csv('output.csv', index=False)  # Write DataFrame to CSV
df.to_excel('output.xlsx', index=False)  # Write DataFrame to Excel
