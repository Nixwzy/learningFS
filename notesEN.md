
# NotesEN.md

**Disclaimer:** This document contains notes I have taken throughout my Fullstack development course. There is also a separate file available in Portuguese in the repository. You can access it here: [NotesPT.md](https://github.com/Nixwzy/learningFS/blob/main/notesPT.md). 

The NotesEN file may be updated slightly slower than NotesPT, as each entry requires translation from the original notes. While every effort is made to keep both files up to date, there might be minor delays in syncing new content between the two versions.

This file contains notes I took throughout my Fullstack development course. It documents concepts and practical examples related to technologies such as PHP, Laravel, NodeJS, and React. It's a personal learning repository where I record important information acquired during the classes.

## CSS Selector

```css
elementName {
    /* selects all occurrences of the element */
}

#elementId {
    /* selects the specific ID of the element */
}

.elementClass {
    /* selects the specific class of the element */
}

element, anotherElement, anotherElement2 {
    /* selects multiple elements at the same time */
}

element anotherElement {
    /* selects an element within another */
}
```

## CSS Borders

```css
element {
    border: width style color;
}
```

### Border Styles
- `solid` -> Most used
- `dotted`
- `dashed`
- `double`
- `groove`

### Border Positions

```css
element {
    border-bottom: width style color;
}

element {
    border-top: width style color;
}

element {
    border-left: width style color;
    border-right: width style color;
}

element {
    border-radius: width;
}
```

## Creating a round div using border (and also manipulating shapes)

```css
.div {
    background-color: #00FF00; /* making the div visible */
    width: 200px;
    height: 200px;
    border-radius: 100px; 
    border: 3px solid darkgreen;
    
    /* to ensure the div is round, the border-radius must be half the size of the square */
}
```

## Margin and Padding

Every HTML element has 4 distinct properties:
- Content (text);
- border;
- padding;
- margin.

### Manipulating padding

```css
/* Manipulating all sides of the padding with different values */
.example {
    padding: top, bottom, left, right;
}
.example {
    padding: 1px, 2px, 3px, 4px;
}

/* Manipulating top/bottom and left/right with the same value */
.example {
    padding: 10px, 20px;
}

/* Applying only one value to all sides */
.example {
    padding: 10px;
}
```

## Width and Height

width -> width  
height -> height  

There are ways to determine the size of width/height, some of them are:

```css
.example {
    width: 100px;
    /* 100 pixels */
}

.example {
    width: 100%;
    /* uses 100% of the available width of the parent element */
}

.example {
    width: auto;
    /* same as not defining anything */
}

.example {
    width: inherit;
    /* inherits the size of the previous item */
}

.example {
    min-width: 50px;
    max-width: 500px;
    width: 550px;
    /* The width will not be smaller than 50px or larger than 500px */
}
```

## Box-Sizing

```css
* {
    box-sizing: content-box;
    /* or */
    box-sizing: border-box;
}

/* The use of the asterisk in CSS is a universal selector. */
/* content-box: padding and border are not included in the dimensions, being added to the object. */
/* border-box: the total dimension value includes padding and border. */
```

## Anchor tag attributes (link)

### Target
Using target="_blank" within the anchor tag makes the page open in a new tab.

```html
<a href="page.html" target="_blank">New Page</a>
```

### Title
Using title makes a message appear when hovering over the link.

```html
<a href="page.html" title="Message">New Page</a>
```

## HTML Formatting

```html
<b>bold</b> -> Bold, without relevance semantics.
<strong>strong</strong> -> Bold, with relevance semantics.

<i>italic</i> -> Italic, without relevance semantics.
<em>emphasize</em> -> Italic, with relevance semantics.

<small>small</small> -> The font becomes smaller relative to the previously specified size.

<del>del</del> -> Strikes through the text.

<mark>mark</mark> -> Highlights the text. (Applies a default yellow background)

<sup>sup</sup> -> Displays superscript text.

<sub>sub</sub> -> Displays subscript text.

<u>underline</u> -> Underlines the text, without relevance semantics.

<abbr>abbr</abbr> -> Defines an abbreviation as a hover.

<code>code</code> -> Defines a code snippet within the text.

<pre>pre</pre> -> Defines preformatted text.
```

## Creating CSS Tables

```html
<table></table> -> Create a table;
<tr></tr> -> Creates rows (horizontal);
<td></td> -> Creates columns (vertical);
```

A basic table is:

```html
   <table class="table" width="400" border="1">
      <thead>
        <tr>
          <th>Header 1</th>
          <th>Header 2</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Content</td>
          <td>Content</td>
        </tr>
        <tr>
          <td>Content</td>
          <td>Content</td>
        </tr>
        <tr>
          <td>Content</td>
          <td>Content</td>
        </tr>
      </tbody>
    </table>

```
## Forms

To create a form:
```html
<form>
</form>
```

With two attributes:

### Action Attribute
```html
<form action="nextPage.html">

</form>
```
Defines where the form data will be sent.

### Method Attribute
Specifies how the data will be sent:

GET: sends data via URL (used for simple requests).
POST: sends the data in the request body (safer for sensitive data).
```html
<form method="GET">

</form>

<form method="POST">

</form>
```
### Input

```html
<form action="nextPage.html" method="GET">
    <input type="text" name="name"/>
    <input type="submit">
</form>
```
In the example above, whatever is entered in the input will be sent as data stored in the form of "name" to the next page.

### Some Types of Input

- text
    - email
    - password
- radio 
- checkbox
- submit

And many others, which can be checked here: [Input Types](https://www.w3schools.com/html/html_form_input_types.asp).

### Select

```html
<form action="nextPage.html" method="GET">
    <select name="name">
        <option value="value">Option 1</option>
        <option value="value">Option 2</option>

        <input type="submit">
    </select>
</form>
```
The submit will cause the selected value (value) from the select options to be sent to the next page.

- Selected Attribute:
```html
<form action="nextPage.html" method="GET">
    <select name="name">
        <option value="value">Option 1</option>
        <option value="value" selected>Option 2</option>

        <input type="submit">
    </select>
</form>
```
The option that will appear as default will always be the first unless the selected attribute is placed, which makes the option the default.

### Input Type File

When implementing an input type file, you must include, in the form attributes, the attribute **enctype="multipart/form-data"** so the server can receive the file.
```html
<form method="POST" action= "example.php" enctype="multipart/form-data">
    <input type="file" name="photo" accept="image/*" /> /* Example */
</form>
```

## Inheritance
In CSS, inheritance allows certain styles to be passed from a parent element to its children. For example, if you set the text color on the <body> element, all child texts will inherit that color unless another, more specific rule is applied.

## Specificity

Specificity defines the priority of rules applied to the same element. More specific rules take precedence over less specific ones. The order of specificity, in ascending order, is generally: type selectors (elements like div, p), classes (.class), and highest, IDs (#id). If two selectors have the same specificity, the last one in the code will be applied. **An example of this:**

**HTML**
```html
<html>
    <body>
    <div class="container">
        This is some text.   <!-- Text that will be changed -->
    </div>
  </body>
</html>
```

**CSS**

```css
.container {
    color: #FF0000; /* red color */
}

/* div {
    color: #0000FF; blue color
}
    This selection, if it competes with .container (class inside the div), the class wins due to the higher specificity of the .container class compared to the div element selector. That is, the red color remains. 


body .container {
    color: #00FF00; green color
}
    This selection, if it competes with .container, body .container wins due to higher specificity, as it involves both the body selector and .container. That is, the green color prevails.
 */
```

**Note:** CSS is processed from top to bottom, meaning that the browser reads and applies CSS in the order it appears in the file. 
So, if there are two rules with the same specificity for the same element, the last rule in the code takes precedence. 
This is particularly useful for overriding styles with newer or more specific rules.

## Units of Measurement in HTML and CSS
**em** -> relative (multiplicative) to the font size of the parent element. </br>
**rem** -> relative to the root element (the root element).</br>
**%** -> percentage (relative to the parent element).</br>
**vw and vh** -> viewport width and viewport height, measuring the width and height based on the viewport size.</br>
**vmin and vmax** -> based on the smallest and largest dimension of the viewport, respectively.</br>
**px** -> pixels </br>
**pt** -> points (1/72 in)</br>
**cm** -> centimeters</br>
**mm** -> millimeters</br>
**ch** -> width of the character</br>

## Object-fit
The **object-fit** property in CSS is used to specify how the content (usually images) of an element should fit within its container.

### Object-fit values:

1. **fill**:
   - This is the default value.
   - The content is stretched to completely fill the container, ignoring its original aspect ratio. This can cause the content to appear distorted.
     ```css
     img {
       object-fit: fill;
     }
     ```

2. **contain**:
   - The content is resized to fit entirely within the container, preserving its original aspect ratio. If the content doesn't fill the entire space, it will be centered, and the remaining space will be left blank.
     ```css
     img {
       object-fit: contain;
     }
     ```

3. **cover**:
   - The content is resized to cover the entire container, preserving its aspect ratio. This may result in part of the content being cropped, but it ensures there is no empty space within the container.
     ```css
     img {
       object-fit: cover;
     }
     ```

4. **none**:
   - The content retains its original size, without resizing. If the content is larger than the container, it will overflow; if it is smaller, there will be empty space.
     ```css
     img {
       object-fit: none;
     }
     ```

5. **scale-down**:
   - This value combines the behaviors of none and contain. The content will only be resized if it is larger than the container, but it will maintain its aspect ratio.
     ```css
     img {
       object-fit: scale-down;
     }
     ```

## Picture source media
In terms of responsiveness, the **picture** tag, together with the **source** tag and **media** attribute, helps the website adjust based on the screen size.

```html
<picture>
  <source media="(min-width: 650px)" srcset="image1.jpg">
  <source media="(min-width: 450px)" srcset="image2.jpg">
  <img src="image3.jpg" alt="Responsive Image">
</picture>
```
In this case:

If the screen width (using min-width) is 650px or more, image 1 will be displayed;</br>
If the screen width is between 450px and 649px, image 2 will be shown;</br>
If it doesn't meet either of these conditions and is smaller than 450px, image 3 will be shown. (It’s quite similar to an if-else statement, lol).</br>
## CSS: @media
The @media rule is a CSS feature that allows adapting the layout and design of a page based on changes in the screen size. Here’s an example:
```css
body {
  background-color: green; /* default background color will be green unless any of the @media queries are satisfied */
}

@media (min-width: 1000px) {
  body {
    background-color: blue; /* when the screen is at least 1000px, the background color will be blue */
  }
}
@media (min-width: 700px) and (max-width:999px) { /* when the screen is between 700px and 999px, the color will be red */
  body {
    background-color: red;
  }
}
@media (min-width: 300px) and (max-width: 699px) { /* when the screen is between 300px and 699px, the color will be yellow */
  body {
    background-color: yellow;
  }
}
```
No need to focus only on the background color; other properties can also be added to adapt the page layout based on the available screen size.
### @media onlyprint
```css
@media only print {
    body {
        display: none;
    }
}
```
The **only print** query essentially makes the style inside this media query apply only when the page is printed.

### @media orientation
The @media rule can be used to alter the layout based on the screen orientation, either landscape (horizontal) or portrait (vertical).

- Creating four divs (boxes) with the class box:
```html
  <body>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </body>
```
In this case, I want the boxes to be displayed vertically when the phone is in portrait mode and horizontally when it is in landscape mode.</br> To achieve this, simply add the following CSS:
```css
body {
  display: flex;
  background-color: #CCC; /* setting the background color */
}

.box { /* defining the properties for the boxes */
  width: 100px;
  height: 100px;
  border: 3px solid black;
  background-color: #CDC;
  margin: 2pt;
}

@media (orientation: landscape) { /* defining the @media rule for landscape mode */
  body {
    flex-direction: row;
  }
}

@media (orientation: portrait) { /* defining the @media rule for portrait mode */
  body {
    flex-direction: column;
  }
}
```
In this case, the page looks like this:

Landscape mode:
<p></p> 
<img src="assetsForNotes\landscapeExample.png"> 
<p></p> 
- Portrait mode: 
<p></p> 
<img src="assetsForNotes\portraitExample.png"> 
<p></p>

### @media aspect-ratio
The @media (aspect-ratio) rule is a media query used to apply styles based on the width-to-height ratio of the screen. </br> The aspect ratio is expressed as the relationship between the width and height of a device, like 16/9, 4/3, and so on.

```css
@media (aspect-ratio: 16/9) {
  body {
    background-color: blue; /* when the screen has a 16:9 ratio, the background will be blue */
  }
}
@media (aspect-ratio: 4/3) {
  body {
    background-color: green; /* when the screen has a 4:3 ratio, the background will be green */
  }
}
```