# Reading for Day 9

-[Functional Programming Concepts](<https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa>)

1. What is functional programming?

- It is a programming paradigm - it is a style of building the structure and elements of computer programs - that treats computation as the evaluation of mathematical functions and avoids changing state and mutable data.

2. What is a pure function and how do we know if something is a pure function?

- A pure function is one that returns the same result if given the same arguments. When a function relies only on the parameters passed to the function and it does not cause any observable side effects.

3. What are the benefits of a pure function?

- It makes the code easier to test

4. What is immutability?

- Something that is unable to be changed

5. What is Referential transparency?

- When a function consistently yields the same result for the same input

  `pure functions + immutable data = referential transparency

## Video to watch

- [Node JS Tutorial for Beginners #6 - Modules and require()](<https://www.youtube.com/watch?v=xHLd36QoS4k>)

1. What is a module?

- It is a bit of code that focuses on a specific functionality that when brought together with other modules, makes a program... it is another javaScript file.

2. What does the word 'require' do?

- It is a builtin function to include modules from other files

3. How do we bring another module into the file that we are working in?

- We use the `require()` and place that in a variable

4. What do we have to do to make a module available?

- We have to use `module.export`
