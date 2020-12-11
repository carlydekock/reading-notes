# Reading 10 - JavaScript Error Handling & Debugging

## Execution Contexts
- Global context: code that is in the script, but not in a function. There is only one global context in any page.
- Function context: code that is being run within a function, each fnction has its own function context
- Global scope: variable is declared outside the function, can be used anywhere because it has global scope
- Function-level scope: when a variable is declared within a function, it can only be used within that function

## The Stack
- The JavaScript interpreter processes one line of code at a time.
- When a statement needs data from another function, it stacks (or piles) the new function on top of the current task

## Error Objects
- When an error object is called, it will contain the following properties:
  - name
  - message
  - fileNumber
  - lineNumber
- Seven types of built-in error objects:
  1. Error: generic error
  1. SyntaxError: syntax has not been followed
  1. ReferenceError: tried to reference variable that is not declared/within scope
  1. TypeError: unexpected data type that cannot be coerced
  1. RangeError: numbers not in acceptable range
  1. URIError: encodeURI(), decodeURI(), and similar methods used incorrectly
  1. EvalError: eval() function used incorrectly

  ## How to Deal with Errors
  1. Debug the script to fix erros
  2. Handle errors gracefully using try, catch, throw, and finally

  ## Debugging Workflow
  - Where is the problem?
  - Check how far the script is running
  - Use breakpoints where things are going wrong
  - When you have set breakpoints, see if the variables around them have the values you would expect them to
  - Break down/ break out parts of the code to test functionality
  - Check the number of parameters for a function, or the number of items in an array

  ### Debugging Tips:
  - Try aother browser
  - Add numbers to the console
  - Strip it back to the minimum
  - Explain the code to someone else
  - Search for online resources that might address the issue
  - Code playgrounds (sites to paste code)
  - Validation tools online

  ## Browser Dev Tools / JavScript Console
  - The JavaScript console will tell you where there is a problem with a script, where to look for the problem, and what kind of issue it seems to be
  - Console in Chrome: shows when there is an error, and displays the line where it became a problem for the interpreter
  - Using the console in Chrome to type code can also be a good resource
  - Using console.log() to write to the console
  - Using breakpoints to pause execution of a script, you can then check the values stored in variables at that point in time
  - Stepping through code function in Chrome
  - Can also set conditional breakpoints
  - Debugger keyword: creates breakpoint in code

  ## Handling Exceptions
  - Try: first specify the code that you think might throw an exception within the try block. Try clause should always have either a catch, finally, or both.
  - Catch: if try code block throws an exception, catch steps in with an alternative set of code. Has one parameter, the error object.
  - Finally: contents of the finally code block will run either way, whether the try block succeeded or failed. 

[<==Back>](README.md)