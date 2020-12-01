# Reading 2 - Basics of HTML, CSS & JS

## Text (Duckett HTML book, pg. 40-61)
- Structural markup: elements that you use to describe both headings and paragraphs
- Semantic markup: provides extra information, such as where emphasis is placed, quotations, etc. Some examples:
  - ```<strong>```: indicates that the content has strong importance
  - ```<em>```: indicates emphasis that subtly changes meaning
  - ```<blockquote>```: used for longer quotations
  - ```<q>```: used for shorter quotes that sit within paragraph
  - ```<abbr>```: used if you have an abbreviation or acronym
  - ```<cite>```: can indicate where the citation is from
  - ```<dfn>```: indicate the defining instance of a new term
  - ```<address>```: used to contain contact details for the author of the page
  - ```<ins> or <del>```: can be used to show content that is inserted or deleted into a document
  - ```<s>```: indicates something that is no longer relevant, but shouldn't be deleted
- Headings: h1-h6, browsers display these at different sizes (h1 is largest, h6 is smallest)
- Bold: enclose bold text in ```<b>```
- Italics: enclose text in italics in ```<i>```
- Superscript: enclose text in ```<sup>```
- Subscript: enclose text in ```<sub>```
- Horizontal line break: use ```<br />``` to add a line break
- Horizontal rule: use ```<hr />``` to create a line between themes or sections on a page

## Introducing CSS (Duckett HTML book, pg. 226-245)
- CSS allows you to create rules that specify how the content of an element should appear. 
- Imagine there is an invisible box around every HTML element. CSS allows you to create rules that control the way that each individual box and its contents are presented.
- CSS works by associating style rules with HTML elements.
- CSS rule:
  - Contains two parts: 
    1. Selector: indicates which element rule applies to
    1. Declaration: indicates how the element referred to should be styled
       - Declarations have two parts:
         1. Property: indicates aspects of the element you want to change
         1. Values: specifies the settings you want to use for the chosen property
  - For example: ```p {font-family: Arial;}``` --> ```p``` is the selector, ```font-family: Arial;``` is the declaration
  - Another example: ```h1, h2, h3 {font-family:Arial; color: yellow'}``` --> ```font-family``` and ```color``` are properties, ```Arial;``` and ```yellow;``` are values.
- CSS can be used externally or internally.
  - External: use the ```<link>``` element, which also needs href, type and rel specifications.
  - Internal: use the ```<style>``` element, which should also have the type attribute (should be text/css).
- CSS selectors: there are many types of selectors that allow you to target rules to specific elements in an HTML document:
  - Universal
  - Type
  - Class
  - ID
  - Child
  - Descendant
  - Adjacent sibling
  - General sibling
- Things to keep in mind:
  - CSS rules cascade, if two selectors are identical, the latter of the two will take precedence
  - If one is more specific than the other, the more specific rule will take precedence
  - The value of a property will be inherited by child elements

## Basic JavaScript instructions (Duckett JS book, pg. 53-84)
- Script is a series of instructions that the computer can follow one by one. Each individual instruction or step is a statement. Statement should end with a semicolon.
- Should write comments to explain what the code is doing.
- Variable: the script will have to temporarily store bits of information needed to do it's job, it can store this data as variables. 
  - More info on variables:
    - Before you can use a variable, you need to announce that you want to use it. To do this, you need to create the variable and give it a name or *declare* the variable. For example: ```var quantity;``` the var is the variable keyword and quantity is the variable we are declaring.
    - Once you've created a variable, you can tell it what information to store, this is *assigning a value* to the variable. For example: ```quantity = 3;``` the = is the assignment operator.
- Data types: numeric, string, and boolean
- Once you have assigned a value to a variable, you can then change what is stored in the variable later in the same script. 
- Rules for naming variables:
  1. Name must begin with a letter, $ or _. **Cannot* start with a number. 
  1. Name can contain letters, numbers, $ or _. **Cannot* use a - or period. 
  1. Cannot use keywords or reserved words.
  1. Variables are case sensitive.
  1. Use a name that describes the type of information that the variable stores. 
  1. If the variable is more than one word, use camel case (firstName or lastName for example).
- Arrays: special type of variable that doesn't just store one value, it stores a list of values. Values in an array do not need to be the same data type. When to use an array:
  - When working with a list or set of values that are related to each other
  - When you do not know how many items a list will contain
  - To construct an array:
    - Construct an array using array literal (preferred) or array constructor.
    - Array literal: values are assigned to the array inside a pair of square brackets and each value is separated by a comma.
    - Array constructor: values are specified in parenthesis, each value separated by a comma.
  - Values in an array are accessed as if they are in a numbered list. The numbering of the list starts at zero (not one).
- Expressions: evaluates or results in a single value. Two types of expressions:
  1. Expressions that assign a value to a variable (```var color = 'blue';```)
  1. Expressions that use two or more values to return a single value (```var area = 3 * 2;```)
- Expressions rely on operators. Types of operators: 
  - Assignment (=)
  - Arithmetic (+,-,*,/,++,--,%)
  - String
  - Comparison (```<``` or ```>```, returns true or false)
  - Logical (combine expressions and return true or false)

## Decisions and Loops (Duckett JS book, pg. 145-162)
- Scripts often behave differently depending on how the user interacts with the web page and/or browser window. To determine which path to take, programmers often rely upon three concepts:
  - Evaluations: you can analyze values in your scripts to determine whether or not they match expected results
  - Decisions: using the results of evaluations, you can decide which path your script should go down
  - Loops: want to perform the same set of steps repeatedly
- Comparison operators: evaluate a situation by comparing one value in the script to what you expect it might be, the result will be a boolean true or false. Types of operators:
  - Equal to: ```==```
  - Strict equal to: ```===```
  - Not equal: ```!=```
  - Strict not equal to: ```!==```
  - Greater than: ```>```
  - Less than: ```<```
  - Greater than or equal to: ```>=```
  - Less than or equal to: ```<=```
- In any condition there is usually one operator (options above) and two operands (values or variables). Expressions are often enclosed in parenthesis. For example: ```(score >= pass)``` score and pass are operands, and >= is the operator. 
- An operand does not have to be a single value or variable name, it can be an expression because each expression evaluates into a single value. 
- Logical operators: usually return a single value of true or false, allow you to compare the results of more than one comparison operator. Types of logical operators:
  - Logical and: ```&&```
  - Logical or: ```||```
  - Logical not: ```!```
- If statements: evaluates or checks a condition, if the condition is true, any statements in the subsequent code block are exectued.
- If else statements: if else checks a condition, if it resolves to true the first code block is executed, if it resolves to false the second code block is run instead.

## Notes on Git Commit Messaging
- A well crafted git commit message is the best way to communicate context about a change, which can be very beneficial in the future. 
- Rules of a great Git commit message:
  1. Seprate subject from body with a blank line
  1. Limit the subject line to 50 characters
  1. Capitalize the subject line
  1. Do not end the subject line with a period
  1. Use the imperitive mood in the subject mind
  1. Wrap the body at 72 characters
  1. Use the body to explain what and why versus how


[<==Back>](README.md)