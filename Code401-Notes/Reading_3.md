# Day 3

## Reading

- [Read & Write Files in Python](<https://realpython.com/read-write-files-python/>)
- [Exceptions in Python](<https://realpython.com/python-exceptions/>)

  1. What makes up a file and why that's important in Python

  - Files have 3 main parts:
    1. ***Header:*** holds metadata about the contents
    2. ***Data:*** the contents
    3. ***End of File (EOF):*** the special charachter that indicates the end of the file
  - File Paths have 3 major parts:
    1. ***Folder Path:*** the location on the system where each part of the path is separated by a slash
    2. ***File Name:*** the actual name of the file
    3. ***Extension:*** indicates the type of file and possible contents and is pre-pended with a period
  - Using `C:\VSCode\projects\dogs.txt` is a representation of an ***absolute path***
  - Using `../../VSCode/projects/dogs.txt` is a representation of a ***relative path***
    - Think of each `../` as each floor that you must traverse in order to reach your file from the current directory
    - Think of each named segment as a hallway or door that you must walk through in order to reach the proper room/location in order to find the file
  - Line endings can affect how you work with a file so, it is good to have an understanding of the standardization
    - Windows computers use a Carriage Return and Line Feed charachters (CR+LF)

      ```txt
      Pug\r\n
      Boxer\r\n
      ```

    - Unix and mac systems use just the Line Feed LF charachter (LF)

      ```txt
      Pug\r
      \n
      Boxer\r
      \n
      ```

  - Character Encodings, such as ASCII or Unicode, can affect how a file's contents are displayed

  2. The basics of reading and writing files in Python
  - To work with a file, it must first be opened using either:
    - the `open()` built-in function

      ```py
      file = open('../dogs/breeds.txt')
      ```

    - the `with` statement

      ```py
      with open('../dogs/breeds.txt') as reader
      ```

  ***WARNING: Always make sure files get closed properly!***
  - After working with the file it must be properly closed
    1. To properly close a file, use the **try-finally** block

        ```py
        reader = open('dog_breeds.txt')
        try:
          # statements
        finally:
          reader.close()
        ```

    2. Use the `with` statement... it automatically closes the file

        ```py
        with open('dog_breeds.txt', 'r') as reader:
          # statements
        ```

        - Notice the second argument in the above example, this indicates the mode in which to open the file. The basic modes are;
        1. `'r'` for reading and is the default
        2. `'w'` for writing, truncating or overwriting the file first
        3. `'rb'` or `'wb'` this opens for read or write, respectively, in binary mode
  - There are 3 differnt categories for file objects:
    1. Text files ***most common encounter***
    When using `open()`, a ***TextIOWrapper*** file object is returned
    2. Buffered binary files
    When using `open()`, a ***BufferedReader*** or ***BufferedWriter*** object is returned
    3. Raw binary files (a low-level building-block for binary and text streams)
    When using `open()`, a ***FileIO*** is returned
  - Reading methods
    - `.read(size=-1)` Reads from the fiile based on the number of bytes. If no argument is passed or None or -1 is passed, the entire file is read.
    - `.readline(size=-1)` Reads and returns 1 line from the stream. If `size` is specified, that will be the most ***size*** bytes read
    - `.readlines(hint=-1)` Reads and returns a list of lines. ***hint*** can be used to control the number of lines read
      - An example of how to read the entire file as a list
        ```py
        f = open('dog_breeds.txt')
        f.readlines() # Returns a list object

        # or use the list() function like so

        list(f)
        ```

  3. Some basic scenarios of reading and writing files
  - Iterating over each line of a file
  - Appending to a file

## Videos

- [Read & Write Files in Python - Companion Video](<https://realpython.com/courses/reading-and-writing-files-python/>)

## Bookmark and Review

- [Reading and Writing Files in Python Quiz](<https://realpython.com/quizzes/read-write-files-python/>)