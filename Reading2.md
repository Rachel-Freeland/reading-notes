Day 2's chapters cover manipulating text in headings, paragraphs, font styles, and the structural and semantic markup to bring your pages to life. We are also introduced to more CSS such as, what it is, how it works, and the rules, properties and, values associated with it. Our reading from the javaScript book introduces us to the basics of language... it's syntax, grammar, decisions, and loops.

# HTML

## Structure

**Building Structure**

HTML has 6 **heading "levels"** beginning with \<h1\> all the way to \<h6\> with the headings getting smaller with each increase in the heading number.

**Paragraphs** are will start on a new line and the \<p\> and the \</p\> tags are used.

**Bold** text can be accomplished through surrounding the desired text to be bolded with \<b\> and the \</b\> tags.

***Italics*** is accomplished through surrounding the desired text to be italicized with the \<i\> and the \</i\> tags.
The \<sup\> and \</sup\> tags surround text that should appear as a **superscript** while the \<sub\> and \</sub\> tags encase text that should appear as **subscript**.

**Whitespace** can be used by web page authors to make their code more readable. However, whenever a browser comes across 2 or more spaces next to each other, it only shows 1 space. Also, if it comes across a line break, that is treated as a single space as well. A.K.A. ***Whitespace collapsing***

If you need to **add a new line** to a paragraph section, you can use the \<br /\> tag. A **horizontal rule** can be used to create a break between themes and uses the \<hr /\> tag.

- Note: elements that have only one tag are known as ***empty elements***

## Semantics

To mark text of **strong** importance, it is surrounded by \<strong\> and \</strong\> tags and browsers typically render it as bold text.

To show **emphasis** in the text, surround the desired text to have emphasis with the \<em\> and \</em\> tags. The browser will render this text in italics.

**Quotes** can be handled in 2 ways:

- For longer quotes, you can use the \<blockquote\> and \</blockquote\> tags. This particular way of marking a quote indents the text. _Note: Do not use this just to indent a quote... use CSS to accomplished that task._
- For shorter quotes, you can use the \<q\> and \</q\> tags. This particular way surrounds the text in quote marks.

**Abbreviations and Acronyms** can both be used with the \<abbr\> and \</abbr\> tags from HTML5 and going forward. _If working in an older HTML, the \<acroynm\> and \</acronym\> tags can be used._

Work can be **cited** through the use of the \<cite\> and \</cite\> tags. The contents of the tags will be rendered in italics and can be used to indicate where the citation cam from. This should **NOT** be used for a person's name.

To mark the **defining instance of** a new term, surround the term to be defined with the \<dfn\> and \</dfn\> tags. Some browsers show the defined content in italics however, Safari and Chrome do not change the appareance of the text.

**Author Details** are containd in the \<address\> and \</address\> tags. Browsers often render the text inside the tags in italics. The element is used to contain the contact details of the author. 

To show content that has been **inserted** into a document, use the \<ins\> and \</ins\> tags. The inserted text is usually underlined. To mark the **deleted** text, use the \<del\> and \</del\> tags. The text marked as deleted is shown with a line through it.

To mark text that is no longer accurate or relevant, use the \<s\> and the \</s\> tags. This will create a single line through the outdated or inaccurate information.

## Understaning CSS

- For ***CSS***, one should treat the desired element like it has an invisible box that surrounds it.

- With CSS, you create rules that control how that box and its contents are presented. CSS rules contain 2 parts:
  - a _selector_ such as 'p' followed by an opening curly brace followed by the declaration.
  - a _declaration_  uses the property desired followed by the value such as, 'font-family: Arial;' followed by the closing curly brace.

When using an **external CSS** document it must be linked to the HTML file throught the use of the \<link\> tag that is an empty tag meaning that it is a self-closing tag. This tag should contain 3 attributes:

- _href_ which specifies the path to the file
- _type_ the value for a CSS file should be set to "text/css"
- _rel_ which denotes the relationship between the file and HTML page.

If you desire an **internal CSS** style then, you place the CSS rules for the page within the \<style\> and \</style\> tags.

## CSS Selectors

|**SELECTOR**|**MEANING**|**Example**|
|:---:|:---:|:---:|
|**Universal Selector**|All elements in the document |* \{ \}|
|**Type Selector**|Matches the element name| _h1_, _h2_, _p_ Targets the tags of these elements|
| **Class Selector**| Matches the class attribute of the same value.|p.note \{ \} Targets only the \<p\> values that have a value of note.|
| **ID Selector**| Matches the id attribute of the same value.| \#introduction \{ \}|
| **Child Selector**         | Matches the element that is a direct child of another.| li\>a \{ \}  Targets any \<a\> elements that are children of the _li_ element.|
|**Descendant Selector**|Matches an element that is a descendant of another specified element.| p a \{ \}   Targets **ANY** \<a\> that inside a \<p\> element.|
|**Adjacent Sibling Selector**        |Matches the next sibling of another| h1+p \{ \}     Targets ONLY the 1st element after any \<h1\> element.|
|**General Sibling Selector**| Matches an element that is a sbiling of another, although it does not have to be directly preceding the element. | h1~p \{ \}  If you had 2 \<p\> elements that are siblings of an \<h1\> element, this rule would apply to both.|

## CSS Precedence

- **Last Rule** states that if 2 selectors are identical, the latter of the 2 will take precedence.

- **Rule of Speificity** states that if 1 selector is more specific than another, then that rule will take precedence.

- **Importanat Rule** states that you can add ***!important*** after any property value to indicate that it should be considered the more important rule.

## JavaScript Basics

Each script is like a set of instructions.

Each step is known as a **statment**

Every statement should end with a ";"

JavaScript **IS** case sensitive.

Comments should be used to explain what your code does. 

- Multi-line comments are denoted by **/\*** and **\*/**.
- Single line comments are denoted by **//**.

A variable must be declared before using it. A
variable is declared by using the keyword, **var**. For ex.

  ```
  var quantity;
  ```

After a variable is declared, you can then assign a value to it. For ex.
  ```
  let quatity = 3;
  ```
  
## Data Types

1. **Numeric Data Type**: includes negatives and decimal values.
2. **String Data Type**: includes letters and other characters. 

- _Note: Strings are placed inside quote marks._
- Quotes used inside a string need to be "escaped" maening a backslash is required preceding the quotes.

3. **Boolean Data Type**: can be 1 of 2 values: _true_ or _false_.

## Rules for naming variables

1. Must begin with a letter, dollar sign, or an underscore. It ***MUST*** not start with a number.
2. The name can contain letters, numbers, dollar sign, or an underscore. You ***CANNOT*** use a dash or a period.
3. You ***CANNOT*** use **keywords** or **reserved** words.
4. All variables are case sensitive.
5. Use a name that describes the information that the variable stores.
6. When a variable is made up of more than one word, use camelCase.

## Arithmetic Operators

|Name|Operator| What it does|
|:---:|:---:|:---:|
| Addition |+| Adds one value to another.|
| Subtraction|-| Subtracts one value from another.|
| Division|/| Divides 2 values.|
| Multiplication|\*| Multiplies 2 values.|
| Increment|++| Adds one to the current number.|
| Decrement|--| Subtracts one from the current number.|
| Modulus|%| Divides 2 values and returns the remainder.|

## Decisions & Loops

Conditional statements allow your code to make decisions about what should or should not happen next.

Comparison operators and Logical Operators are used to evaluate and compare the condtional statements.

|**Comparison Operator**|**What it means**|**Example**|
|:---:|:---:|:---:|
|==|Is loosely equal to|'Hello' == 'Hello' returns _true_|
|===|Is strictly equal to|'3' === 3 returns _false_ because one is a string and the other is a numeric data type|
|!-|Is not equal to|'Hello' != 'Goodbye' returns _true_ because these are not the same|
|!==|Is strictly not equal to|'3' !== 3 returns _true_ because they are not the same data type|
|>|Greater than|5 > 3 returns _true_ because 5 IS greater than 4|
|<|Less than| 4 < 5|
|>=|Greater than or Equal to|5 >= 6 returns _false_ because 5 is not greater than or equal to 6|
|<=|Less than or Equal to|4 <= 3 returns _false_|

|**Logical Operator**|**What it means**|**Example**|
|:---:|:---:|:---:|
|&&|If both of the expresions evaluate to _true_ then, the expression returns _true_. If either expression evaluates to _false_ then, the expression returns _false_|true && true returns _true_  true && false returns _false_ false && false returns _false_|
|\|\||If either expression evaluates to _true_ then the expression returns _true_|true || true returns _true_ true || false returns _true_ false || false returns _false_
|!|Takes a single Boolean and inverts it|!\(2 < 1\) returns _true_ !true returns _false_ !false returns _true_|

- Logical expressions are evaluated left to right. If the 1st condition can provide enough information to establish an answer then, the 2nd expression is not evaluated.

## If Statements

An _if_ statement evaluates a condition and if it evaluates to _true_ then, the statements in the code block will execute.
An example of an _if_ statement:

  ```
  if \(userName == 'Bob'\)
    \{
      congratulate\(\);
    \}
  ```  

