# JavaScript

## References

JavaScript & JQuery By Jon Duckett

- pp. 100 - 105 & 183 - 242

### Objects

- Group together a set of variables and functions to create a model of something you would recognize in the real world.
  
  - Variables are a.k.a Properties (attributes and things that can describe the object)
  - Functions are a.k.a Methods (represent tasks and ways to act on that object)
  - Uses a key/value or name/value pairings

Creating an Object: Literal Notation

- Each object is the curly braces and their contents
- Each object is stored as a variable
- Each _key_ is separated from its _value_ using a colon
- Each property and method is separated by a comma (except for the last value)

```js
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  checkAvailability: function() {
    return this.rooms - this.booked;
  }
};
```

Accessing an Object and Dot Notation

- Properties or methods can be accessed using _dot notation_ or _square brackets_

```js
(dot notation)
var hotelName = hotel.name;
var roomsFree = hotel.checkAvailability();

(square bracket notation)
var hotelName = hotel['name'];
var roomsFree = hotel['checkAvailability'];
```

- Square bracket notation is often used when:
  
  - The property or method name contains special characters
  - Property name is a number (while allowed... should be avoided)
  - A variable is being used in place of the property name (see ch. 12)
  
### Document Object Model (DOM)

- The DOM is not part of HTML or JavaScript, it is a separate set of rules
- Purpose serves to tell browsers how to create a model of an HTML page and how to access JavaScript and update the contents of the page
- Also referred to as an API (Application Programming Interface) which lets programs (and scripts) talk to each other
- The DOM tree is created as a browser loads the page and is stored in the browsers' memory. It consists of 4 types of nodes:
  1. The Documnet node
      - When ever you access any element, attribute, or text node, you navigate to it via the document node
      - Every element, attribute, and piece of text is represented by its own DOM node
  2. Element nodes
      - Describe the structure of the page
      - When accessing the DOM tree, start by looking for elements
      - Once you find the element you want then you can access its text and attributes
  3. Attribute nodes
      - These nodes represent the attributes carried on the opening tags of the HTML elements
  4. Text nodes
      - Once you gain access to the element node then, you can reach the text within the element.

Working With the DOM Tree

- Access and updating the tree involves 2 steps:
  1. Locate the node that represents the element you want to work with
      1. Select an individual node - 3 Common ways to select an individual element
          1. getElementById() - uses the value of the _id_ attribute (p.195)
          2. querySelector() - Uses a CSS selector, and returns the 1<sup>st</sup> matching element (p. 202)
          3. You can also select individual elements by traversing the DOM tree
      2. Select multiple nodes (NodeLists) - 3 Common ways to select multiple elements
          1. getElementsByClassName() - selects all elements with the matching class attribute (p. 200)
          2. getElementsByTagName() - selects all elements that have the specified tag name (p. 201)
          3. querySelectorAll() - uses a CSS selector to select all matching elements (p. 202)
      3. Traversing between element nodes
          1. parentNode - selects the parent of the current element node (p. 208)
          2. previousSibling/nextSibling - does what it says, it selectst the previous or next sibling in the DOM tree (p. 210)
          3. firstChild/lastChild - selects the 1<sup>st</sup> or last child of the current element (p. 211)
  2. Use its text content, child elements, and attributes
      1. Access / Update Text Nodes
          - The text nodes only property is the `nodeValue`
          - `nodeValue` lets you access or update the contents of a text node (p. 214)
          - The text node does NOT include any text inside any child elements
      2. Work with HTML Content
          - One property allows acces to child elements and text content, `innerHTML` (p. 220)
          - To access just the text content, `textContent` (p. 216)
          - DOM Manipulation: Several methods allow you to create new nodes, add nodes to a tree and remove nodes from a tree: `createElement`, `createTextNode`, `appendChild()/removeChild()` (p. 222)
      3. Access or Update Attribute Values (p. 232)
          - `className/id` - lets you get or update the value of the _class_ or _id_ attributes
          - hasAttribute() - checks if an attribute exists
          - getAttribute() - gets the value of the attribute
          - setAttribute() - updates the value
          - removeAttribute() - removes an attribute

<b>Methods That Select Individual Elements</b>

- getElementById() - This is the quickest and most efficient way to access an element because no 2 elements should share the same _id_

```js
document.getElementById('one')
```

- ***document*** refers to the document object
- ***getElementById()*** finds an element based upon the value of the _id_ attribute
- ***memeber operator*** '.'  indicates that the method on the right is being applied to the node on the left
- ***parameter*** is 'one' and is the value of the _id_ attribute

- querySelector()

  - newest addition to the DOM
  - very flexible because its parameter is a CSS selector
  - more accurate at targeting many more elements

<b>DOM Queries That Return More Than 1 Element</b>

- ***NodeList*** is a collection of element nodes
  - they look like arrays and are numbered like arrays
  - they are an object called a ***collection***
  - the order that element nodes are stored is the order they appear in the HTML page
- ***Live NodeList*** is when your script updates the page and the NodeList is updated at the SAME time
- ***static NodeList*** is when your script is updates the page but, the NodeList is not updated to reflect the changes

  ***DOM Queries that return a NodeList***

  - `getElementsByTagName('li')` - returns a list containing the index number & element

  ```js
  var elements = document.getElemetsByTagName('li');  // find <li> elements

  if (elements.length > 0) {  // if 1 or more are found
    var el = elements[0];  // selects the 1st one using the array syntax
    el.className = 'cool';  // changes the value of the class attribute to 'cool'
  }
  ```

  - `getElementsByClassName('hot')` - returns a list of the elements with a _class name_ that matches 'hot' and their index numbers

  ```js
  var elements = document.getElemetsByClassName('hot'); // find 'hot' items

  if (elements.length > 2) {  // if 3 or more elements with className 'hot' are found

    var el = elements[2];  // select the 3rd one from the NodeList
    el.className = 'cool';  // change the value of the class attribute
  }
  ```

  - `querySelectorAll('li[id]')` - returns a list of the `<li>` elements that have and _id_ attribute and their index number
    - Note: this method offers more flexibility and accuracy

  ```js
  // querySelector() only returns the 1st match
  var el = document.querySelector('li.hot');
  el.className = 'cool';

  // querySelectorAll() returns a NodeList
  var els = document.querySelectorAll('li.hot');
  els[1].className = 'cool';  // selects the 2nd matching element and changes it
  ```
  
<b>Selecting An Element From A NodeList</b>

- 2 ways to select an element from a NodeList

  - The _item()_ methond
    - When using the _item()_, you specify the index number of the node that you want
    - Before running the _item()_ method, programmers check to make sure that there is at least 1 item in the NodeList before running the code

    ```js
    var elements = document.getElementsByClassName('hot')
    if (elements.length >= 1) {
      var firstItem = elements.item(0);
    }
    ```

    1. Select elements that have a class attribute of 'hot' and store the NodeList in a variable called ***elements***
    2. Use the ***length*** property to check how many elements were found. If you have at least 1... run the code in the ***if*** statement
    3. Store the first element from the NodeList in a variable called ***firstItem***
  - Array syntax
    - Preferred over the _item()_ method because it is faster
    - Make sure you check for the node(s)
    - If you repeatedly use the NodeList, store it in a variable

    ```js
    var element = document.getElementByClassName('hot');
    if (elements.length >= 1) {
      var firstItem = elements[0];
    }
    ```

    1. Create a NodeList containing elements that have a ***class*** attribute whose value is ***hot***, and store it in a variable called ***elements***
    2. Run the code if the number is greater than or equal to 1
    3. Get the first element from the NodeList

<b>Repeating Actions For An Entire NodeList</b>

- Use a loop, in this example, we use a _for_ loop

```js
let hotItems = document.querySelectorAll('li.hot');

for (let i = 0; i < hotItems.length; i++) {
  hotItems[i].className = 'cool';
}
```

  1. Assigns the variable with a NodeList of all items whose class attribute is _hot_
  2. Length of the NodeList refers to the number of elements or, in this case, how many times the loop will run
  3. Using the array syntax, indicates which item in the NodeList is currently being manipulated

<b>Traversing the DOM</b>

- When you have an element node, you can select another element in relation to it using;
  1. ***parentNode*** This finds the element node for the contained element. If, for example, you started with the 1st `<li>` element, then its _parent node_ would be the `<ul>` element
  2. ***previousSibling / nextSibling*** These find the element in question in relation to the current element.
  3. ***firstChild / lastChild*** These find the first or last child of the given element
- ***Whitespace Nodes*** are created from spaces or carriage returns in most browser with the exception of IE. So, be careful using:
  - previousSibling
  - nextSibling
  - firstChild
  - lastChild

- To work with the content of elements, you can:
  - Navigate to the text node - works best when the element contains only text and no other elements
    - Once you have navigated from an element to its text node the property you use is _nodeValue_. This allows you to access text from the node. ***See page 214***
    - In order to use _nodeValue_, you must be on a text node and not the element that contains it

    ```js
    document.getElementById('one').firstChild.nextSibling.nodeValue;
    ```

      1. The `<li>` element node is selected by using the _getElementById()_ method
      2. The 1st child of `<li>` is the `<em>` element
      3. The _nextSibling_ of the `<em>` is the text node
      4. You now have the text node and can access its contents using the _nodeValue_

  - Accessing and Changing a Text Node
  
  ```js
  var itemTwo = document.getElementById('two');  // Get the 2nd list item

  var elText = itemTwo.firstChild.nodeValue;  // Get the text content

  elText = elText.replace('pine nuts', 'kale');  // Change pine nuts to kale

  itemTwo.firstChild.nodeValue = elText;  // Update the list item with the new info
  ```

  - Work with the containing element - allows you to access its text nodes and child elements. Works best when an element has text nodes and child elements that are siblings
    - When working with an elelment node, the element can contain markup.
    - Use `get` to retrieve or `set` to update the markup as well as text
      - `innerHTMl` gets/sets the text & markup ***See page 220***
      - `textContent` get/sets the text only ***See page 216***
      - `innerText` gets/sets the text only ***See page 216***

  - Using `textContent` and `innerText`
    - `textContent` allows you to collect or update the text in the containing element and its children
    - `innerText`: ***this property should be avoided***

  - ***Adding / Removing*** HTML Content: 2 Approaches - `innerHTML` and DOM manipulation
    - `innerHTML` ***Is a SECURITY RISK*** see p.228 for issues
      - Can be used on any element node
      - Can be used to retrieve and replace content
    - DOM manipulation can be safer that using `innerHTML` but, requires more code and can be slower
      - `createElement()` creates the new element
      - `createTextNode()` creates a new text node
      - `appendChild()` allows you to specify which element you want this node added to, as a child of it.
      - `innerBefore()` used to add the new element BEFORE the selected DOM node

    ```js
    let newEl = document.createElement('li'); // Creates a new element & stores it
    
    let newText =  document.createTextNode('quinoa'); // Creates a text node & stores it

    newEl.appendChild(newText); // Attach the new text node to the new element

    let position = document.getElementsByTagName('ul')[0]; // Find the position where the new element should be added

    position.appendChild(newEl); // Insert the new element into position
    ```

  - ***Removing Elements*** VIA DOM Manipulation
    1. Store the element to be removed in a variable
    2. Store the parent of that element in a variable
        - Use `parentNode`
    3. Remove the element from its containing element
        - Use `removeChild()`

    ```js
    let removeEl = document.getElementsByTagName('li')[3]; //  Element to be removed

    let containerEl = removeEl.parentNode;  // The containing element

    containerEl.removeChild(removeEl);  // Removes the element
    ```

- Comparing `innerHTML` with DOM Manipulation

- `innerHTML`
  - Advantages:
    - Uses less code than DOM manipulation methods
    - Faster than DOM manipulation when adding a lot of new elements to a page
    - Simple way to remove all content from 1 element (by assigning a blank string)
  - Disadvantages:
    - Should not be used to add content that comes from a user due to security risks
    - Can be difficult to isolate single elements
    - Event handlers may not work how intended

- DOM Manipulation
  - Advantages:
    - Suited for changing 1 element from a DOM fragment where there are many siblings
    - Does not effect event handlers
    - Easily allows a script to add elements incrementally
  - Disadvantages:
    - Can be slow if you have to make a lot of changes
    - You have to write more code to achieve the same thing that `innerHTML` achieves

Cross-Site Scripting (XSS) Attacks

- Defending Against XSS

  - Validate input goint to the server
    1. Use validation - only allowing the characters needed when supplying information
    2. Double-check validation on the server before displaying user content or storing it in a database
    3. The database may safely contain markup and script from trusted sources... because it is not trying to process it

  - Escape Data Coming From the Server & Database
    4. Escape ***ALL*** potentially dangerous characters before the data leaves the database
    5. Make sure that you are inserting content generated by users into certain parts of template fiiles
    6. DO NOT create DOM fragments containing HTML from untrusted sources

- Attribute Nodes
  - 2 steps to accessing and updating attributes
    1. Select the element node that carries that attribute and follow it with a '.'
    2. Then, use one of the methods or properties to work with that element's attributes
        - `getAttribute()` - gets the value of an attribute
        - `hasAttribute()` - checks if an element node has a specified attribute
        - `setAttribute()` - sets the value of the attribute
        - `removeAttribute()` - removes an attribute from an element
        - `className` - gets or sets the value of the _class_ attribute
        - `id` - get or sets the value of the _id_
        
