The reading for today is about HTML and javaScript. The HTML encompasses HTML structure, extra markup, layout and, process & design. The javaScript covers the ABCs of Programming for beginners.

# HTML

HTML is structured using elements. Almost all elements have 2 tags: an opening and a closing tag. There are a few exceptions to this rule but, the majority use 2. The elements covered in today's reading are:
  - **\<html\>** (everything between the opening and closing tag is considered HTML code unless otherwise noted)

  - **\<body\>** (the body of the page is what you see in the browser window)

  - **\<h1\>** (as well as the other levels of headings h2, h3, etc.)

  - **\<p\>** (paragraph)

  - **\<head\>** (this tag contains information _about_ that particular page)

  - **\<title\>** (this is displayed on the tab of the browser and is typically found in the \<head\> element)

  - **\<div\>** (used to group a set of elements together in one block-level box) _Use the id or class attribute to apply CSS style rules._

  - **\<span\>** (Serves as an inline equvialent of the \<div\> element) _This element is most commonly used to control the appearance of the content of these elements and is typically used with the id or class attribute._

  - **\<iframe\>** an abbreviation of inline frame. This element requires the use of the **src** (specifies the URL), **height** (expressed in pixels), **width** (expressed in pixels), **scrolling** (***note: not used in HTML5.*** This attribute indicates whether the iframe should have scroll bars), **frameborder** (***note: not used in HTML5.*** Indicates if the iframe should have a frame border.) and **seamless** (***note: new attribute in HTML5.*** This attribute is used in iframes where scrollbars are not wanted.)

  - **\<meta\>** resides inside the \<head\> element and is used with several attributes:
    - description
    - keywords
    - robots
    - author
    - pragma _Used to prevent the browser form caching the page._
    - expires _Used to indicate when a cached page should no longer be cached._
  
  - **\<header\>** and **\<footer\>** Used as a:
    - Main header or footer at the top and bottom of every page
    - A header or footer for an individual \<article\> or \<section\> within the page.

  - **\<nav\>** Used to contain the navigation for the site

  - **\<article\>** A container for any section of a page that could stand alone such as an article, blog entry, a comment, or forum post, etc.

  - **\<aside\>** When used inside an \<article\> element, it should contain info related to the article. When used outside of an \<article\> element, it is used to contain information regarding the whole page.

  - **\<section\>** Groups related content together and should have its own heading.

  - **\<figure\>** Used to  ontain any content that is referenxed from the main flow of an article... not just images. Typical uses include:
  
    - Images
    - Videos
    - Graphs
    - Diagrams
    - Code Samples
    - Text that supports the main body of an article

  - **\<figcaption\>** Provides a text description of the content of the \<figure\> element.

Start each page with a ***\<!DOCTYPE html\>*** to ensure that the page renders correctly. This tells the browser what to expect and should be placed on the very 1st line of the document.

  Placing comments within your code is important so that you and others that come after you will understand what your code is meant to do. Comments can be:

  - single line comments denoted by the //_

  - multiple line comments denoted by \<!\-\- and \-\-\> 

The **ID** attribute, a.k.a. "**gloabal attribute**", is intended to be used to uniquely identify an element from the other elements of the same type so that it can be styled differently or separately from the others.
  _The value should start with a letter or an underscore._

  The **CLASS** attribute works like the ID attribute but, it is used to uniquely identify more than one or two elements. _You can indicate an element belongs to more than one class by using a space between the class names._

  **BLOCK** level elements always appear to start on a new line. Examples of a block level element are: \<h1\>, \<p\>, and list elements whether ordered or unordered.

  **INLINE** level elements always appear to continue on in the same line as the last element. Examples of inline elements are: \<a\>, \<b\>, \<em\>. amd \<img\>.
  
  # JavaScript
  
  JavaScript makes web pages more interactive by:

1. Accessing content
   <p>You can use javaScript to select any element, attribute or text from an HTML page.</p>
2. Modifying content
   <p>You can use it to add elements, attributes, and text to the page or remove them.</p>
3. Program rules
   <p>You can specify a set of steps for the browser to follow which gives it access and the ability to change the content of a page.</p>
4. Reacting to events
   <p>You can specify that a script should run when a specific event has occurred, for example... when a button is pushed.</p>

A script is a series of instructions that a computer can follow to achieve a goal. A script is similar to a recipe or handbook. It is a series of instructions that a computer can follow step-by-step.

When writing a script you should know the intended goal then, you can design the script and then, last but, not least... you can code each step.
