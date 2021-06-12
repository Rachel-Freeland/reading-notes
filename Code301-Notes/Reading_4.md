# References for today's reading

- [React - Forms](https://reactjs.org/docs/forms.html)
- [The Conditional (Ternary) Operator Explained](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)
- [React - Forms](https://react-bootstrap.github.io/components/forms/)
- [React Docs - Conditional Rendering](https://reactjs.org/docs/conditional-rendering.html)

## Questions regarding React Docs - Forms

1. What is a ‘Controlled Component’?
    - It is a component that takes its current value through props and changes through callbacks. A parent component "controls" it bby handling the callback and managing its own state and passing the new values as props to the controlled component. <https://stackoverflow.com/q/42522515>
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
    - It depends on what you are trying to achieve but, keep in mind that each update to state on each keypress can slow down a browser.
3. How do we target what the user is entering if we have an event handler on an input field?
    - You target the value with `{this.state.value}` and with the `onChange` attribute that calls a function written for that event.

## Questions regarding The Conditional (Ternary) Operator Exaplained

1. Why would we use a ternary operator?
    - The question should be, "why wouldn't you use a ternary operator?" wherever you have an if/else statement that evaluates to a truthy vs falsey.
2. Rewrite the following statement using a ternary statement:

 ```js
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
  ```

  ```js
  if (x === y)? console.log(true) : console.log(false);
  ```

## Things I want to know more about
