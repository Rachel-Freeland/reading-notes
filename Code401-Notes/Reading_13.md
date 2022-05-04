# Day 13

## Reading

- [How to run Linear Regression in Python](https://bigdata-madesimple.com/how-to-run-linear-regression-in-python-scikit-learn/)

## Additional Resources

- [Linear Regression in Python](https://realpython.com/linear-regression-in-python/)

- Regression analysis is considered to be one of the most important fields in statistics and machine learning. It is used to search for relationships between the different variables. Regression helps us to understand how the different variables are related to each other such as, in the case of gender impact on salaries.

- Linear Regression is the simplest of the regression methods due to its ease of interpreting results.

- The Python package for Linear Regression is NumPy.

- There are 5 basic steps for implementing Linear Regression
    1. Import the classes and packages needed

        ```py
        import numpy as np
        from sklearn.linear_model import LinearRegression
        ```

    2. Establish the data that you want to work with
    3. Create a regression model and fill it with the data

        ```py
        model = LinearRegression()
        ```

    4. Check the results. Do they look correct?

        ```py
        results = model.score()
        ```

    5. Apply the model for predicting the outcomes

## Videos

- [Intro to Simple Linear Regressions](https://www.youtube.com/watch?v=KsVBBJRb9TE)

### Bookmark & Review

- [Train & Test Splits](https://towardsdatascience.com/train-test-split-and-cross-validation-in-python-80b61beca4b6)

- [What is Linear Regression?](https://www.statisticssolutions.com/free-resources/directory-of-statistical-analyses/what-is-linear-regression/)
