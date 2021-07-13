# Day 2 Reading notes from:

- [React Lifecycle](<https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093>)

1. Based off the diagram, what happens first, the `render` or the `componentDidMount`?

    - It appears that `render` happens BEFORE the `componentDidMount`

2. What is the very first thing to happen in the lifecycle of React?

    - The constructor is called before mounting

3. Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`

    - `constructor`
    - `render`
    - `componentDidMount`
    - `React Updates`
    - `componentWillUnmount`

4. What does `componentDidMount` do?

    - It allows you to make DOM manipulations, network requests, etc. It is a good place to setup subscriptions.

## Additional Resources

- [React Bootstrap Documentation](<https://react-bootstrap.github.io/>)
- [Netlify](<https://www.netlify.com/>)

## Videos

- [React State vs Props](<https://www.youtube.com/watch?v=IYvD9oBCuJI>)

1. What types of things can you pass in the props?

    - Props are like arguments to a function. They are what you pass want to initialize your component to or what you want your component to render like such as a title.

2. What is the big difference between props and state?

    - Props are what you pass to a component and state is what you handle inside of that component. Props are outside of the component and must be updated outside of the component. State is handled in the componenet and you update it inside the component.

3. When do we re-render our application?

    - When the state changes or the app needs to be re-rendered due to something the user has done.

4. What are some examples of things we could store in state?

    - Things that you will update or change such as a counter.

## Bookmark / Skim

- [React Docs - State and Lifecycle](<https://reactjs.org/docs/state-and-lifecycle.html>)
- [React Docs - Handling Events](<https://reactjs.org/docs/handling-events.html>)
- [React Tutorial through 'Developer Tools'](<https://reactjs.org/tutorial/tutorial.html>)
