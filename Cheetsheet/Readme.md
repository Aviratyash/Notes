# Pandas DataFrame Cheat Sheet

## Introduction to Pandas DataFrame

Pandas DataFrame is a 2-dimensional labeled data structure with columns of potentially different types. It is a powerful tool for data analysis in Python.

## Table of Contents

1. **Creating DataFrames**
   - From a dictionary:
     ```python
     import pandas as pd
     
     data = {'Name': ['Alice', 'Bob', 'Charlie'],
             'Age': [25, 30, 35],
             'City': ['New York', 'Los Angeles', 'Chicago']}
     
     df = pd.DataFrame(data)
     ```
   - From a list of lists:
     ```python
     data = [['Alice', 25, 'New York'],
             ['Bob', 30, 'Los Angeles'],
             ['Charlie', 35, 'Chicago']]
     
     df = pd.DataFrame(data, columns=['Name', 'Age', 'City'])
     ```

2. **Viewing Data**
   - Display first few rows:
     ```python
     df.head()
     ```
   - Display last few rows:
     ```python
     df.tail()
     ```
   - Display summary information:
     ```python
     df.info()
     ```

3. **Selecting and Filtering Data**
   - Selecting a single column:
     ```python
     df['Name']
     ```
   - Selecting multiple columns:
     ```python
     df[['Name', 'Age']]
     ```
   - Filtering rows based on condition:
     ```python
     df[df['Age'] > 25]
     ```

4. **Adding and Removing Columns**
   - Adding a new column:
     ```python
     df['IsStudent'] = [False, True, False]
     ```
   - Removing a column:
     ```python
     df.drop('City', axis=1, inplace=True)
     ```

5. **Handling Missing Data**
   - Dropping rows with missing values:
     ```python
     df.dropna()
     ```
   - Filling missing values with a specific value:
     ```python
     df.fillna(0)
     ```

6. **Aggregation and Grouping**
   - Grouping by a column and applying an aggregation function:
     ```python
     df.groupby('City')['Age'].mean()
     ```

7. **Sorting and Indexing**
   - Sorting by values in a column:
     ```python
     df.sort_values(by='Age', ascending=False)
     ```
   - Resetting index:
     ```python
     df.reset_index(drop=True, inplace=True)
     ```

8. **Saving and Loading Data**
   - Saving DataFrame to CSV:
     ```python
     df.to_csv('data.csv', index=False)
     ```
   - Loading data from CSV:
     ```python
     df = pd.read_csv('data.csv')
     ```

## Resources

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Pandas Cheat Sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)

## Conclusion

Pandas DataFrame simplifies data manipulation tasks in Python, making it easier to analyze and work with tabular data efficiently.
