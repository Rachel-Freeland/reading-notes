# HTML & JS for Reading 9

## HTML

- Chapter 7 "Forms" pg. 144 - 175
- Chapter 14 "Lists, Tables, & Forms" p. 330-357
- <cite>HTML & CSS by Jon Duckett</cite>

## JS

- Chapter 6 "Events" p. 243- 292
- <cite>JavaScript & JQUERY by Jon Duckett</cite>

## Forms

### Form Controls

- For adding text:
  - Text input: used for a single line of text such as, email address or names
  - Password input: like the text input but, masks the characters entered
  - Text area: for larger area for text such as, messages or comments

- For making choices:
  - Radio buttons: user to select 1 out of a number of choices
  - Checkboxes: user can select and unselect options
  - Drop-down boxes: user must pick 1 out of a number of options

- For submitting forms:
  - Submit buttons: submits your data from the form to another web page or server
  - Image buttons: similar to a submit button but, allows the use of an image
  - File upload: allows users to upload files to a site

### Form Structure

- `<form>` this is where the form controls live
- `action` attribute: REQUIRED by the `<form>` element. The value it takes is the URL for the server that will receive the information in the form
- `method` property: forms are sent using 1 of 2 methods:
  - _get_: with this method, the form values are added to the URL specified in the `action` attribute. This method is best for:
    - short forms
    - when just retrieving data from the web server
  - _post_: values are sent in HTTP headers. This method should be used for:
    - when allowing users to upload a file
    - when the form contains sensitive information
    - adding information to, or deleting information from a database

```html
<form action="http://www.example.com/subscibe.php" method="get">
  <p>This is where the form controls will appear</>
</form>
```

### Text Input p. 152

- `<input>` used to created several different form controls
- `type="text"` creates a single line of input
- `name` the value of this attribute identifies the form control and is sent along with the information to the server
- `maxlength` used to limit the number of characters into a text field
- `size` attribute should no longer be used on forms

```html
<form action="http://www.example.com/login.php">
<p>Username:
  <input type="text" name="username" size="15" maxlength="30" />
</p>
</form>
```

### Password Input p. 153

- `type="password"` creates a text box that blocks out the characters ***Does not meant that the data is being sent securely***
- `name` indicates the name of the password input
- `size, maxlength` same as for text input

```html
<form action="http://www.example.com/login.php">
  <p>Username:
    <input type="text" name="username" size="15" maxlength="30" />
  </p>
  <p>Password:
    <input type="password" name="password" siez="15" maxlength="30" />
  </p>
</form>
```

### Text Area p. 154

- `<textarea>` used to create a text box that accepts multiple lines of text ***Note: unlike the other form controls, this one NEEDS a closing tag***
- Use the `width` and `height` however old code may have _cols_ and _rows_

```html
<form action="http://www.example.com/comments.php">
  <p>What did you think of this gig?</p>
  <textarea name="comments" cols="20" rows="4">Enter your comments...</textarea>
</form>
```

### Radio Button p. 155

```html
<form action="http://www.example.com/profile.php">
  <p>Please select your favorite genre:
  <br />
  <imput type="radio" name="genre" value="rock" checked="checked" /> Rock
  <input type="radio" name="genre" value="pop" /> Pop
  <input type="radio" name="genre" value="jazz" /> Jazz
  </p>
</form>
```

### Checkbox p. 156

```html
<form action="http://www.example.com/profile.php">
  <p>Please select your favorite music service(s):
  <br />
    <input type="checkbox" name="service" value="itunes" checked="checked" /> iTunes
    <input type="checkbox" name="service" value="lastfm"> Last.fm
    <input type="checkbox" name="service" value="spotify"> Spotify
  </p>
</form>
```

### Drop Down List Box p. 157

- `<select>` allows users to select 1 option from the drop down lis
- `<option>` specifies the options that the user can select from

```html
<form action="http://www.example.com/profile.php">
  <p>What device do you listen to music on?</p>
  <select name="devices">
    <option value="ipod">iPod</option>
    <option value="radio">Radio</option>
    <option value="computer">Computer</option>
  </select>
  </p>
</form>
```

### More types of forms that are similar to above

- Multiple Select Box p.158

- File Input Box p. 159

- Submit Button p. 160

- Image Button p. 161

### Button & Hidden Controls p. 162

- `<button>` allows users control over how their buttons appear and allows other elements to inside the button
- `type="hidden"` these controls are not shown on the page however, you can see it if you use ***View Source***. This allows the page authors to add values to the form that the user cannot see.

```html
<form action="http://www.example.com/add.php">
  <button><img src="images/add.gif" alt="add" width="10" height="10" />Add</button>
  <input type="hidden" name="bookmark" value="lyrics" />
</form>
```

### Labeling Form Controls p.163

### Grouping Form Elements p. 164

### Form Validation p. 165

### Date Input p. 166

### Email & URL Input p.167

### Search Input p. 168


## Lists, Tables, and Forms

### Lists p. 333 - 336

- `list-style-type` allows you to control the bullet points
- `list-style-images` allows you to use an image as your bullet point
- `list-style-position` indicates whether the marker should appear inside or outside the containing box
- `list-style` is the CSS shorthand for lists - the marker's style, image and position can be listed in any order

### Tables p. 337 - 340

- `empty-cells` - specifies whether or not to show the borders of empty cells
- `border-spacing`, `border-collapse` - allows you control over the distance between adjacent cells

### Forms p. 342 - 347

- Styling Text Inputs
  - `font-size`
  - `color` and `background-color`
  - `border` and `border-radius`
  - Psuedo classes
    - `:focus` changes the background color of the text input whe it is being used
    - `:hover` 
  - `background-image` adds a background image to the box

- Styling Submit Buttons
  - `color`
  - `text-shadow`
  - `border-bottom`
  - `background-color`
  - Psuedo class
    - `:hover`

- Styling Fieldsets & Legends
  - `width`
  - `color` and `background-color`
  - `border` and `border-radius`
  - `padding`

- Cursor Styles
  - `cursor` property allows you to control the type of cursor that should be displayed
    - Values accepted:
      - auto
      - crosshair
      - default
      - pointer
      - move
      - text
      - wait
      - help
      - url("cursor.gif");

- Web Developer Toolbar p. 348
  - <www.chrispederick.com/work/web-developer>
  - Helpful extension for Firefox and Chrome that provides tools to show you the CSS styles that apply to an element when you hover over it.
    1. Outlines draws a red outline when you hover over an element
    2. Structure allows you to see the structure of the element when you hover over it
    3. CSS Styles when hovering over the element click with your mouse to display the CSS

## JS - Events p. 243 - 292

- Events are the browser's way of indicating when something has happened, such as, a button has been clicked
- Binding is the process of stating which event you are waiting to happen
- List of different event types on pp. 246 - 247
- Events are ***fired*** or ***raised*** when triggered such as, when a user clicks on a link
- Events ***trigger*** a function or script

- 