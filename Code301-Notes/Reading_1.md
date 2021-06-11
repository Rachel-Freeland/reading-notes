# References to today's reading assignment

- [Component Based Architecture](<https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm>)
- [What is 'props' and How to use it in React](<https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0#:~:text=%E2%80%9CProps%E2%80%9D%20is%20a%20special%20keyword,way%20from%20parent%20to%20child>)
- [React Tutorial through 'passind data through props'](<https://reactjs.org/tutorial/tutorial.html>)
- [React Docs - hello world](<https://reactjs.org/docs/hello-world.html>)
- [React Docs - Introducing JSX](<https://reactjs.org/docs/introducing-jsx.html>)
- [React Docs - Rendering Elements](<https://reactjs.org/docs/rendering-elements.html>)
- [React Docs - Components and props](<https://reactjs.org/docs/components-and-props.html>)

## Questions to answer for reading on _Component Based Architecture_

1. What is a component?
    - A component is a software object that is modular, portable, replaceable and reusable that encapsulates its implementation and exports it as a higher-level interface.
2. What are the charactistics of a component?
    - Reusability - most are designed to be reused whilde there may be some designed for a specific task
    - Replaceable - may be freely substituted with other similar components
    - Extensible - can be extended from an existing component in order to provide a new behavior
    - Encapsulated - allows the user to use its functionality but, does not expose details of the internal processes or any internal variables or state
    - Independent - designed to have minimal dependencies on other components
3. What are the advantages of using component based architecture?
    - Ease of development
    - Ease of deployment
    - Reduced cost
    - Reusable
    - Modification of technical complexity
    - System maintenance and evolution
    - Independent

## Questions in regards to _What is Props and How to Use it in React_

1. What is props short for?
    - Props is short for the word ***properties***
2. How are props used in React?
    - They are used to pass data from one component to another in a uni-directional flow.
    - First, define an attribute and its value
        - Just like in HTML we can assign attributes and values to HTML tags, we can do the same in React. We define our own attributes and assign them values with the `{}`

        ```js
        <childComponent someAttribute={value} anotherAttribute={value} />
        ```

    - Next, we pass data using props
        - Passing props is like passing variables to a function

        ```js
        const ChileComponent = (props) => {
          return <p>I'm the 1st chile!</p>;
        };
        ```

    - Last but, certainly not least, we render the props data

        ```js
        const ChildComponent = (props) => {
          return <p>{props.text}</p>;
        };
        ```

3. What is the flow of props?
    - The flow is one-way or uni-directional from parent to child.

## Things I want to know more about

