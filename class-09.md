# Reading 9 - Forms and JavaScript Events

## Forms (HTML book, pg 144-175)
- Forms allow users to search, as well as perform other functions
- Form controls:
  - Adding text: text input, password input, text area
  - Making choices: radio button, checkboxes, drop down boxes
  - Submitting forms: submit buttons, image buttons
  - Uploading files
- How forms work:
  1. User fills in info and presses buttom
  1. Name of each form control sent to the server along with value input or selected
  1. Server processes the information, may also store the information in a database
  1. Server creates a new page to send back to the browser
- Form structure: ```<form>``` element, with ```action``` and ```method``` attributes
- ```<input>``` element is used to create several different form controls, type/name/maxlength attributes
- Password input: ```<input type="password">``` along with name/size/maxlength attributes
- Text area: ```<textarea>``` used to create multi line text input
- Radio button: allows users to pkck just one of a number of options, ```<input type="radio">```
- Checkbox: allows users to select and unselect one or more options to answer a question, ```<input type="checkbox">```
- Drop down list: also known as a select box
  - ```<select>``` element used to create a drop down list box
  - contains two more more ```<option>``` elements
- Multiple select box: ```<select>``` with ```multiple``` attribute
- File input: ```<input type="file">```
- Submit button: ```<input type="submit">```
- Image button: ```<input type="image">```
- Date input: ```<input type="date">```
- Email and URL input: ```<input type="email">``` or ```<input type="url">```
- Search input: ```<input type="search">```

## Lists, Tables and Forms (HTML book, pg 330-357)
- Bullet point styles: ```list-style-type```
- Positioning the marker: ```list-style-position```
- List shorthand: ```list-style```
- Table properties:
  - width
  - padding
  - text-transform
  - letter-spacing, font-size
  - border-top, border-bottom
  - text-align
  - background-color
  - :hover
- Styling text inputs: font-size, color, background-color, border, border-radius, :focus, :hover, background-image
- Styling submit buttons: color, text-shadow, border-bottom, background-color, :hover
- Cursor styles: ```cursor``` property can have multiple different values/styles

## Events (JS book, pg 243-292)
- When an event has accured it is described as having fired or been raised
- Events are said to trigger a function or script
- Different event types:
  - UI events: load, unload, error, resize, scroll
  - Keyboard events: keydown, keyup, keypress
  - Mouse events: click, dblclick, mousedown, mouseup, mousemove, mouseover, mouseout
  - Focus events: focus/focusin, blur/focusout
  - Form events: input, change, submit, reset, cut, copy, paste, select
  - Mutation events: occur when DOM structure changed by a script
- How events trigger JavaScript code:
  1. Select the element node(s) you want the script to respond to
  1. Indicate which event on the selected node(s) will trigger the response
  1. State the code you want to run when the event occurs
- Three ways to bind an event to an element
  1. HTML event handlers (bad practice)
  1. Traditional DOM event handlers
  1. DOM level 2 event listeners
- Event flow:
  - Event bubbling: the event starts at the most specific node and flows outwards to the least specific node
  - Event capturing: event starts at the least specific node and flows inwards to the most specific one
- Why flow matters? The flow of events matters when yourcode has event handlers on an element and one of its ancestor or descendant elements
- When an event occurs, the event object tells you information about the event and the element it happened upon

[<==Back>](README.md)