# Reading 12 - Chart.js, Canvas

## Chart.js API
- Chart.js is a JavaScript plugin that uses HTML5's canvas element to draw the graph onto the page
- Can be used for bar charts, line charts, pie charts, and more

## Chart.js docs
- Creating a chart: include a script in your page along with a single ```<canvas>``` node to enter the chart

## Canvas API

### Basic usage
- ```<canvas>``` element has only two attributes, width and height
- Always a good idea to supply it with an id
- Can be styled like any normal image (margin, border, background)
- ```<canvas>``` element differs from an ```<img>``` tag in that it is easy to define fallback content to be displayed in older browsers. Just insert alternate content inside the element.
- Requires a closing tag ```</canvas>```
- The ```<canvas>``` creates a fixed-size drawing surface that exposes one or more rendering contexts which are used to create and manipulate content shown
- To display something, a script first needs to access the rendering context and draw on it
- ```<canvas>``` element has one method called ```getContext()```, used to obtain the rendering context and its drawing functions. Takes one parameter, the type of context ("2d" for example)

### Drawing shapes with canvas
- Canvas grid or coordinate space: normally 1 unit in the grid corresponds to 1 pixel on the canvas
- ```<canvas>``` only supports two shapes: rectangles and paths (lists of points connected by lines)
- Drawing a rectangle:
  - ```fillRect(x, y, width, height)```: draws a filled rectangle
  - ```strokeRect(x, y, width, height)```: draws a rectangle outline
  - ```clearRect(x, y, width, height)```: draws a transparent rectangle
  - ```rect(x, y, width, height)```: draws a rectange whose top-left corner is specified by (x,y)
- Drawing paths:
  - Takes a few extra steps:
    1. First, you create the path
    1. Then you use drawing commands to draw into the path
    1. Once the path has been created, you can stroke or fill the path to render it
  - ```beginPath()```: creates a new path
  - ```choosePath()```: adds a straight line to the path, going to the start of the current sub-path
  - ```stroke()```: draws the shape by stroking its outline
  - ```fill()```: draws a solid shape by filling the path's content area
- Moving the pen: ```moveTo(x, y)``` moves the pen to the coordinates specified
- For drawing straight lines: ```lineTo(x, y)``` draws a line from the current drawing position to the position specified by x and y
- Drawing arcs:
  - ```arc(x, y, radius, startAngle, endAngle, anticlockwise)```: draws an arc centered at (x,y) with radius r starting at startAngle and ending at endAngle going in given direction by anticlockwise (defaulting to clockwise)
  - ```arcTo(x1, y1, x2, y2, radius)```: draws an arc with the given control points and radius, connected to the previous point by a straight line
- Bezier and quadratic curves (generally used to draw complex organic shapes)
  - ```quadraticCurveTo(cp1x, cp1y, x, y)```
  - ```bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)```
  - A quadratic Bezier curve has a start and an end point and just one control point
- The ```Path2D()``` constructor returns a newly instantiated Path2D object

### Applying styles and colors
- Colors: two important properties to use ```fillStyle``` and ```strokeStyle```
- Transparency: can be done by setting ```globalAlpha``` property or by assigning a semi-transparent color to the stroke and/or fill style
- Can use ```rgba()``` to set fill and stroke style individually
- Line styles:
  - ```lineWidth = value```: sets the width of lines drawn in the future
  - ```lineCap = type```: sets appearnce of the ends of lines
  - ```lineJoin = type```: sets the appearance of the "corners" where lines meet
  - ```miterLimit = value```: establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes
  - ```getLineDash()```: returns the current dash line pattern array containing an even number of non-negative numbers
  - ```setLineDash(segments)```: sets the current line dash pattern
  - ```lineDashOffset = value```: specifies where to start a dash array on a line
- Using gradients: 
  - ```createLinearGradient(x1, y1, x2, y2)```: creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2)
  - ```createRadialGradient(x1, y1, r1, x2, y2, r2)```: creates a radial gradient, parameters represent two circles
- Patterns: ```createPattern(image, type)``` creates and returns a new canvas pattern object
  - Type specifies how to use the image in order to create the patter, and can be one of these values: repeat, repeat-x, repeat-y, no-repeat
- Shadows: 
  - ```shadowOffsetX = float```: indicates horizontal distance the shadow should extend from object
  - ```shadowOffsetY = float```: indicates vertical distance the shadow should extend from object
  - ```shadowBlur = float```: indicates the size of the blurring effect
  - ```shadowColor = color```: standard CSS color value indicating color of the shadow effect

### Drawing text
- Two methods to render text:
  1. ```fillText(text, x, y [, maxWidth])```: fills a given text at the given (x,y) position
  1. ```strokeText(text, x, y [, maxWidth])```: strokes a given text at the given (x,y) position
- Styling text:
  - ```font = value```: current text style being used whe drawing text
  - ```textAlign = value```: text alignment setting, possible values are start, end, left, right, or center
  - ```textBaseline = value```: baseline alignment setting, possible values are top, hanging, middle, alphabetic, ideographic, bottom
  - ```direction = value```: directionality, possible values are ltr, rtl, inherit
  - ```measureText()``` returns object containing width in pixels that the specified text will be when drawn in the current text style

[<==Back>](README.md)