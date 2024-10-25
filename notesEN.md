
# NotesEN.md

**Disclaimer:** This document contains notes I have taken throughout my Fullstack development course. There is also a separate file available in Portuguese in the repository. You can access it here: [NotesPT.md](https://github.com/Nixwzy/learningFS/blob/main/notesPT.md).

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
## Form Attributes

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
