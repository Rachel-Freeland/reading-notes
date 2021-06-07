# HTML

## Images

To add an image, use the `<img>` tag. It is a self-closing tag. When using this tag, 2 attributes are a <b>MUST</b>:

- `src` which tell the browser where to find the image to be used... usually a relative URL
- `alt`, a.k.a <b>alt text</b>, provides a text description of the image is used by screen readers for the vision impaired

Other attributes that can be used are:

- `title` the contents of this attribute are usually what you see when you hover over an image, the tooltip.
- `height` this attribute sets the height of the image in pixels
- `width` this attribute, like the height attribute, sets the height of the image in pixels. An increasingly common practice is to specify the image height and width in CSS.

Placement of Images:

1. <b>Before a paragragh:</b> The paragraph will start on a new line AFTER the image
2. <b>Inside the start of a paragraph:</b> The 1<sup>st</sup> row of text will align with the bottom of the image
3. <b>In the middle of a paragraph:</b> The image is place between the words of the paragraph that it appears in

Placement of Images In Relation To HTML Elements:

1. <b>Block-Level Elements</b>
  
    - Block-level elements always appear on a new line. If the image is followed by a block-level element, the element will start on a new line AFTER the image.

2. <b>Inline Elements</b>

    - Inline elements sit WITHIN a block-level element and therefore, do not start on a new line.
    - If the `<img>` is inside a block-level, any text or other inline elements will flow AROUND the image.
  
3 Rules For Creating Images

Lossless compression makes it possible to reconstruct the image because there is no information lost during compression.

Lossy compression is irreversible data loss and the image CANNOT be reconstructed to its original state.

1. Save the images in the right format

    1. jpeg/jpg (lossy compression)
        - Can acheive compression ratios of 1:10 without any recognizable difference in quality
        - Best for images with many different colors
        - Use for images that contain a natrual scene or photo where variation in color and intensity is smooth
        - Does not support transparency
        - Supports around 16 million colors
    2. png (lossless compression)
        - Use for images with few colors or large areas of the same colors
        - Use for any image that needs transparency or for images with text & objects with sharp contrast edges such as logos
        - Supports transparency:
          - By inserting an alpha channel that allows partial transparency OR,
          - By declaring a single color as transparent
        - PNG8 vs PNG24
          - PNG8 can support up to 256 colors
          - PNG24 can support up to 16 million colors like jpg images
        - <b><i>NOTE:</i></b> this format is HIGHLY unsuitable for storing or transferring of high-resolution photos
    3. gif (lossless compression)
        - Use for images with few colors or large areas of the same colors
        - png compression is about 5 - 25% better that gif compression therefore, it is now mainly used for animated images
        - Supports transparency by declaring a single color in the color palette as transparent
        - Limited to 256 colors
        - Suitable for ads and banners and even memes

2. Save the images at the right size
    - Image sizes can be:
      - Reduced which will create an image that is quicker to download
      - Enlarged but, if you increase the size too much then, you will get a blurry or pixelated image.
      - Cropped however, when cropping, you could lose important details. It is best to just choose or save an image of the correct size

3. Measure the images in pixels

    - When sizing an image for use on the screen, you should ALWAYS set the dimensions in pixels (not centimeters or inches)

Vector Images

- Are computer graphic images that are defined in terms of points on a Cartesian plane which are then connected by lines and curves to form shapes
- These images can be scaled up or down without affecting the quality of it.
- Often created in programs like Adobe Illustrator

Figure And Figure Caption

- New element to HTML5
- Allows an image and its caption to be grouped and associated with each other
- Can have more than one image as long as they all share the same caption
- Uses the `<figure>` element to contain the image and the caption together and the `<figcaption>` contains the caption to the image(s)

## Color

Colors can be specified in 1 of 4 ways:

- RGB values

```css
p {
  color: rgb(100, 100, 90);
}
```

- Hex codes

```css
h2 {
  color: #ee3e80;
}
```

- Color names

```css
h1 {
  color: DarkCyan;
}
```

- HSL (Hue, Saturation, and Lightness) colors

  - Hue: the colloquial idea of color
  - Saturation: determines the amount of gray in the color
  - Lightness:the amount of white(lightness) or black (darkness) in a color
    - 0% lightness is black
    - 100% lightness is white
  - Alpha: determines transparency with numbers between 0 and 1.0
    - 0.5 represents 50% transparency
    - 0.75 represents 75% transparency

```css
body {
  background-color: hsl(0, 0%, 78%);
}

p {
  background-color: hsla(0, 100%, 100%, 0.5);
}
```

- Older browsers do not recognize HSL or HSLa values and it is a good idea to add an extra rule using the more traditional RGB, Hex code, or color name.

## Text

Typeface Terminology

- Serif: have details on the ends of the main strokes of the letters. Examples include:
  - Georgia
  - Times
  - Times New Roman
- Sans-serif: have straight ends to the letters and have a cleaner look. Examples include:
  - Arial
  - Verdana
  - Helvetica
- Monospace: every letter is the same width... commonly used for code due to the ability to line things up nicely. Examples include:
  - Courier
  - Courier New
- Weight: determines the boldness/thickness of the font
- Style: other than normal you have - <i>Italic</i> which has a cursive aspect to it and <i>Oblique</i> which takes the normal style and puts it on an angle
- Stretched: in <i>Condensed</i> letters are thinner and closer together and in <i>Extended</i> letters are thicker and further apart

Specifying Typefaces

- The <i>font-family</i> property allows you to specify the typeface that shoud be used for any text inside the element(s) to which the CSS rule applies.
- A list of fonts separated by commas from more specific 1<sup>st</sup> choice to a more generic  font
- If a font name is made up of more than one word, it should be put in double quotes
- Designers suggest no more than 3 different fonts for a page

```css
  body {
    font-family: Georgia, Times, serif;
  }
```

Size of Type

- The <i>font-size</i> property enables you to determine the size of font appropriate to your project
- There are several ways to specify the size, such as:

  - Pixels - indicated by a <i>px</i> and provides very precise control. Browser default size is 16px
  - Percentages - indicated by a <i>%</i>
    - 75% = 12px
    - 200% = 32px
    - If you set a percentage for the body and then one for another element in the body then the element within the body is a percentage of the body element's text. This means that if yuou choose 75% for the `body` and 75% for the `<p>` the text in the `<p>` will be 75% of the 12px meaning it will be 9px.
  - Ems: equivalent to the width of a letter 'm'

Units of Type Size

- Refer to p. 276 to see the equivalency charts for pixels, percentages, and ems.

More Font Choicea

- `@font-face`: allows you to use a font, even if it is not installed on the computer of the person browsing
- `font-family`: specifies the name of the font. This allows it to be used as a value of the <i>font-family</i> property
- `src`: specifies the path to the font
- `format`: specifies the format that the font is supplied in. The various font formats should appear in this order:
  
  1. eot
  2. woff
  3. ttf/otf
  4. svg
- Check out pp. 277 - 278 for useful links for fonts
- `font-weight`: allows you to create bold text. Your choices for this property are 'normal' or 'bold'
- `font-style`: allows you to create italic text. Your choices for this property are 'normal', 'italic', and 'oblique' (discussed earlier)
- `text-transform`: Text can be transformed to change the case of the text. Choices are: uppercase, lowercase, and capitalize (capitalizes the first letter of each word)
- `text-decoration`: choices are:
  - none: removes any decoration already applied
  - underline: adds a line under the text
  - overline: add a line over the top of text
  - line-through: adds a line through the words
  - blink: animates the text to make it flash on and off (frowned upon as it is considered annoying)
- Leading (pronounced ledding) describes the vertical space between line of text.
  - Incresing the line-height creates a vertical gap between lines of text larger
- Kerning describes the space between each letter
  - `letter-spacing` property allows you to control the space between each letter
  - `word-spacing` property allows you to control the gap between words. The default gap between words is usually around 0.25em
- `text-align` property allows you to control the alignment of the text. Choices are: left, right, center, and justify
- `vertical-align` property is <b>NOT</b> intended for you to vertically align text (although you can do it). It is more commonly used with inline elements such as, `<img>`, `<em>`, or `<strong>`. Values excepted are: baseline, sub, super, top, text-top, middle, bottom, and text-bottom. (Look at p. 286)
- `text-indent` property allows you to indent the first line of text within an element. Amount to indent is specified using _pixels_ or _ems_.
- `text-shadow` property is used to create a drop shadow which is a dark version of the word just behind it and slightly offset. This property takes 3 values for length and one for color:
  - The 1<sup>st</sup> length indicates how far to the left or right the shadow should fall
  - The 2<sup>nd</sup> length indicates the distance to the top or bottom the shadow should fall
  - The 3<sup>rd</sup> length is optional and indicates the amount of blur that should be applied to the drop shadow
  - The 4<sup>th</sup> value indcates the color of the drop shadow

Styling the First Line or Letter

- Uses `:first-letter` and `:first-line`

```css
p.intro:first-letter {
  font-size: 200%;
}

p.intro:first-line {
  font-weight: bold;
}
```

Styling Links

- Uses `:link` or `:visited`
  - `:link` allows you to set styles for links that have not been visited
  - `:visited` allows you to set styles for links that have been visited

Responding to Users

- `:hover` commonly used to change the appearance of links or buttons when a user hovers over the link or button
- `:active` commonly used for when a link or button is being activated such as, on a click
- `:focus` applies when an element has focus such as, a link you can click on.

Order that psudeo-classes should appear in:
  
  1. `:link`
  2. `:visited`
  3. `:hover`
  4. `:focus`
  5. `:active`

Attribute Selectors
  
- Refer to p. 292
