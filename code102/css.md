# CSS Notes

## What is CSS?
- Allows you to create rules that specify how the content of an element should appear.
- Key to understanding how CSS works is to imagine an invisible box around every HTML element.

## How CSS works
- CSS rule contains two parts: a selector and a declaration
- Selector indicates which element the rule applies to
- Declaration indicates how the elements referred to in the selector should be styled. Declarations have two parts - property and a value
- Property indicates the aspects of the element you want to change
- Values specify the settings you want to use for the chosen properties
- Using external CSS: can use the `<link>` element in an HTML document to tell the browser where to find the CSS file to style the page
- Using internal CSS: can include CSS rules within HTML page by placeing them inside `<style>` element, which is usually in the `<head>` element
- When building a site with more than one page, you should use external CSS style sheet

## How to write CSS rules
- For example: `p {font-family: Arial;}` p is the selector, `{font:family: Arial;}` is the declaration
- Another example: `h1,h2,h3 {font-family: Arial; color:yellow;}` color is the property, and yellow is the value
- CSS selectors: different CSS selectors allow you to target rules to specific elements in HTML document
  - Universal: applies to all elements in document
  - Type: matches element names
  - Class: matches element whose class attribute has a value that matches
  - ID: matches element whose id attribute has value that matches
  - Child: matches element that is direct child of another
  - Descendant: matches element that is descendant of another
  - Adjacent sibling: matches element that is next sibling of another
  - General sibling: matches element that is sibling of another

## How CSS rules apply to HTML pages
- CSS rules cascade, if the last two selectors are identical the latter of the two will take precedence
- If one selector is more specific than others, the more specific rule will take precedence
- You can add !important after any property value to indicate that it should be considered above others

## Color

### How to specify color
There are three common ways to specify your color choices:
  1. RGB values: expresses colors in terms of how much red, green and blue are used to make it up
  1. Hex codes: six digit code to represent color
  1. Color names: 147 predetermined color names recognized by browsers

### Color terminology and contrast
- Foreground color: the `color` property allows you to specify the color of text inside an element
- Hue: is essentially the idea of color
- Saturation: refers to the amount of gray in a color
- Brightness: referes to how much black is in a color
- Contrast: keep contrast in mind when picking foreground and background colors to promote readability
- Opacity (rgba in CSS): value between 0.0 and 1.0 that correlates to percentage opacity

### Background color
- The `background-color` property sets the color of the background for that HTML element or box.
- If you don't specify a color, the background is transparent


[<==Back>](../code102contents.md)

[Back to Home Page](../README.md)