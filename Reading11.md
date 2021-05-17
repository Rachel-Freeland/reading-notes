# HTML For Reading 11

## References
<cite>HTML & CSS by Jon Duckett</cite>

## Images

- Specifying the size of images using html or css allows the browser to load more smoothly and faster because it knows how much space to leave on the page.

### Aligning images

_Note:_ the align attribute for images is no longer supported instead, do this:

1. Add a float property to the class that was created for the size image you want
2. Create new classes with names such as align-left or align-right. These classes are used in addition to the classes that indicate the size of the image

```html
<p><img src="img/magnolia-medium.jpg" alt="magnolia" class="align-left medium" /></p>
```

```css
img.align-left {
  float: left;
  margin-right: 10px;
}

img.medium {
  width: 250px;
  height: 250px;
}
```

### Centering images

***By Default: Images are `inline` elements***

- To center an image, it must be changed to a block element with the `display` property.
- 2 ways to center:
  1. On the containing element, you can use the `text-align` property with the value of _center_
  2. On the image itself, set the value to the left and right margins to _auto_

### Background Images

 - Use the `background-image` property and specify the url

### Repeating Images

- `background-repeat` you can choose _repeat_, _repeat-x_, _repeat-y_, or _no-repeat_
- `background-attachment` determines whether a background image stays in 1 place of moves as the user scrolls the page
  - You can choose _fixed_ or _scroll_

### Background Position

- The `backgroun-position` property takes a pair of values to specify where on the page the image should be displayed.
  - Horizontal and vertical pairs used: left top, left center, left bottom, center top, center center, etc...
  - You can also use a pair of pixels or percentages that represents the distance from the top left corner which is equal to: 0% 0%

### Shorthand

- `background` is the shorthand property for setting the background image
- The properties for this shorthand must be specified in the follow order, however, you can skip any value that you choose not to specify
  1. background-color
  2. background-image
  3. background-repeat
  4. background-attachment
  5. background-position

### Image Rollovers & Sprites

- 