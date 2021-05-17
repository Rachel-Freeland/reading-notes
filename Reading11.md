# HTML For Reading 11

## References
<cite>HTML & CSS by Jon Duckett</cite>

## Images

- Specifying the size of images using html or css allows the browser to load more smoothly and faster because it knows how much space to leave on the page.

### Aligning images p. 411

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

### Centering images p. 412

***By Default: Images are `inline` elements***

- To center an image, it must be changed to a block element with the `display` property.
- 2 ways to center:
  1. On the containing element, you can use the `text-align` property with the value of _center_
  2. On the image itself, set the value to the left and right margins to _auto_

### Background Images p. 413

 - Use the `background-image` property and specify the url

### Repeating Images p. 414

- `background-repeat` you can choose _repeat_, _repeat-x_, _repeat-y_, or _no-repeat_
- `background-attachment` determines whether a background image stays in 1 place of moves as the user scrolls the page
  - You can choose _fixed_ or _scroll_

### Background Position p.415

- The `backgroun-position` property takes a pair of values to specify where on the page the image should be displayed.
  - Horizontal and vertical pairs used: left top, left center, left bottom, center top, center center, etc...
  - You can also use a pair of pixels or percentages that represents the distance from the top left corner which is equal to: 0% 0%

### Shorthand p. 416

- `background` is the shorthand property for setting the background image
- The properties for this shorthand must be specified in the follow order, however, you can skip any value that you choose not to specify
  1. background-color
  2. background-image
  3. background-repeat
  4. background-attachment
  5. background-position

### Image Rollovers & Sprites p.417 - 418

- A `rollover` is when you create a link or button that changes to a 2<sup>nd</sup> style
- This can be achieved by:
  - Setting a background image for the link or button that has 3 different styles for the same button but, only allows enough space to show 1 at a time.
- A `sprite` is when a single image is used for several different parts of an interface
  - Advantage to using `sprites` is that the page loads much faster since the browser only needs to request 1 image rather than many.

## Practical Information

### SEO - Search Engine Optimization p.479 - 482

- SEO helps users find you site when using a search engine
- There are 7 key places where ***keywords*** can appear to help improve findability
  1. `Page title`
  2. `URL / Web address` (name of the file appears in URLs, keywords should be part of file name)
  3. `Headings` (keywords in the headings helps search engines know what your page is about)
  4. `Text` (repeating keywords in the main body)
  5. `Link text` (using keywords in the text that creates the link between pages)
  6. `Image alt text` (accurate descriptions of pictures/images)
  7. `Page descriptions` (using the `<meta>` tag within the `<Head>` element)

#### Identifying Keywords and Phrases

1. Brainstorm
2. Organize > group keywords into separate lists for the different sections or categories of your site
3. Research > there are tools that can help you by suggesting other keywords based on the keywords you enter
4. Compare > compare the keywords to see which are likely to help your page rise to the top
5. Refine > pick your the keywords to focus on
6. Map > pick 3 - 5 keywords that map to each page of your site

### Analytics p. 483 - 487

- As soon as people start coming to your site, you can start analyzing it.
- Google Analytics is a free service and one of the best out there
- Allows you to see how many people are coming to your site, page views, pages per visit, average time on site, etc
- Allows you to see what visitors are looking at, pages, landing pages, top exit pages, and bounce rate (people who left on the same page that they arrived on)
- Allows you to see where traffic is coming from

### Putting Your Site On The Web p. 487 - 489

- In order to put your site on the web you will need to choose a domain name and a web hosting site
- Transfering code and images is done via FTP & 3rd party tools
