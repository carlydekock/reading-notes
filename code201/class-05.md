# Reading 5 - Images, Color, Text

## Images (HTML & CSS book, pg. 94-125)
- Adding images: ```<img>``` element (no closing tag). Must carry these attributes: ```src```, ```alt```, ```title```
- Height and width of images: also will often use ```height``` and ```width``` in the img element to specify size
- Where to place an image:
  1. Before a paragraph
  1. Inside the start of a paragraph
  1. In the middle of a paragraph
- Rules for creating images:
  1. Save images in the right format (jpeg, gif, or png)
  1. Save images at the right size (same wideth and heigth it will appear on website)
  1. Measure images in pixels
- Image formats:
  - JPEG: use when many different colors in the picture
  - GIF/PNG: images with few colors or large areas of the same color
- Pixels: tiny squares on the computer screen that make up images
- Resolution: number of pixels respresented on a screen
- Transparency: creating images that are partially transparent can be done with a transparent GIF or PNG
- In HTML5: ```<figure>``` and ```<figcaption>```

## Color (HTML & CSS book, pg. 246-263)
- Colors we seen on a screen are created by mixing amounts of red, green and blue (RGB)
- Ways to specify color: RGB values, Hex codes, color names
- Keep in mind hue, saturation, and brightness
- Contrast: ensure there is enough contrast in the text and background color to make things readable
- CSS3 new features:
  - ```opacity``` property, will allows you to specify the opacity of an element (RGBA)
  - Hue/saturation/lightness values to specify colors (```hsl``` and ```hsla```)

## Text (HTML & CSS book, pg. 264-299)
- Typeface terminology:
  - serif: extra details on the ends of the main strokes of letters
  - sans-serif: straight ends to letters (cleaner design)
  - monospace: every letter is fixed width (fixed width font)
- Broswers will only display typefaces if they are installed on that user's computer
- PC and Mac can render tyle differently
- Specifying typefaces: ```font-family```
- Size of type: ```font-size``` (in pixels, or ems, default is 16px)
- Bold: ```font-weight``` property (normal, bold)
- Italics: ```font-style``` property (normal, italic, oblique)
- Upper/lowercase: ```text-transform``` (uppercase, lowercase, capitalize)
- Underline/strike: ```text-decoration``` (none, underline, overline, line-through, blink)
- Leading: vertical space between lines of text, ```line-height```
- Letter and word spacing: ```letter-spacing``` and ```word-spacing```
- Kerning: space between each letter
- Alignment: ```text-align``` (left, right, center, justify)
- Vertical alignment: ```vertical-align``` (baseline, sub, super, top, text-top, middle, bottom, text-bottom)
- Indenting: ```text-indent```
- Drop shadow: ```text-shadow```
- Styling links: ```:link```, ```:visited```
- Responding to users: ```:hover```, ```:active```, ```:focus```
- Attribute selectors: 
  - Existence: []
  - Equality: [=]
  - Space: [~=]
  - Prefix: [^=]
  - Substring: [*=]
  - Suffix: [$=]


[<==Back>](../README.md)