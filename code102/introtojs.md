# Intro to JavaScript

## The Basics
- Three languages used to create web pages:
  1. HTML: the content layer
  1. CSS: the presentation layer
  1. JavaScript: the behavior layer
- JavaScript is written in plain text just like HTML and CSS
- JavaScript files have a .js extension, and should be kept in a js or javascript folder
- Use the HTML element `<script>` to tell the browswer it is coming across a script
- The src attribute tells where the JavaScript file is stored
- JavaScript is case sensitive

## Terms
`document.write('Good afternoon!');`
- This piece of code is called "calling a method of an object.
- Document is the **object**. All web browsers implement this object.
- The document object has several methods and properties, knows as **members** of that object.
- You can access the members of an object using a dot between the object name and the member you want to access. This dot is the **member operator**.
- The remainder of the line, `write.('Good afternoon!');` is called the **method**.
- The write () method of the object (document) allows new content to be written into the page where the script element sits.
- `('Good afternoon!')` is the **parameter**.
- Each piece of information is called a parameter of the method. The write method needs to know what to write into the page.

## The Language: Syntax and Grammar
- A script is a series of instructions that a computer can follow one by one. 
- Each individual instruction or step is known as a statement.
- Statements should each start on a new line and end with a semicolon.
- The semicolon tells the JavaScript interpreter when a step is over, and indicates for it to move on to the next.
- Statements surrounded by curly braces are known as **code blocks**. Closing curly brace is not followed by a semicolon.
- Include comments to explain what your code does. Use // for single line comments, or /* for multi line comments.
- Scripts need to temporarily store bits of information, it can store this data in **variables**.

## Variables
- Before using a variable, you need to "declare" the variable by giving it a name. For example, `var quantity;`, var is the variable keyword and the variable name we are declaring is quantity. 
- If variable names are more than one word, they are written using camelCase, the first word is all lowercase and any subsequent words have their first letter capitalized.
- Assigning a value to the variable, `quantity = 3;`. The = sign is used as the assignment operator, and in this example the 3 is the variable value at this time.
- Until you have assigned a value to a variable, the value is **undefined**.
- Where a variable is declared can have an effect upon whether the rest of the script can use it. This is called the **scope** of a variable.
- Once you have assigned a value to a variable, you can then change what is stored in the variable later in the same script.

## Data Types
- Numeric data type: handles numbers (whole numbers, negative numbers, and decimals) but do not include a comma in the numbers
- String data type: consists of letters and other characters, enclosed in quotes (' or ")
- Boolean data type: one of two values - true or false

## Three Variations of How to Declare Variables
1. Variables are declared and values assigned in the same statement
1. Three variables are declared on the same line, then values assigned to each
1. Two variables are declared and assigned values on the same line, then one is declared and assigned a value on the next line


[<==Back>](README.md)