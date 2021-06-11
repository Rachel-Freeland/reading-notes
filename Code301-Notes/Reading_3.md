# Reading Topics / Resources

- [React Docs - Lists & Keys](<https://reactjs.org/docs/lists-and-keys.html>)
- [The Spread Operator](<https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab>)
- [How to Pass Functions Between Components](<https://www.youtube.com/watch?v=c05OL7XbwXU>)
- [React - Lifting State Up](<https://reactjs.org/docs/lifting-state-up.html>)

## Questions regarding Lists & Keys

1. What does .map() return?
    - It returns an array
2. If I want to loop through an array and display each value in JSX, how do I do that in React?

    ```js
    function NumberList(props) {
      const numbers = props.numbers;
      return (
        <ul>
          {numbers.map((number) =>        
            <ListItem key={number.toString()}                 
            value={number} />      
            )}   
        </ul>
      );
    }
    ```

3. Each list item needs a unique ____.
    - Key / id
4. What is the purpose of a key?
    - Keys help React to identify which items have changed, are added, or are removed.

## Questions regarding the Spread Operator

1. What is the spread operator?
    - It is an ellipsis of 3 dots used to expand an iterable object into a list of arguments
2. List 4 things that the spread operator can do.
    - Copy an array
    - Concatenate arrays
    - Math functions
    - Add an item to a list or to a state in React
3. Give an example of using the spread operator to combine two arrays.

    ```js
    [...["abcdef"]] //Array ["abcedf"]
    [..."abcdef!"] // Array(7) ["a", "b", "c", "d", "e", "f", "!"]
    const hello = {hello: "abcdef"}
    const world = {world:"abcdef!"}

    const helloWorld = {...hello,...world}
    console.log(helloWorld) //Object {hello: "abcdef", world: "a b c d e f !"}

    'abcedf, a b c d e f !`
    ```

4. Give an example of using the spread operator to add a new item to an array.

    ```js
    const fewFruit = ['🍏','🍊','🍌']
    const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
    console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]
    ```


5. Give an example of using the spread operator to combine two objects into one.

    ```js
    const objectOne = {hello: "🤪"}
    const objectTwo = {world: "🐻"}
    const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
    console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
    const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
    objectFour.laugh() // 😂😂😂😂😂
    ```

## Questions regarding How to Pass Functions Between Components

1. In the video, what is the first step that the developer does to pass functions between components?
    - The first thing he does is he adds the function / method to the list of items that are being passed in the parent like adding an attribute to an HTML item.
2. In your own words, what does the increment function do?
   - It updates the "state" of the count for the person in the Person array
3. How can you pass a method from a parent component into a child component?
    - In the parent item you add the `{this.xxxxx}` to list of returned items that will be passed from the parent to the child. Then, on the child you include `{this.props.xxxxx(this.props.name)}` with 'xxxxx' being whatever the name of the property is
4. How does the child component invoke a method that was passed to it from a parent component?
    - It uses the `this.props.method()` and add the `this.props.item` to the call like this `this.props.method(this.props.item)`

## Things I want to know more about

- The negative impacts of using an index as a key
- Rest parameters
