# HTML

Today's reading is a repeat from class Reading 4

## Key Concepts in Positioning Elements

- In CSS, each HTLML element is treated as if it was its own box. 2 types of boxes:
  - block-level - starts a new line after each element and are the main building blocks of any layout
    - You can actually control the height and width of these elements with the _height_ and _width_ property
    - Has a vertically-based layout
    - Examples of block-level elements:
      - `<h1>`
      - `<p>`
      - `<ul>`
      - `<li>`
      - `<div>`

  - Inline-block - flows in between surrounding text
    - Has a horizontally-based layout
    - Examples of inline elements:
      - `<img>`
      - `<b>`
      - `<i>`
      - `<span>`

- Containing or Parent elements are the outer box to which the elements on the inside are contained
- If, a box is nested inside several other boxes, the containing / parent element is ALWAYS the DIRECT parent of that element

### Flexbox Layout (not in reading but, discussed in class)

- I wanted more information about flexbox layouts. This is not contained in the reading so, I got my information at <https://css-tricks.com/snippets/css/a-guide-to-flexbox/>

- <b>Flexbox</b> is best used in componenets of an application and small-scale layouts while <b>grid</b> layout is best for large-scale layouts
- Flex containers expand to allow items to fill available free space and shrink them when needed
- Has a flex-flow based layout
- ![Flexbox terms](https://css-tricks.com/wp-content/uploads/2018/11/00-basic-terminology.svg)
- Items are laid out according to either the main axis or the cross axis
  - main axis: is the primary which items are laid out. This will vary according to the `flex-direction` property
  - cross axis: sits perpendicular to the main axis and varies according to the main axis

- ***Properties*** to set up for the ***parent container:***
  - `display:` this enables flex content for all the direct children

```css
div {
  display: flex; /* or inline-flex */
}
```

- `flex-direction:` defines the direction of the flow of items and establishes the main axis
  - Options for this property are:
    - row: establishes the direction of rows going left to right `ltr`; right to left `rtl`
    - column: same as row but, aligns top to bottom
    - row-reverse: reverses the direction of the row
    - column-reverse: reverses the direction of the column
  
  ```css
  div {
    flex-direction: row | row-reverse | column | column-reverse;
  }
  ```

- `flex-wrap` by default, css attempts to place flex items onto one line however, you can change that with this property
  - Options for this property:
    - `nowrap` (default): does what it says... it will fit all flex items onto one line
    - `wrap` will wrap on multiple lines, top to bottom
    - `wrap-reverse` wraps from bottom to top
  
  ```css
  div {
    flex-wrap: nowrap | wrap | wrap-reverse;
  }
  ```

- `flex-flow` is the shorthand property for flex box which combines the `flex-direction` and `flex-wrap` into one property. _Default_ value set at `row nowrap`;

 ```css
div {
  flex-flow: column wrap;
}
```

- `justify-content` defines the alignment along the ***main axis***

  <img src="https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg" alt="examples" height="350px" width="200px">

  - Examples above give you an idea of how the different options work

- `align-items` determines the default behavior for how items will be laid out but, this is for the ***cross axis***

  <img src="https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg" height="400" width="350">

  - This gives you an idea of the options and how they work

- `align-content` is similar to `justify-content` but, works on resolving extra space in the cross axis
- ***Note:*** this only works when `flex-flow` is set to with `wrap` or `wrap-reverse`

  <img src="https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg" height="400" width="300">

  - Note: the different options and how they work. They work just as the sound like they do.

- While the ***parent container*** is important, we must not forget that the ***child container*** needs some properties set as well. 

- ***Child Container Properties***
  - Items can be given an order and by default are laid out in source order. But, you can take control of this order with the `order` property
  
  ```css
  .item {
    order: 5; /* default is 0*/
  }
  ```

  <img src="https://css-tricks.com/wp-content/uploads/2018/10/order.svg" height="282" width="350">

  - To me, this kind of acts like the z-index but, in a slightly different way

- `flex-grow` gives an item the ability to grow. If all items are set to 1, the space is divided evenly among them. If you give one of the items a 2, then it would be twice the size of the others

  <img src="https://css-tricks.com/wp-content/uploads/2018/10/flex-grow.svg" height="300px" width="200px">

- `flex-shrink` shrinks the item in the same way that `flex-grow` works.

- `flex-basis` defines a default size for an element before distributing the remaining space. The ***auto*** keyword tells the browser to look at that element's height and width while ***content*** means to size it based on what it contains
- `flex` this is the shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`. Only the first parameter is required. ***Default is set to*** `0`, `1`, and `auto`
  - ***NOTE*** This is PREFERRED over the individual properties

```css
.item {
  flex: none | <'flex-grow'> <'flex-shrink'> || 'flex-basis'
}
```

- `align-self` overrides the default (or specified by `align-items`) individual flex items

## References

<cite>https://css-tricks.com/snippets/css/a-guide-to-flexbox/</cite><br/>
<cite>HTML & CSS by Jon Duckett</cite>