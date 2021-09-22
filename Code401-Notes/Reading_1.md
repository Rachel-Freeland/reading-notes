# Notes for Code 401: Day 1

## [Java Basics](<https://docs.oracle.com/javase/tutorial/java/nutsandbolts/index.html>)

### Variables

- Naming Conventions:
  - Names are case-sensitive
  - Should begin with a letter and may use a mix of numbers letters, dollar signs and underscore characters while containing no white spaces
  - If the name consists of one word... use all lowercase letters however, use camel case. Exceptions include"
    - If the variable stores a constant value, the variable should be all uppercase and each word separated by an underscore
- Due to the statically-typed nature of Java, all variables must first be declared using the data type and name.
- Primitive Data Types (there are 8):
  - byte
  - short
  - int
  - long
  - float
  - double
  - boolean
  - char
- Arrays
  - Declaring a variable to refer to an array
    - `type[] variableName;`
    - For example: `int[] anArray`
  - Creating an array
    - `variableName = new type[number of elements]`
    - For example: `anArray = new int[]10`
  - Each element of an array is accessed using its index and bracket notation
  - There is an ***arraycopy*** method that allows you to copy data to another array

### Operators

- Java uses the usual assignment (`=`), math operators (`+, -, *, /, %`), unary operators (`+, -, ++, --, !`), and the conditional operators (`&&, ||, ?:(ternary)`)

### Expressions, Statements, & Blocks

- This is the same as in other languages

#### Control Flow statements

- if/then and if/then/else Statements
- switch Statement
- while and do-while Statements
- for Statement
- Branching statements
  - ***break*** Statement
  - ***continue*** Statement
  - ***return*** Statement

## [Reddit Thread on Compiling](<https://www.reddit.com/r/explainlikeimfive/comments/233dq5/eli5_what_does_it_mean_to_compile_code/>)

Compiling a program is where the computer takes human language and coverts it into machine language which thus, makes the code executable.

## For Reference

[Reading Java Documentation](<https://www.dummies.com/programming/java/making-sense-of-javas-api-documentation/>)