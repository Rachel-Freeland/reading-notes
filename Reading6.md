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
      2. Select multiple nodes (nodelists) - 3 Common ways to select multiple elements
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


