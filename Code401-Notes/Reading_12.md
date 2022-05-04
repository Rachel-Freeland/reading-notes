# Day 12 of Python

## Reading

- [Pandas in 10](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)



## Additional Resoureces

- [Pandas - Getting Started](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html)
- [Real Python - Pandas Tutorials](https://realpython.com/learning-paths/pandas-data-science/)

Pandas is a powerful tool for working with tabular data. It is often used for data science but,
the use seems to be unlimited especially when combined with other libraries such as, NumPy

## Videos

- [What is Pandas](https://www.youtube.com/watch?v=dcqPhpY7tWk&t=391s)

With Pandas, data can be manipulated performing such actions as: load, prepare, manipulate, shape, etc. It is like Excel but, free.
Working with Pandas revolves are the data frame. Data visualization can happen very quickly when working with Pandas.

### Bookmark & Review

- [Master Pandas](https://towardsdatascience.com/be-a-more-efficient-data-scientist-today-master-pandas-with-this-guide-ea362d27386)

#### Cheatsheet

- Reading/Writing Data:
  - `pd.read_csv` - also `read_excel`, `read_sql`, etc.
  - `pd.to_csv` - also see examples above

- Checking the data;
  - `data.shape`
  - `data.describe()`

- Seeing the data:
  - `data.head(n)` - print n number of rows from the head
  - `data.loc[n]` or `data.loc[n, 'column_1']` print the nth row or print the data at nth row column_1, respectively
  - `data.loc[range(x,y)]` print the subset of rows x through y
