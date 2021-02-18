# Reading 7 - Object-Oriented Programming, HTML Tables

## Domain Modeling
- **Domain modeling** is the process of creating a conceptual model in code for a specific problem
- **Object-oriented model** is an entity that stores data in properties and encapsulates behaviors in methods
- Can be a tool for communication within and between technical and business teams
- Object-oriented programming in JS fundamentals:
  1. The ```new``` keyword instantiates (creates) an object
  1. The constructor function initializes properties inside that object using the ```this``` variable
  1. The object is stored in a variable for later use

### Tips for building your own domain model:
- When modeling a single entity that will have many instances, build self-contained objects with the same attributes and behaviors
- Model its attributes with constructor function that defines and initializes properties
- Model its behavior with small methods that focus on one job
- Create instances using the ```new``` keyword followed by call to a constructor function
- Store new object in a variable so you can access its properties and methods from outside
- Use the ```this``` variable within methods so you can access the objects's properties and methods from inside

## Tables (HTML book, pg. 126-145)
- Table represents information in a grid format (like a spreadsheet)
- Basic table structure:
  - ```<table>``` to create the table
  - ```<tr>``` for table rows
  - ```<td>``` table data
  - ```<th>``` table heading (can use scope attribute to indicate whether for a column or row)
- Additional attributes:
  - ```colspan``` to indicate how many columns a cell should run across
  - ```rowspan``` to indicate how many rows a cell should span down the table
- For long tables, use ```<thead>```, ```<tbody>``` and ```<tfoot>```

## Functions, Methods, and Objects (JS book, pg. 106-144)
- Creating an object - constructor notation:
  - The new keyword and the object constructor create a blank object, then add properties and methods (for example: ```var hotel = new Object()```)
- To update the values of a property, use dot notation or square brackets. They work on objects created using literal or constructor notation. 
- To delete a property, use the delete keyword.
- Creating multiple objects - constructor notation:
  - Object constructors can use a function as a template for creating objects
  - First, create the template with the object's properties and method
- Name of a constructor funtion usually begins with a capital letter
- Create instances of the object using the constructor function. The new keyword followed by a call to the function creates a new object. Properties of each object are given as argments to the function
- ```this``` commonly used inside functions and objects, where the function is declared alters what this means

### Storing Data
- In JavaScript, data is represented using name/value pairs
- Can use an array or object to group a set of related values
- In arrays and objects the name is also known as a key
- Variable: has just one key (the variable name) and one value
- Arrays: can store multiple pieces of info, each value in an array is a key/value pair (key is index number, value from comma-separated list)
- Individual objects: store sets of name/value pairs
- Multiple objects: good when you have lots of objects with similar functionality

### Objects
- Can combine arrays and objects to create complex data structures: arrays store series of objects in order, objects can hold arrays as values of their properties
- Built in objects: help you get a wide range of information such as width, length, content of heading, etc
  - Browser Object Model: contains objects that represent the current browser window or tab
  - Document Object Model
  - Global JavaScript objects
    - String object: each character in string is automatically given a number, called an index number
    - Number object: isNan(), toFixed(), toPrecision(), toExponential()
    - Math objects: Math.PI(), Math.round(), Math.sqrt(n), Math.ceil(), Math.floor(), Math.random()
    - Date and time objects: to work with dates, create an instance of the Date object

[<==Back>](../README.md)