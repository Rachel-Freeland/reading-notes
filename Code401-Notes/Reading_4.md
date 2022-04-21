# Day 4 Reading Topics

## Read

- [Classes and Objects](<https://www.learnpython.org/en/Classes_and_Objects>)
- [Thinking Recursiveliy in Python](<https://realpython.com/python-thinking-recursively/>)

- [Pytest Fixtures and Coverage](<https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage>)

- Classes are a template to create objects.
- Objects receive their attributes and methods from their classes.
- Accessing various attributes within a, use dot notation. `myobjects.variable`
- Calling a function on the object made from a specific class, use parenthetical notation. `myobjects.function()`
- The dunger init function, is called when the class is initiated. It is used for assigning the values in a clas.

- Recursive functions will continue to call itself and repeat its behavior until some condition is met to return a result.
- Each recursive call adds another layer to the call stack and unwinds as each call returns a result.
- To maintain **state** during recursion:

  1. Thread the state through each recursive call so that the current state is part of the current call's execution context, ***OR;***

    ```py
    def sum_recursive(current_num, accumulated_sum):
      # Base case
      # Return final state
      if current_num == 11
        return accumulated_sum
      
      # Recursive case
      # Thread the state through the recursive call
      else:
        return sum_recursive(current_num + 1, accumulated_sum + current_number)
    ```

  2. Keep the state in global scope

    ```py
    # Global mutable state
    current_num = 1
    accumulated_sum = 0

    def sum_recursive();
      global current_num
      global accumulated_sum

      # Base case
      if current_num == 11
        return accumulated_sum
      
      # Recursive case
      else:
        accumulated_sum += current_num
        current_num += 1
        return sum_recursive()
    ```

- A data structure is considered recursive when it can be defined in terms of a smaller version of itself, for example, a ***list*** is recursive.
  1. Start with an empty list, and apply the attach_head(element, smaller list) reursively
  2. Recursion = self-referential function

- **PyTest Fixtures** are a defined, reliable and consistent context for tests.
- Fixtures define the steps and data that constitue the arrange phase of a test.
- We can mark a function to denote that it is a fixture with `@pytest.fixture`
- If a fixture raises and exception, pytest will stop executing fixtures for that test and mark the test as having an error.
- PyTest Coverage checks that your tests have run all of the code
- To obtain coverage it needs to be installed from PyPI
- To invoke coverage, without and with specifying the program(s) to test: `pytest --cov` or `pytest --cov=mymul .`

### Bookmark & Review

- [Pytest Fixtures](<https://docs.pytest.org/en/latest/explanation/fixtures.html>)
