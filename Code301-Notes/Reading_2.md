# Reading Topics/Resources

- [React: Lifecycle](<https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093>)
- [React Bootstrap](<https://react-bootstrap.github.io/>)
- [React State vs Props](<https://www.youtube.com/watch?v=IYvD9oBCuJI>)
- [State and Lifecycle](<https://reactjs.org/docs/state-and-lifecycle.html>)
- [React Docs: Handling Events](<https://reactjs.org/docs/handling-events.html>)
- [React Tutorial throught Developer Tools](<https://reactjs.org/tutorial/tutorial.html>)

## Questions to be answered about React Lifecycle

1. Based off the diagram, what happens first, the 'render' or the 'componentDidMount'?

    - First would be the render and then, the componentDidMount

2. What is the very first thing to happen in the lifecycle of React?

    - The `constructor()` is called

3. Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`

    1. constructor
    2. render
    3. componentDidMount
    4. React updates
    5. componentWillUnmount

4. What does componentDidMount do?

    - It loads anything that needs to use a network request and/or it initializes the DOM

## Questions about React State vs Props

1. What types of things can you pass in the props?

    - Anything that you would pass to a function

2. What is the big difference between props and states?

    - **Props** are things that you ***pass into*** a component from ***outside*** the component while **states** are things that you are handling ***inside*** that component. Props are updated outside the component while states are updated inside the component.

3. When do we re-render our application?

    - When the state changes

4. What are some examples of things that we could store in state?

    - Examples of things that we could store in state would be:
      - User repsonses to prompts
      - Counters that need to be updated
      - Anything that will change

## Things I want to know more about
