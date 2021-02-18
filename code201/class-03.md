# Reading 3 - HTML Lists, Control Flow with JS, and the CSS Box Model

## Lists (HTML book, pg. 62-73)
- Three list types in HTML:
  1. Ordered lists: ```<ol>```
  1. Unordered lists: ```<ul>```
  1. Definition lists: ```<dl>``` used with ```<dt>``` for term being defined and ```<dd>``` for the definition.
- Lists can be nested.

## Boxes (HTML book, pg. 300-329)
- By default a box is sized just big enough to hold its contents. Can set specified height and width properties. 
- Most popular ways to specify the size of the box are to use pixels, percentages, or ems
- Limiting width using min-width and max-width
- Limiting height with min-height and max-height
- ```overflow``` tells the browser what to do if the content within the box is larger than the box itself, and can have two values - ```hidden``` or ```scroll```
- Each box has three adjustments that can be made:
  1. Border: separates the edge of one box from another
     - ```border-width```: can be specified either in pixels or thin/medium/thick
     - ```border-style```: can take values of solid, dotted, dashed, double, groove, ridge, inset, outset, hidden/none
     - ```border-color```
     - ```border``` shorthand command to specify width, style and color in one property
  1. Margin: sits outside the border
  1. Padding: space between the boarder of a box and any content conatined within it
- The ```display``` property allows you to turn inline element into block-level element or vice versa, or hide an element from the page. It can take values of: inline, block, inline-block, and none. 
- Hiding boxes can be done using the ```visibility``` property, which can take two values - hidden or invisible.
- CSS3 properties:
  - ```border-image```
  - ```box-shadow```
  - ```border-radius```

## Review from Reading 02 - Ch. 2 Basic JavaScript Instructions (JS book, pg. 70-73)
- Array: special type of variable that can store a list of values
- Creating an array:
  - Create an array just like you would any other variable: ```var arrayName```
  - Values are assigned inside square brackets, seprated by commas: ```arrayName = ['first, 'second', 'third']```
- Accessing values in an array:
  - Think of values in an array like an ordered list, starting at zero though not one.
  - Each item in an array is automatically given a number called an index.
  - To retrieve an item, the array name is specified along with the index number in square brackets.
- Each array has a property called lenth, which holds the nubmer of items in the array.
- You can change an array value by selecting it and assigning it a new value. 

## Decisions and Loops (JS book, pg. 162-182)
- Switch statement: starts with a variable called the switch value, each case indicates a possible value for the variable and the code to run if it matches
  - You have a default option that is run if none of the cases match
  - If a match is found, that code is run and then a break statement stops the rest from running
- Type coercion: JavaScript converts data types behind the scenes to complete the operation if you use something it did not expect
- Truthy: values are treated as if they are true
- Falsy: values are treated as if they are false
- Unary operator: returns a result with just one operand
- Loops: check a condition, if it returns true, a code block will run. Then the condition will be checked again and if true will run again. Repeats until returns false. There are three types of loops:
  - For: used to run code a specific number of times
    - Loop counter --> initialization, condition, update
  - While: used when don't know how many times the code should run
  - Do While: similar to the while loop, one difference is it will always run the statements at least once even if false
  

[<==>Back](../README.md)