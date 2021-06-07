# HTML

## Links

### Linking to other sites

- Links are created using the \<a\> element.
- The page is specified using the _href_ attribute.
- To write a link, it will look like:

```html
<a href="http://www.imdb.com">IMDB</a>
```

The text that resides between the tags will becomce a clickable link

### Linking to pages on the same site

When linking to other pages withing the same site, you can use a shorthand known as a **relative** URL.

Relative URLs are considered shorthand because you do not have to include the domain name.

```html

<ul>
  <li><a href="index.html">Home</a></li> // in the _same_ folder
  <li><a href="http://www.imdb.com">IMDB</a></li> // _external_ link
  <li><a href="music/listings.html">Listings</a></li> // _child_ folder
  <li><a href="movies/dvd/reviews.html">Reviews</a></li> // _grandchild_ folder
  <li><a href="../index.html">Home</a></li>  // _parent_ folder (indicates the folder above)
  <li><a href="../../index.html>Home</a></li>  // _grandparent_ folder (indicates 2 folders above)
</ul>
```
  
### Directory Structure

- If you need help understanding Data Structure, check out pg. 82 in the HTML book.

### Relative URLs

- Relative URLs can be used when linking pages within hyour own website.
- Because you do not need to state a domain, these URLs are considered _shorthand_.

### Email links

- The ***mailto:*** property starts up the user's email program and addresses an email to the one defined in the _href_ attribute.

```html
<a href="mailto:rachel.freeland1@gmail.com>Rachel's email</a>
```

### Opening links in a new window

- Opening new links in a target window can be done with the ***target*** property.
- Generally, you should avoid opening new windows but, if you do, it is good practice to inform the user that you are doing so.
- The property should be set to **_blank**

```html
<a href="http://www.imdb.com" target="_blank">IMDB</a>
```

### Linking to a specific part of the same page

- In order to link to a specific area of the web page, you need to use an **id=** property.
- When writing the link, you will insert a # in front of the id for the area of the page you want to access.

```html
<a href="#top">Top</a>
```

### Linking to a specific part of another page

- If the page you are linking to whether your own or another, you can link to a specific area of that page if the **id** property has been used.
- Just include the URL whether absolute or relative, it is similar to the way it is done for the same page... use a # in front of the section name.

```html
<a href="http://www.htmlandcssbook.com/#bottom">IMDB</a>
```

## Layout

- Layout is how we control the different elements of the web page

- CSS treats each HTML element as if it is in its own box.
- The box is either block-level box or an inline box.
  - Block-Level Elements:

  ```html
    - <h1>
    - <p>
    - <ul>
    - <li>
    <br />
    ```

  ```html
  - Inline Elements
    - <img>
    - <b>
    - <i>
    ```
  
- If one block-level box contains another block-level box then, the outer box is considered a **containing** or **parent** element.

### Controlling the position of elements

<h4>Positioning schemes:</h4>
<p>Allows the ability to control the layout of the page. Use the <i>position</i> property in CSS to specify the positioning of an element.
<b>Note:</b> You may also use the <i>float</i> property in combiniation with one of these poisitions.

- Normal flow

  - Every block-level element starts on a _new_ line and are stacked vertically on each other.
  - Even if the width of the boxes is small enough to allow them to appear side-by-side, they will still stack vertically. ***Note: This is the default behavior***
  - Each <b><i>block-level</i></b> element sits on top of the next one. This the **default** so, does not require a CSS property.

    Proper syntax concerning normal flow would be:

    ```css
    position: static;
    ```

- Relative positioning

  - This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been.
  - This does not effect the position of other surrounding elements.
  - Relative positioning moves an element to where it would have been in normal flow.

  - Using the offest properties indicates how far to move the box.

  - Box offset properties are usually stated in _pixels_, _percentages_, or _ems_

  ```css
    p.example {
    position: relative;
    top: 10px;
    left: 100px;
    }
  ```

- Absolute positioning

  - This positions the element in relation to its containing element
  - Absolute positioned elements will move as users scroll up and down the page.
  - When using a value of _absolute_ for the **position** property, the box will be taken out of normal flow and no longer affects the position of other elements on the page.

  - The box offset properties are used to position the box where the element should appear in relation to its containing element.

  - Box offset properties are usually stated in _pixels_, _percentages_, or _ems_

  ```css
  h1 {
    position: absolute;
    top: 0px;
    left: 500px;
    width: 250px;
  }
  ```

<B>Note:</b> The following are <i>box offset</i> properties that tell a browser how far from the TOP or BOTTOM and LEFT or RIGHT the item should be placed
  
- Fixed positioning

  - Is a form of absolute positioning however, they do not affect the position of surrounding elements AND the do NOT move as the user scrolls.
  - Positions the element in relation to the browser window instead of the containing element.

- Floating elements and the ***z-index***

  - Floating an element allows you to take it out of normal flow and position it to the far left or right of the containing box.
  - The element that was floated becomes a block-level element around which other content can flow.
  <h4>Overlapping Elements</h4>
   The z-index allows you to control which box appears on top.

  - The higher the number, the closer that element is to the front. Thus, an element with a z-index of 10 will appear over the top of one with a z-index of 5.
  - Also referred to as "stacking context", as if the blocks have been stacked on top of each other on a z axis.

### Floating Elements

- Floating an element allows you to take it out of normal flow and "float" it as far right or left of the containing element as possible.
- Anything else that sits inside the container with the floated element will flow around the floated element.
- <b>Should be used with</b> the <i>width</i> property, otherwise, results will be inconsistent.

#### Using Floats to place elements side-by-side

- The <i>float</i> property is commonly used to float boxes next to each other.
- The <i>height</i> of the box can affect where that element will sit.

  - One way to solve this problem is to set the height of the elements float next to each other all the same height as the tallest element that is being floated.

  - One fix for this issue is to use the <i>clear</i> property instead.

- The <i>clear</i> is used to tell the browser that <b>NO</B> element should touch the left, right, or both sides of the the box.

#### Creating Multi-Column Layouts with floats

- Achieved using the \<div\> element to represent each column and is used with these properties:
  
  - Width: sets the width of the colums
  - Float: positions the columns next to each other
  - Margin: creates a gap between the colums

- \<div\> elements can be nested and each can contain headings, paragraphs, and images.

### Fixed Width Layouts

- A fixed width layout does not change size according to the size of the brwoser window.
- Measurements tend to be in pixels.

- Advantages:

  - Pixel values are accurate
  - The designer has far greater control over the appearance and position of the items on the page
  - The designer can control the length of lines of text regardless of the user's window size
  - Image sizes will remain the same relative to the rest of the page.

- Disadvantages:

  - Can end up with BIG gaps around the edge of the page
  - If the user's screen resolution is higher that the designer's screen, the page and text can be smaller and harder to read.
  - If the user adjusts the font size, text may not fit within the allotted spaces
  - The page will oftentimes take up more vertical space than a responsive/liquid layout

### Liquid Layouts

- Responsive/Liquid layouts stretch and contract according to the size of the browser window.
- Measurements for this type of layout are usually stated in percentages.
- Advantages:

  - Pages will expand to fill the entire browser whether on a laptop or a large screen desktop
  - If the user has a small window, the page can contract to fit it without the user having to scroll to the side.
  - This design is tolerant of the users setting font sizes larger than wha the designer intended.

- Disadvantages:

  - If the designer doesn't control the width of sections of the page then, the page can look very different than intended.
  - If using a wide window, the lines of text can become very long.
  - If using a very narrow window, the lines of the text can appear squished up or only a couple of words per line.
  - If the page contains a fixed width item such as, an image, the image can overlow into the text.

## Layout Grids

- Check out the grid layouts on pp. 387 - 404

## Functions, Methods, and Objects

- Function: a series of instructions that, when grouped together, perform a specific function. A function contains "reusable" script so that you are not typing the same instructions over and over again.
- "Calling" a function, tells it to perform the function.
- Parameters: Pieces of information from outside the function that provides the function with the information needed to carry out the instructions.
- Return value: the response you get from the function, if you are expecting one.
- A function is "declared" when you use the <b>function</b> keyword and then give the function a name, the <b>function name</b> using camelCase. The curly braces { } denote the beginning and end of the <b>code block</b>. Within the code block are a statement or series of statements that perform a task.
- Example of a function that does not take any parameters:

```js
function functionName() {
  document.write('Hello');
}
```

- To call a function, it should look something like this:

```js
sayHello();
```

- Declaring a function that takes a parameter or parameters should look similar to this;

```js
function getArea(width, height) {
  return width * height;
}
```

- To call a function that needs parameters:

```js
getArea(3, 5);
```

- Some functions return information to the code that called them. For example:

```js
function calculateArea(width, height) {
  let area = width * height;
  return area;
}
```

<b>Note:</b> The interpreter leaves the function when <b><i>return</i></b> is used.

- How to set up a function to return multiple values:

```js
function getSize(width, height, depth) {
  let area = width * height;
  let volume = width * height * depth;
  let sizes = [area, volume];
  return sizes;
}
```

- How to access the different values from one function:

```js
let areaOne = getSize(3, 2, 3)[0];
let volumeOne = getSize(3, 2, 3)[1];
```

- Declaring a function and giving it a name allows the developer to call and use that function later in the code.\

- Function expression: is a function used where the interpreter would expect an expression. The name is usually <i>omitted</i>. A function without a name is a.k.a "anonymous function."

```js
let area = function(width, height) {
  return width * height;
};

let size = area(3, 4);
```

- <b>IIFE</b> - <b>I</b>mmediately <b>I</b>nvoked <b>F</b>unction <b>E</b>xpressions, pronounced "iffy," are not given a name. Instead, they are called immediately like below...

```js
let area = (function() {
  let width = 3;
  let height = 2;
  return width * height;
}());
```

### When to use Anonymous Functions and IIFEs

- As an argument when a function is called (to calculate the value for that function)
- To assign the value of a property to an object
- In event handlers and listerners to perform a task when an event occurs
- To prevent conflicts between two scripts that might use the same variable names

## Variable Scopes

- The location where you declare your variable will affect where it can be used within your code. If you declare it within a function, it can only be used within that function.

- A <b>Local variable or function-level variable</b> are variables declared with that function and can only be used within that function. This is known as, <b>local scope or function-level scope</b>

- Local variables are created by the interpreter when the function is run and removed as soon as the function has finished its task.
  - If the function is run twice, you may get 2 different values returned
  - 2 different functions can use variables of the same name without any conflict

- <b>Global variables</b> are created outside of a function and can be used anywhere within the script. It is considered to have a <b>global scope</b>

- Global variables are stored in memory for as long as the web page is loaded in the web browser.
  - Global variables take up more memory than local variables
  - Global variables have an increased risk of naming conflicts
