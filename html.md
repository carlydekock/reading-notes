# Read 04: Structure web pages with HTML

## Process and Design

### Questions to consider
- Who is the site for? Consider your target audience, the demographics of a sample of your target audience.
  - Individuals or companies?
  - Invent some fictional visitors to your site, keep them in mind when considering design decisions.
- Why are people visiting your site?
  - Underlying motivations of visitors
  - Goals of visitors when they visit
- What information people are looking for
  - Prioritize levels of information they'll be looking for
  - Consider the most important features you are offering
- How often will people visit your site

### Site Maps
Once you know what needs to appear on your site, you can organize information into sections or pages.

### Wireframes
Simple sketch of the key information that needs to go on each page of the site. Helpful to show the hierarchy of information.

### Using good design to get your message across
- Content
- Prioritizing
- Organizing
- Visual Hierarchy: order in which your eyes perceive what they see. Use contrast to create, consider size, color, and style.
- Grouping: consider proximity, closure, continuance, white space, color, and borders
- Similarity: consistency of style, headings

### Site Navigation
Follow these principles when designing site navigation:
- Concise
- Clear
- Selective
- Context
- Interative
- Consistent

## Structure Overview
- HTML pages are text documents.
- HTML uses elements to describe the structure of the page.
- Each element has an opening and closing tag. Opening tag denotes start of the content, closing tag denotes the end.
- Opening tags can carry attributes. An attribute provides additional information about the contents of an element. 
- Attributes require a name and a value, separated by an equals sign. The specified value should be placed in quotes. 

## HTML5 Layout
- Building blocks: block-level (starts on a new line) or inline (flow in between surrounding text)
- Containing elements: A box may be nested inside other block level elements, containing element is always the direct parent of that element. Common to do this with a `<div>` element.
- Positioning schemes to control layout of the page:
  1. Normal flow: every block level element appears on a new line (position:static)
  1. Relative positioning: moves from normal flow or normal position, shifting top/right/bottom/left (position:relative)
  1. Absolute positioning: positions the element in relation to its containing element. Heading is in top right corner, and paragraphs start at top of the screen. (position:absolute)
  1. Fixed positioning: positions element in relation to browser window (position:fixed)
  1. Floating elements: allows you to position to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow. (float property)
- Overlapping elements: the z-index property allows you to control which elements sit on top
- Creating columns on a webpage: Using the `<div>` command, along with width, float and margin, you can create columns side by side
- Due to variation in size, web designers often create pages of around 960-1000 pixels wide
- Fixed width versus liquid width: fixed width does not change size when a user changes the size of a browser window while liquid layouts do change size
- Linking CSS style sheets to a page: Using @import or separate `<link>` elements for each style sheet

## Extra Markup
- Comments in HTML can be entered like this: `<!-- comment here -->`
- id attributes can be used to identify certain unique elements on a page
- class attribute can be used to identify several elements together
- Block level elements will always appear to start on a new line (h1, p, u1, and li for example)
- Inline elements will appear to continue on the same line (a, b, em, and img for example)
- Use `<div>` to group elements together
- The `<span>` element acts like an inline div element
- You can add a little window from another web page onto your page (map for example) using `<iframe>`
- The `<meta>` element lives inside the head and gives info about the page that is not displayed on the page itself
- Escape characters are used to display characters in the broswer that are reserved by HTML code (& or " for example)