# Reading 8 - CSS Layout

## Key concepts
- Block level versus inline elements
- Containing element (direct parent of elements it contains)

## CSS positioning schemes
- Normal flow: every block level element on a new line
  - ```position:static```
- Relative positioning: moves element from normal flow, shifting top/right/bottom/left
  - ```position:relative```
- Absolute positioning: positions in relation to containing element, moves as users scroll up and down the page
  - ```position:absolute```
- Fixed positioning: form of absolute positioning that positions in relation to browser window
  - ```position:fixed```
- Floating elements: take out of normal flow and position to the left/right of containing box
  - ```float```
- z-index: used when you want to control the which element sits on top, also referred to as stacking context (think of it as bring to front/send to back)
- Multi column layouts: achieved with a ```<div>``` element to represent each column, and three CSS properties (width, float, margin) to position the columns next to each other

## Other concepts/notes
- Screen sizes: design needs to be able to work on a range of different sized screnes
- Page sizes: since sizes vary so much, web designers often try to create pages of around 960-1000px wide
- Fixed width layout: does not change size as the user increases or decreases the size of browser window
- Liquid layout: stretches and contracts as the user increases or decreases size of browser window (usually use percentages)
- Layout grid: a good tool to visualize/plan the placement and arrangement of content on the page

[<==Back>](../README.md)