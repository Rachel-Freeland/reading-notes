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
- If one block-level box contains another block-level box then, the outer box is considered a **containing** or **parent** element.

### Controlling the position of elements

Positioning schemes:

- Normal flow

  - Every block-level element starts on a _new_ line and are stacked vertically on each other.
  - Even if the width of the boxes is small enough to allow them to appear side-by-side, they will still stack vertically. ***Note: This is the default behavior***

- Relative positioning

  - This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been.
  - This does not effect the position of other surrounding elements.

- Absolute positioning

  - This positions the element in relation to its containing element
  - Absolute positioned elements will move as users scroll up and down the page.
  
- Fixed positioning

  - Is a form of absolute positioning however, they do not affect the position of surrounding elements AND the do NOT move as the user scrolls.
  - Positions the element in relation to the browser window instead of the containing element.

- Floating elements and the ***z-index***

  - Floating an element allows you to take it out of normal flow and position it to the far left or right of the containing box.
  - The element that was floated becomes a block-level element around which other content can flow.
  - The z-index allows you to control which box appears on top.

#### Normal Flow

  Each block-level element sits on top of the next one. This the **default** so, does not require a CSS property.

  Proper syntax concerning normal flow would be:

  ```css
    position: static;
  ```

#### Relative Positioning

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

#### Absolute Positioning

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

#### Fixed Positioning

#### Overlapping Elements

#### Floating Elements

#### Using Floats to place elements side-by-side

#### Clearing Floats

#### Creating Multi-Column Layouts with floats

### Fixed Width Layouts

### Liquid Layouts

## Layout Grids

## Multiple Style Sheets
