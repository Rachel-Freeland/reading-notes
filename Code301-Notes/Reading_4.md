# Reading for Day 4:

- [React Docs - Forms](<https://reactjs.org/docs/forms.html>)

1. What is a 'Controlled Component'?
    - A 'controlled component' is a component that renders form elements and controls them by keeping the form data in athe component's state. It takes its current value through props and notifies changes through callbacks like `onChange`. A parent component "controls" it by handling the callback and managing its own state and passing the new values as props to the controlled component. <https://stackoverflow.com/questions/42522515/what-are-react-controlled-components-and-uncontrolled-components>
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why?
    - I feel that this is a user preference and you may want to save it to state when they submit or update as they type depending on what you want to achieve. However, with that said, the user can receive instant feedback without having to wait until they submit the form if you update state as they type.

3. How do we target what the user is entering if we have an event handler on an input field?
    - We bind the `this` to the function that will be called

    ```js
    this.handleChange = this.handleChange.bind(this);

    handleChange(event) {
      this.setState({ value: event.target.value });
    }
    ```

- [The Conditional (Ternary) Operator Explained](<https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff>)

1. Why would we use a ternary operator?
    - A ternary operator can be used wherever a conditional `if` statement occurs.

2. Rewrite the following statement using a ternary statement:

```js
if(x === y) {
  console.log(true);
} else {
  console.log(false);
}
```

```js
if (x === y)? true : false;
```

## Bookmark / Skim

- [React Bootstrap - Forms](<https://react-bootstrap.github.io/components/forms/>)
- [React Docs - Conditional Rendering](<https://reactjs.org/docs/conditional-rendering.html>)
