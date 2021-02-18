# Problem Domain, Objects, and the DOM

## Understanding the Problem Domain
- Understanding the problem domain is the most critical piece of writing code
- Make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem
- Take a part of the problem and fully understand that part before expanding the problem domain
- Make sure you understand the problem inside and out before you try and solve it with code

## Object Literals (JS book, pg 100-105)
- Object: objects group together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on new names.
  - Variables become properties
  - Functions become methods (tasks that are associated with the object)
  - Properties and methods have a name and a value
  - In an object, that name is called a key
  - Value of a property can be a string, number, Boolean, array or another object
  - Value of a method is always a function
- Name/value pairs:
  - HTML uses attribute names and values
  - CSS uses property names and values
  - In JavaScript:
    - Variables have a name and you can assign them a value (string, number or Boolean)
    - Arrays have a name and a group of values (each item in array is a name/value pair)
    - Named functions have a name and value that is a set of statements to run
    - Objects consist of a set of name/value pairs (names are referred to as "keys")

### Creating an object (literal notation):
- Object is the curly braces and their contents
- Object is stored in a variable
- Separate each key from its value using a colon
- Separate each property and method with a comma (but not after the last value)
- Example of an object (from the textbook pages 101-102):
``` 
  var hotel = {
    name: 'Quay',
    rooms: 40,
    booked: 25,
    checkAvailability: function() {
      returnthis.room - this.booked;
    }
    }
```
- In the example - name, rooms and booked are the properties, and checkAvailability is the method.
- "this" keyword in the method is used to indicate that it is using the rooms and booked properties of this object
- When setting properties, treat the values like you would for variables:
  - strings live in quotes
  - arrays live in brackets

### Accessing an object
- You can access the properties or methods using **dot notation**:
  - Use the name of the object followed by a period, then the name of the property or method you want to use
  - For example:
  ```
  var hotelName = hotel.name;
  var roomsFree = hotel.checkAvailability();
  ```
  - hotel is the object
  - name and checkAvailability() are the property/method names
  - (.) is the member operator
- You can access properties using **square brackets**:
  - This time the object is followed by square brackets, with the property or method inside them
  - For example:
  ```
  var hotelName = hotel['name'];
  var roomsFree = hotel['checkAvailability']();
  ```
  - This notation is commonly used when:
    1. The name of the property or method containes special characters
    1. The name of the property is a number
    1. A variable is being used in place of the property name
  
## Document Object Model (JS book, pg. 183-242)
- The **Document Object Model (DOM)** specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents
- DOM is not a part of HTML or of JavaScript
- DOM covers two primary areas:
  1. Making a model of the HTML page
    - DOM specifies the way in wich broswer should structure this model using a **DOM tree**
    - DOM tree is made of objects, each object represents a different part of the page
  1. Accessing and changing the HTML page
    - DOM is sometimes called **Application Programming Interface (API)**, APIs let programs and scripts talk to each other
- DOM tree consists of four different types of **nodes**:
  1. Document node: represents the entire page, starting point for all visits to the DOM tree
  1. Element nodes: to access the DOM tree you start by looking for elements. Once you find the element you want, then you can access its text and attribute nodes if you want to
  1. Attribute nodes: opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree. Attribute nodes are not children of the element that carries them, they are part of that element
  1. Text nodes: once you have accessed an element node, you can then reach the text within that element, which is stored in its own text node. Text nodes cannot have children.

### Working with the DOM Tree
- Step 1: Access the elements
  - Note: the terms elements and element nodes are used interchangeably
  - Select and individual element node: 
    - ```getElementById()```uses the vaue of an element's id attribute
    - ```querySelector()```uses CSS selector, returns first matching element
    - Select individual elements by traversing from one element to another within the DOM tree
  - Select multiple elements (nodelists): 
    - ```getElementsByClassName()```selects all elements that have specific value or their class attribute
    - ```getElementsByTagName()```selects all elements that have specified tag name
    - ```querySelectorAll()```uses CSS selector to select all matching elements
  - Traversing between element nodes: 
    - ```parentNode```selects parent of current
    - ```previousSibling/nextSibling```selects previous or next sibling from DOM tree
    - ```firstChild/lastChild```selects first or last child of the current element
- Step 2: Work with those elements
  - Access/update text nodes: ```nodeValue```
  - Work with HTML content: 
    - ```innerHTML```allows access to child elements and text content
    - ```textContent``` allows access to just text content
    - Several methods let you create new nodes, add nodes to a tree and remove from a tree: 
      - ```createElement()```
      - ```createTextNode()```
      - ```appendChild()/removeChild()```
  - Access or update attribute values: 
    - ```className/id```lets you get or update the value of the class and id attributes
    - ```hasAttribute()```checks if exists
    - ```getAttribute()```gets its value
    - ```setAttribute```updates the value
    - ```removeAttribute()```removes an attribute
- Caching DOM queries: methods that find elements in the DOM tree are called DOM queries, when you need an element repeatedly, you can use a variable to store the result of the query
- Storing elements in variables is really storing the location of the elements within the DOM tree in a variable
- DOM queries may return one elemeent, or they made return a **NodeList** (collection of nodes)
  - Each node is given an index number
  - Order in which the elements are stored in a NodeList is the same order that they appeared in the HTML page
- Look like arrays and are numbered like arrays but they are not arrays; they are a type of object called a **collection** (can use ```length``` to tell how many items, and ```item()``` to return a specific node when given an index number)
- Live NodeList: NodeList is updated when script updates the page
- Static NodeList: when script updates, NodeList not updated to reflect the changes made by the script
- Selecting an element from a NodeList:
  - The ```item()``` method: specify the index number of the element you want as a parameter of the method
  - Array syntax (preferred due to speed): access individual nodes using [] syntax, specify the index of the element you want

### Adding or Removing HTML content
Two different approaches:
  1. The ```innerHTML``` property
  1. DOM manipulation

#### Inner HTML property: 
- Note: security risks associated with this
- Approach: can be used on any element node. Used to both retrieve and replace content. To update, new content is provided as a string
- Adding content: store new content, select the element whose content you want to replace, set the element's innerHTML property to be the new string
- Removing content: set the innerHTML to an empty string, to remove one element you have to provide the entire fragment minus that element

#### DOM Manipulation
- Note: safer, but requires more codes and can be slower
- Approach: set of DOM methods that allow you to create element and text nodes, then attach or remove
- Adding content: use a DOM method to create new content one node at a time and store it in a variable, then another DOM method is used to attach it to the right place in the DOM tree
- Removing content: can remove any element using a single method

[<==Back>](../README.md)
