# Pandas Cheatsheet

## Introduction
Pandas is a powerful Python library for data manipulation and analysis. It provides data structures like DataFrames and Series, which are essential for working with structured data. This cheatsheet provides a quick reference for common operations using Pandas.

## Installation
Install Pandas using pip:
```bash
pip install pandas
Importing Pandas
bash
Copy code
import pandas as pd
Basic Operations
Creating DataFrames
bash
Copy code
# From a dictionary
df = pd.DataFrame({'Column1': [1, 2, 3], 'Column2': ['A', 'B', 'C']})

# From a list of lists
df = pd.DataFrame([[1, 'A'], [2, 'B'], [3, 'C']], columns=['Column1', 'Column2'])
Reading Data
bash
Copy code
# From CSV file
df = pd.read_csv('filename.csv')

# From Excel file
df = pd.read_excel('filename.xlsx', sheet_name='Sheet1')
Viewing Data
bash
Copy code
# Display first few rows
df.head()

# Display last few rows
df.tail()

# Summary statistics
df.describe()
Data Selection
bash
Copy code
# Selecting a column
df['Column1']

# Selecting multiple columns
df[['Column1', 'Column2']]

# Selecting rows by index
df.loc[0]  # Selects row at index 0

# Selecting rows and columns by index
df.loc[0, 'Column1']
Data Manipulation
bash
Copy code
# Adding a new column
df['NewColumn'] = [1, 2, 3]

# Applying a function
df['Column1'].apply(lambda x: x * 2)

# Filtering rows
df[df['Column1'] > 1]

# Sorting
df.sort_values(by='Column1')

# Grouping and aggregating
df.groupby('Column1').mean()
Handling Missing Data
bash
Copy code
# Checking for null values
df.isnull()

# Dropping rows with null values
df.dropna()

# Filling null values
df.fillna(value=0)
Writing Data
bash
Copy code
# To CSV file
df.to_csv('newfile.csv', index=False)

# To Excel file
df.to_excel('newfile.xlsx', sheet_name='Sheet1', index=False)
This cheatsheet covers many of the basic operations and functionalities of Pandas. For more detailed information, refer to the Pandas Documentation.
