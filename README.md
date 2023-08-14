# Syntax, Styles & Selectors

## Intro

CSS selectors are a crucial part of the language, as they allow web developers to target specific HTML elements and apply styles to them. A CSS selector is a pattern that is used to select one or more HTML elements, which can then be styled using CSS properties.

## Lesson Objectives

- Understand what CSS is
- Understand how CSS works
  - Understand the cascading effect of CSS
- Understand what a CSS Selector is

## Lesson Content

### Syntax

Below is an example of the syntax for CSS

```css
/* 
I'm a comment! 
comments in CSS are 
multiline by default
*/

/*
Type Selectors for elements like 
body, p, h1, h2, img
*/
typeSelector {
    property-name: value; 
}

/*
Class Selectors for styles we use in 
more than one place
*/
.classSelector {
    property-name: value;
}

/*
ID Selectors for styles we use in one 
place
*/
#idSelector {
    property-name: value;
}

/*
Attribute Selectors for styles on an 
element with a certain value on the 
specified attribute
*/
selector[attribute='value'] {
    property-name: value;
}

/* 
Descendant selectors are used to select 
the decendent of another element like the 
list items in an unordered list
*/
parentSelector childSelector {
    property-name: value;
}

/*
Pseudo-class selectors are for selecting 
an element in a certain state
*/
selector:state{
    property-name: value;
}
```

### Styles

Before we implement an external CSS Stylesheet, the `HTML` style tag is notable but not recommended. We can use `<style>` to embed our styles in the `HTML` but this makes our page less accessible, see below for the correct usage.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Acme Inc - About</title>
    
    <!-- style tag -->
    <style>
        p {
            color: red;
        }
    </style>
    <!-- do not use -->

</head>
<body>
<!-- Content for page -->
</body>
</html>
```

### Selectors

There are several different types of CSS selectors, including:

#### `Type selectors`

These are the most basic selectors and are used to select all elements of a particular type.

- The selector `p` would select all `paragraph elements` on a web page.

```css
p {
    /* Type Selectors for elements like body, p, h1, h2, img */
    color: red; 
}
```

#### `Class selectors`

These are used to select elements based on their class `attribute`. Class selectors are denoted by a full-stop/period (`.`) followed by the class name.

- The selector `.my-class` would select all elements with the `class` name `my-class`.

```css
.text-green {
    /* Class Selectors for styles we use in more than one place */
    color: #00ff00;
}
```

#### `ID selectors`

These are used to select elements based on their ID `attribute`. ID selectors are denoted by a hash symbol (`#`) followed by the ID name.

- The selector `#my-id` would select the element with the ID `my-id`.

```css
#contentSection {
    /* ID Selectors for styles we use in one place */
    background-color: black;
}
```

#### `Attribute selectors`

These are used to select elements based on their attributes, such as their `href` or `src` attributes. Attribute selectors are denoted by square brackets (`[]`) followed by the attribute name and, optionally, the attribute value.

- The selector `a[href='https://www.example.com']` would select all anchor elements with an `href` attribute that matches `https://www.example.com`.

```css
a[href='http://google.com']{
    /* Attribute selector example */
    color: red;
}
```

#### `Descendant selectors`

These are used to select elements that are descendants of other elements. Descendant selectors are denoted by a space between two selectors.

- the selector `ul li` would select all list item elements that are descendants of unordered list elements.

```css
ul li {
    /* Descendant selector example */
    font-weight: bold;
}

```

#### `Pseudo-class selectors`

These are used to select elements based on their state or position within the document.

- The `:hover` pseudo-class selector is used to apply styles to an element when the user hovers over it with their mouse.

```css
    a:hover{
        /* is green when mouse is hovering */
        color: green;
    }
```

These are just a few examples of the many different types of `CSS selectors` available.

By learning how to use selectors effectively, web developers can create dynamic and visually appealing websites that are easy to navigate and use.

## Resources

### W3 Schools

- [CSS](https://www.w3schools.com/w3css/default.asp)
- [CSS Selectors](https://www.w3schools.com/cssref/css_selectors.php)

### MDN Docs

- [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [CSS Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)