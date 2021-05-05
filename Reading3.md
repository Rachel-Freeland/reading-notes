# HTML

## Ordered Lists

Ordered Lists are lists where each item is numbered.

- Ordered lists use the tags `<ol>` and `<li>`
- The `<ol>` and `</ol>` element tags are used to create the ordered list.
- The `<li>` and `</li>` element tags are used for each item in the list.
- For example:

```html
<ol>
  <li>Potatoes</li>
  <li>Water</li>
  <li>Milk</li>
</ol>
```

***Will render as:***

```html
1. Potatoes
2. Water
3. Milk
```

## Unordered Lists

Unordered Lists are preceded by a bullet points.

- Unordered lists use the tags `<ul>` and `<li>`
- The `<ul>` and `</ul>` element tags are used to create the bulleted list.
- The `<li>` and `</li>` element tags are used for each item in the list.
- For example:

```html
<ul>
  <li>Potatoes</li>
  <li>Water</li>
  <li>Milk</li>
</ul>
```

***Will render as:***

```html
▪ Potatoes
▪ Water
▪ Milk
```

## Definition Lists

Definitions Lists are made up of a set of terms along with the definitions for each of those terms.

- Definition lists use the `<dl>`, `<dt>`, and the `<dd>` tags.
- The `<dl>` and `</dl>` tags to create the list.
- The `<dt>` and `</dt>` tags are used to contain the term that is being defined.
- The `<dd>` and `</dd>` tags are used to contain the definition of the term defined.
- For example:

```html
<dl>
  <dt>Ectomorphic</dt>
  <dd>skinny</dd>
  <dt>Simple</dt>
  <dd>of humble origin or modest position</dd>
  <dt>House</dt>
  <dd>a building that servers as living quarters for one or a few families</dd>
</dl>
```

***Will render as***

```html
Ectomorphic
    skinny
Simple
    of humble origin or modest position
House
    a building that serves as living quarters for one or a few families
```

- Note: LIsts can also be nested within each other.

## CSS and Boxes

## Box Dimensions

- By default, a box is sized just large enough to hold its contents. However, you are able to set your own dimensions using the width and height properties.
- The most popular way to specify the size of the box is to use _pixels_, _percentages_, or _ems_.
- Pixels provide the mose accurate control.
- Percentages are used to size the box relative to the size of its container whether it is a browser window or another box.
- When working with ems, the box is sized according to the text that is within it.

### Limiting Width

- Limiting the width can be set according to **min-width** or **max-width**.
- The way to specify the size is the same as above with: _pixels_, _percentages_ or _ems_

### Limiting Height

- Limiting the height of the box is similar as with the width... **min-height** or **max-height**
- The way to specify size continues to be with _pixels_, _percentages_, or _ems_.

### Overflowing Content

- The **overflow** property tells the browser what to do if the content contain within a box is larger than the box itself.
- It can have 1 of 2 properties:
  1. hidden - which hides the extra content that does not fit.
  2. scroll - which adds a scrollbar to the box so that users can scroll to see the missing content.

### Border width

- The **border-width** property is used to control the size of the width of the border of the box.
- The way to specify the parameters is with: _pixels_ or with _thin_, _medium_, or _thick_
- Percentages **CANNOT** be used with this property
- You can also specify specific border widths with 4 separate properties:
  - border-top-width
  - border-bottom-width
  - border-right-width
  - border-left-width
- You can also specify different border widths for the four border values in one property. The values are in a clockwise order starting at the top, right, bottom, and left.
  - For example: border-width: 2px, 1px, 1px, 2px;

### Border Style

- The **border-style** property can take the following values:
  - solid - a single solid line
  - dotted - a series of square dots \(if the border is 2px wide then the dots are 2px with a 2px gap between dots\)
  - dashed - a series of dashes
  - double - 2 solid double lines \( the value of the border-width property creates the sum of the two lines\)
  - groove - appears to be carved into the page
  - ridge - appears to stick out from the page
  - inset - appears embedded in the page
  - outset - appears to be coming out of the screen
  - hidden/none - no border is shown
- Border styles can be changed individually like in border-width.
  - border-top-style
  - border-left-style
  - boder-right-style
  - border-bottom-style

### Border Color

- The border-color property can specify the color of the border using RGB values, hex codes, HSL values or CSS color names.
- The border-color can be styled individually using:
  - border-top-color
  - border-right-color
  - border-bottom-color
  - border-left-color
- It is possible to use shorthand to control all 4 border colors using clockwise position starting at the top.
  - For example:  border-color: darkcyan, deeppink, darkcyan, deeppink;

### Border Shorthand

The border property allows you to specify the width, style, and color of a border in one property in the same order as just listed.
For example:  border: 3px dotted #0088dd;

### Padding

- The **padding** property allows you to specify how much space should appear between the content of an element and its border.
- The value is most often specified in _pixels_ but, can take _percentages_ or _ems_
- ***NOTE:*** If a width is specified for a box, padding is added onto the width of the box.
- Different values can be specified for each side of the box
  - padding-top
  - padding-right
  - padding-bottom
  - padding-left

- Shorthand can also be used moving in a clockwise fashion starting at the top: padding: 10px 5px 3px 1px;

### Margin

- The **margin** property controls the gap between boxes.
- The property accepts values in _pixels_, _percentages_, and _ems_
- Can be specified individually using:
  - margim-top
  - margin-right
  - margin-left
  - margin-bottom

- Shorthand can be used in a clockwise fashion starting at the top: margin: 1px 2px 3px 4px;
  - Another form of shorthand denotes the top/bottom and the left/right margins: margin: 20px 10px;

### Centering Content

- If you want a box centered on a page or within the container that it sits, you can set the left-margin and the right-margin to "auto".
- A width should be set for the box when attempting to center because it will take up the full width of the page.
- The element that the box sits inside should have the text-align property set to a value of center
- The text-align property is inherited by child elements therefore, you also need to speicify a text-align property on the centered box.

### Change Inline/Block

- The **display** property allows you to turn an inline element into a block-level element, or vice versa, and can also hide an element from the page.
  - inline - this causes a block element to act like an inline element
  - block - this causes an inline element to act like a block-level element
  - inline-block - this causes a block-level element to flow like an inline element while retaining other features of a block-level element
  - none - this hides an element from the page

### Hiding Boxes

The **visiblity** property allows you to hide boxes from users but leaves a space where the element would have been.

- The property can take 1 of 2 values
  1. hidden - hides the element
  2. visible - shows the element
- Note: if you do not want a space to appear then, you should use the **display** property with a value of _none_.

### Border Images

The **border-image** property applies an image to the border of any box. It takes a background image and slices it into 9 pieces.
The corner pieces are always placed in the 4 corners of the box but, we can choose whether the sides are _stretched_ or _repeated_
This property requires 3 pieces of information:

1. The URL of the image
2. Where to slice the image
3. What to do with the straight edges... the values are:

- stretch
- repeat
- round - like repeat but if the tiles do not fit exactly, scales the tile image to be shown.

The box must have a border width for the image to be shown.

### Box Shadows

The **box-shadow** property sllows you to add a drop shadow around a box.

### Rounded Corners

Rounded corners are achieved using border-radius. the value indicates the size of the radius in pixels.
You can specify individual values for each corner using:

- border-top-right-radius
- border-bottom-right-radius
- border-bottom-left-radius
- border-top-left-radius

You can also use shorthand starting at the top and going in a clockwise fashion: border-radius: 5px, 10px, 5px, 10px;

### Elliptical Shapes

Elliptical shapes are created when you specify different distances for horizontal and vertical parts of the rounded corner.

- border-radius: 80px 50px; \(the first number is the horizontal and the second number is the vertical\)

Or, you can target just one corner:

- border-top-left-radius: 80px 50px;

## JavaScript

### Arrays

An **array** is a special type of variable. What makes it special is that it can contain more than one value. To create an array:

```js
  colors = ['white','blue', 'green' ];
```

You can access the data within the variable by calling its index number. Ex.:

```js
  el.textContent = colors[1];
```

### Decisions and Loops

### if/else Statements

An _if/else_ statement checks a condition. If the condition evaluates to _true_, the 1st code block is executed. If the condition evaluates to _false_, the 2nd code block is run instead.
An example of an if/else statement:

```js
  if (score >= 50) 
    {
      congratulate();
    } else {
      encourage();
    }
```

## Switch Statments

A _switch_ statement starts with a variable called a **switch** value. Each case indicates a possible value and the code that should run if the variable matches that value.
An example of a _switch_ statement:

```js
switch (level)
   {
    case 'One':
      title = 'Level 1';
      break;

    case 'Two':
      title = 'Level 2';
      break;

    case 'Three':
      title = 'Level 3';
      break;

    default:
      title = 'Test';
      break;
  }
```

## Loops

- A **FOR** loop should be used if you need to run the code a specific number of times.
An example of a **FOR** loop:

```js
for (var i = 0; i < 5; i++) 
{
  document.write\(i\);  
}
```

- A **WHILE** loop is used if you do not know how many executions of the code that should run.
An example of a **WHILE** loop:

```js
var i = 1;
var msg = ' ';

while (i < 10) 
{
  msg += ' x 5 = ' + (i * 5)
  i++;
}
```

- A **DO WHILE** loop is used if you want the loop to run at least once even if the condition evaluates to false.
An example of a **DO WHILE** loop:

```js
var i = 1;
var msg = ' ';

do {
  msg += i + ' x 5 = ' + (i * 5);
  i++;
} while (i < 2);
```
