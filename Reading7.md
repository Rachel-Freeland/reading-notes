# HTML Tables & JS: Functions, Methods, and Objects

## Tables

### Basic Table Structure

- `<table>` - used to create the table. Table contents are written row by row
- `<tr>` - indicates the start of a row
- `<td>` - stands for 'table data' and represents each cell
- `<th>` - used like `<td>` but, represents the heading for either a column or row

- Even if a cell has no data in it, it should still be created but, left empty.
- The _scope_ attribute can be added to a `<th>` element to indicate if this is for a column or a row

- To span columns, use the attribute _colspan_ where the number given indicates the number of columns to span
- To span rows, use the attribute _rowspan_ where the number given indicates the number or rows to span

- Tables use elements to specify the head from the body from the footer
  - `<thead>`
  - `<tbody>`
  - `<tfoot>`

- Opening `<table>` tag should contain the _cellpadding_ attribute to add space inside each cell and the _cellspacing_ attribute to create space between the cells


## Functions, Methods, and Objects

### Creating an Object: Constructor Notation

- The ***new*** keyword combined with the object constructor create a blank object

```js
let hotel = new Object();
```

- Properties and methods can be added using dot notation

```js
hotel.name = 'Quay';
hotel.rooms = 40;
hotel.booked = 25;
hotel.checkAvailability = function() {
  return this.rooms - this.booked;
}
```

### Updating an Object

- With dot notation:

```js
hotel.name = 'Park';
```

- With array or square bracket syntax:

```js
hotel['name'] = 'Park';
```

### Creating Many Objects: Constructor Notation

- Sometimes the need will arise to create several objects that represent similar things
- Create a template with the object's properties and methods
- The name of a constructor function should begin with a capital (unlike other functions)
- The ***this*** keyword refers this property being associated with this object

```js
function Hotel(name, rooms, booked) {
  this.name = name;
  this.rooms = rooms;
  this.booked = booked;
  this.checkAvailability = function () {
    return this.rooms - this.booked;
  };
}
```

- When using the constructor function, you are creating ***instances*** of the object

```js
let quayHotel = new Hotel('Quay', 40, 25);
```

- Even when creating many objects using the same constructor function, the methods stay the same because they ***access***, ***update***, or ***perform*** a calculation on the data stored in the properties.

- Refer to pp. 110 and 111 for detailed example of using the constructor syntax and creating and accessing objects with the constructor notation

### Create The Object, Then Add Properties and Methods

- Literal Notation

```js
let hotel = {}

hotel.name = 'Quay';
hotel.rooms = 40;
hotel.booked = 25;
hotel.checkAvailability = function() {
  return this.rooms - this.booked;
};
```

- Object Constructor Notation

```js
let hotel = new Object();

hotel.name = 'Quay';
hotel.rooms = 40;
hotel.booked = 25;
hotel.checkAvailability = function() {
  return this.rooms - this.booked;
};
```

### Create An Object With Properties and Methods

- Literal Notation

```js
let hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  checkAvailability = function() {
    return this.rooms - this.booked;
  }
}
```

- Object Constructor Notation

```js
function Hotel(name, rooms, booked) {
  this.name = name;
  this.rooms = rooms;
  this.booked = booked;
  this.checkAvailability = function() {
    return this.rooms - this.booked;
  };
}

let quayHotel = new Hotel('Quay', 40, 25);
let parkHotel = new Hotel('Park', 120, 77);
```

### Arrays

- Are a special type of object
- Index numbers dictate the order of properties - starting with 0 for the first element of the array
- Arrays can store a series of objects
- Objects can hold arrays

### Built-In Objects

- ***Object Model:*** a group of objects, each of which represent related things from the real world. Together they form a model of something larger.
- Each of the built-in objects offer a different range of tools that help you write scripts for web pages

#### Browser Object Model (not all of this is from the reading)

- Contains objects that represent the current browser window or tab
- Topmost object would be the ***window*** object, which represents the current browser window or tab
  - document
  - frames
  - history
  - location
  - navigator
  - screen
  - self/window/parent
- ***The Window Object*** - represents the current browser window or tab
  - List of Properties and Methods located on pg 124
 
- Please refer to https://www.techfry.com/javascript-tutorial/javascript-browser-object-model for more information regarding the BOM

#### Document Object Model

- Uses objects to create a representation of the page
- Creates a new object for each element & each individual section of text
- Represents the web page loaded into the current browser window or tab
- See pg 126 for a list of properties and methods

#### Global JavaScript Objects

- Represents things that the JavaScript languate needs to create a model of.
- ***String Object*** common properties and methods (see pg. 128)
- ***Number Object*** common methods found on pg 132
- ***Math Object*** common properties and methods found on pg 134
- ***Date (and Time) Object** common methods found on pg. 137

#### Data Types Revisited

- 5 Simple data types

  1. String
  2. Number
  3. Boolean
  4. Undefined - a declared variable with NO value assigned yet
  5. Null - a variable with absolutely NO value
- Complex data type

  6. Object (includes arrays and functions)
