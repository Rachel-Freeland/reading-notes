# Reading for Day 5:

- [React Docs - thinking in React](<https://reactjs.org/docs/thinking-in-react.html>)

1. How would you break a mock into a component heirarchy?
    - The 1st thing you want to do is to draw boxes around every componenet and subcomponent in the mock and give them names.
      Also, you can use the same techniques you would use to decide if you should create a function or an object.
2. What is the `single responsibility principle` and how does it apply to components?
    - A component should do 1 thing and if you see it growing into more, then break it into smaller subcomponents.
3. What does it mean to build a `static` verion of your application?
    - It means to build a version of the app that takes your data model and renders the UI but, has no interactivity.
4. Once you have a static application, what do you need to add?
    - The next step is to add / identify the minimal set of state.
5. What are the three questions you can ask to determine if something is state?
    1. Is it passed in from a parent via props? If so, it probably isn't state.
    2. Does it remain unchanged over time? If so, it probably isn't state.
    3. Can you compute it based on other state or props in your component? If so, it isn't state.
6. How can you identify where state needs to live?
    1. Identify every componenet that renders something based on that state
    2. Find a common owner component (a single component above all the componenets that need the state in the heirarchy)
    3. Either the common owner or another component higher up should own the state
    4. If you can't find a component where it makes sense to own the state, create a new component solely for holding
      the state and add it somewhere in the heirarchy above the common owner.
