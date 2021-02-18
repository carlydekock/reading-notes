# Reading 1 - Introductory HTML and JavaScript

## HTML Introduction
How people access the web:
- Browsers: web browsers such as Chrome, Safari, Internet Explorer
- Web servers: special computers that are constantly connected to the internet that host websites
- Devices: desktop computers, laptops, tablets, mobile phones are all being used to access websites
- Screen readers: programs that read the contents of a computer screen to a user, commonly used by people with a visual impairment

How the web works:
1. When you connect to the web, you do so via an Internet Service Provider (ISP). You type a domain name or web adress into your browser.
1. Your computer contacts a network of servers called Domain Name Systems (DNS) servers that act like phone books. They tell your computer the IP address associated with the requested domain name. Every device on the web has a unique IP address. 
1. The unique number the DNS server retrns to your computer allows your broswer to contact the web server that hosts the website you requested.
1. The web server then sends the page you requested back to your web browser.

## HTML Structure
``` <html>
        <head>
            <title>This is the title of the page. This will appear in the title bar.
            </title>
        </head>
        <body>
            <h1>Main Heading for the Body of the page</h1>
            <p>Text will be an introduction to the rest of the page.</p>
            <h2>This will be a sub-heading</h2>
            <p>Another group of text.</p>
        </body>
    </html>
```

## HTML Extra Markup
- DOCTYPE: since there have been several versions of HTML, each web page should begin (before the opening ```<html>``` tag) with a DOCTYPE declaration to tell a browser which version of HTML the page is using.
- Comments: to add a comment to code that doesn't appear in the browser, add the text between these characters ```<!-- comment goes here -->```
- ID attributes: every HTML element can carry the ID attribute, which is used to uniquely identify that element from others on the page, and can be used to reference that specific element later on for CSS styling. ```<p id="namehere">```
- Class attributes: every HTML element can also carry a class attribute, which allows you to uniquely identify groups of elements into classes. An element can belong to multiple classes, they should be separated with a space in the naming. ```<p class="nameofclass"> or <p class="nameofclass nameofclass2">```
- The ```<div>``` element allows you to group a set of elements together in one block-level box. For example, you could use a div element to contain all the elements for a header on your webpage (logo and navigation to subpages).
- The ```<span>``` element acts like an inline equivalent to the div element. Commonly used to control the appearance of the content of the elements in CSS.
- The ```<iframe>``` element is used to include a small window into another page on your page, a map for example. Must include these attributes: src, height, and width.
- The ```<meta>``` element lives inside the head element and containes information about that webpage. This information is not visible to users, but communicates necessary information to search engines. 
- Escape characters: Some characters that are used in and reserved by HTML code (left and right angle brackets for example). To have these types of characters appear on your page, you need to use escape characters. 

## HTML5 Layout
- There are many new HTML5 layout elements to replace use of the ```<div>``` element.
- The point of these new elements is so webpage authors can use them to help describe the structure of the page. 
- The ```<header>``` element can be used for the main header at the top of the page, or for a header of an article or section within the page. The header can be used to contain the site name and main navigation. 
- The ```<footer>``` element can be used for the footer at the bottom of the page, or for the footer of an article or section within the page. This can be used to include copyright information for example. 
- Navigation: the ```<nav>``` element is used to contain the major navigational blocks on the site. 
- Articles: the ```<article>``` element acts like a container for any section of a page that could stand alone. 
- Asides: the ```<asides>``` element has two purposes, depending on whether it is inside an article element or not. 
  - Inside the ```<article>```, the ```<aside>``` element contains information that is related to the article but is not essential to its overall meaning. 
  - Outside the ```<article>```, the ```<aside>``` element acts as a container for content that is related to the entire page. 
- Sections: the ```<section>``` element groups related content together, typically each section has its own heading. 
- Heading groups: the ```<hgroup>``` element is to group together a set of one or more h1-h6 elements so that they are treated as one single heading.
- Figures and captions: the ```<figure>``` element can be used to contain any content that is referenced from the main flow of an article (images, videos, graphs, code samples for example). The figure element should have a ```<figcaption>``` element which provides a text description. 
- Where there is no suitable element to group a set of elements, the ```<div>``` element should still be used. 
- Older browsers that do not know the new HTML elements will automatically treat them as inline elements. You should include a line of CSS which states which new elements should be rendered as block level elements. 

## HTML Process & Design
- Once you've decided what needs to appear on the site, you can organize the information into sections and pages using a site map. 
- Wireframe is a simple sketch of the key information that needs to go on each page of the site, it shows the hierarchy. 
- Keep design elements in mind such as grouping, similarity, visual hierarchy (size, color and style).
- When designing navigation keep these principles in mind: concise, clear, selective, context, interactive, and consistent. 

## JavaScript Introduction
- JavaScript can make websites more interactive, interesting and user-friendly. 
- How JavaScript makes web pages more interactive:
  1. Access content
  1. Modify content
  1. Program rules or instructions the browser can follow
  1. React to events triggered by the user or browser

## The ABC of Programming
- Script: a script is a series of instructions that a computer can follow to achieve a goal. 
  - When writing a script:
    1. Define the goal
    1. Design the script
    1. Code each step
- Three languages used to create web pages:
  1. Content layer (HTML, .html files)
  1. Presentation layer (CSS, .css files)
  1. Behavior layer (JavaScript, .js files)

### Terms
- HTML: HyperText Markup Language
- Domain Name System (DNS): network of servers that act like phone books, telling your computer IP address associated with the requested domain name.
- IP address: unique identifier number for every device on the web. Used to be made up of 12 digits, now being updated to up to 32 characters. 
- Elements: characters that live inside angled brackets in HTML code. HTML uses elements to describe the structure of pages. 
- Tags: elements are usually made up of two tags - an opening and a closing tag. Tags act like containers.
- Attributes: provides additional information about the contents of an element, appear on the opening tag of an element and are made up of two parts - name and a value, separated by an equals sign.
- Global attribute: can be used on any element, the id attribute for example. 
- Block elements: elements that always appear to start on a new line in the browser window (examples: ```<h1>, <p>, <ul>, <li> ```)
- Inline elements: elements that always appear to continue on the same line as neighboring elements (examples: ```<a>, <b>, <em>, <img>```)
- Object: in computer programming, each physical thing in the world can be represented as an object. Each object can have it's own properties, events, methods. 
- Properties: each property has a name and a value, each of these name/value pairs tells you something about each individual instance of the object. 
- Events: programmers choose which events to respond to, an event can be used to trigger a specific section of the code. 
- Method: the code for a method can contain lots of instructions that together represent one task. 


[<==Back>](../README.md)