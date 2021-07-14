# Reading for day 3:

- [React Docs - Lists and Keys](<https://reactjs.org/docs/lists-and-keys.html>)

1. What does .map() return?
    - It iterates over the array and return a new array.

2. If I want to loop through an array and display each value in JSX, how do I do that in React?
    - You use the curly braces `{}`

3. Each list item needs a unique ____.
    - Key

4. What is the purpose of a key?
    - To help React to identify which iterms have changed, been added, or those that are to be removed.

- [The Spread Operator](<https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab>)

1. What is the spread operator?
    - It is a set of ellipsis `(...)` to expand an iterable object into a list of arguments. In other words, it spreads the array or objedt into seperate arguments.

2. List 4 things that the spread operator can do.
    1. Copy an array
    2. Concatenate / Combine arrays
    3. Converting a NodeList to an array
    4. Add state to React

3. Give an example of using the spread operator to combine 2 arrays.

```js
onst myArray = [`🤪`,`🐻`,`🎌`]
const yourArray = [`🙂`,`🤗`,`🤩`]
const ourArray = [...myArray,...yourArray]
console.log(...ourArray) 

// 🤪 🐻 🎌 🙂 🤗 🤩
```

4. Give an example of using the spread operator to add a new item to an array.

```js
const fewFruit = ['🍏','🍊','🍌']
const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
console.log(fewMoreFruit) 

//  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]
```

5. Give an example of using the spread operator to combine 2 objects into 1.

```js
const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}

console.log(objectThree) 

// Object { hello: "🤪", world: "🐻", laugh: "😂" }


const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}

objectFour.laugh() 

// 😂😂😂😂😂
```

## Videos

- [How to Pass Functions Between Components](<https://www.youtube.com/watch?v=c05OL7XbwXU>)

1. In the video, what is the first step that the developer does to pass functions between components?
    - Create a function wherever the state is that you want to change.

2. In your own words, what does the `increment` function do?
    - It loops through an array of people and finds the object it wants to change or modify. It then updates the item/array using `this.setState`

3. How can you pass a method from a parent component into a child component?
    - You pass it like you do the properties using the curly braces 
    
    ```js
    increment={this.increment}
    ```

4. How does the child component invoke a method that was passed to it from a parent component?
    - It calls the `this.props.increment()` inside the increment method in the Person component.


### Bookmark / Skim

- [React Tutorial through 'Declaring a Winner'](<https://reactjs.org/tutorial/tutorial.html>)
- [React Docs - Lifting State Up](<https://reactjs.org/docs/lifting-state-up.html>)