# Error Handling & Debugging

## References

<cite>JavaScript & JQUERY by Jon Duckett<cite>

## Understanding Execution & Scope p. 452 - 457

- Understanding how scripts are processed helps you to figure out the source of an error
- _Execution Contexts_ > There is one global execution context PLUS, each ***function*** creates a new execution context
- Every statement in a script is either: (p. 453)
  - Exection Context:
    - Global context > code that is in a script but, not in a function
    - Function context > code that is run in a function. Each function has its own function context
    - Eval context > text is executed like code in an interanal function called `eval()`
  - Variable Scope:
    - Global scope > if a variable is declared outside a function it can be used anywhere
    - Function-level scope > if a variable is declared inside a function, it can only be used within that function
- 2 phases of activity when script enters a new execution context (p.456)
  1. Prepare
      - The new scope is created
      - Variable, functions, and arguments are created
  2. Execute
      - Assigns values to variables
      - References functions and runs their code
      - Executes  statements
- Understanding ***Scope*** (p. 457)
  - Functions have what is called, ***lexical scope***
  - Functions are linked to the object they were defined <b>within</b>
- Understanding Errors p. 458
  - When JS generates and error, it throws an _exception_ and then, stops the interpreter and looks for _exception-handling code_
- Error Objects (p. 459 - 461)
  - Can help you find where your problem exits
  - Will contain the following properties:
    - `name`: type of error
    - `message`: description of that error
    - `fileNumber`: name of the js file name
    - `lineNumber`: line number of where the error lies
  - 7 types of error objects:
    - `Error`: generic error
    - `SyntaxError`: not following proper syntax... kind of like bad grammar
    - `ReferenceError`: attempting to reference a variable that is not declared or within the scope
    - `TypeError`: unexpected data type that cannot be coerced
    - `RangeError`: numbers not within acceptable range
    - `URIError`: encodeURI(), decodeURI(), and other similar methods used incorrectly
    - `EvalError`: eval() used incorrectly
- Console Tools - I have already used most of these so I will bookmark those pages p. 464 - 483
- Tips and Common Errors noted on p. 484 - 485