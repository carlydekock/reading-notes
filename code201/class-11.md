# Reading 11 - Audio, Video, Images

## Images (HTML book, pg. 406-427)
- Controlling size of images in CSS (width, height specifications)
- Aligning images using CSS:
  - ```float``` property
  - Centering: image should be turned into a block level element, using ```display: block```, and then ```text-align: center``` or ```margin``` for left and right margins to auto
- Background images: ```background-image``` allows you to place an image behind any HTML element
- Repeating images: 
  - ```background-repeat```: can have four vales - repeat, repeat-x, repeat-y, no-repeat
  - ```background-attachment```: can have two values - fixed, scroll
- Background position: ```background-position``` allows you to specify where in the browser window the background image should be placed, property usually has a pair of values (first represents horizontal position, second represents vertical)
- ```background``` is shorthand for all other background properties
- Rollovers: link or button that changes to a second style when user moves their mouse over, and a third style when clicked on
- Sprite: when single image is used for several different parts of an interface

## Practical Information (HTML book, pg. 476-492)
- Search engine optimization (SEO): practice of trying to help your site appear nearer the top of search engine results
- On page techniques: methods you can use on your web pages to improve their ratings in search engines
- Off page techniques: getting other sites to link to you

### On Page SEO - 7 key places for keywords
1. Page title
1. URL/web address
1. Headings
1. Text
1. Link text
1. Image alt text
1. Page descriptions

### Site Analytics
- Google Analytics: will give you a piece of tracking code for placement on each page of your site
  - Every time someone visits your site, the racking code sends data to Google servers, provides web based interface that allows you to see how visitors use your site
  - Tracking code should appear just before the closing ```</head>``` tag
- Provides info on things like:
  - Number of visits to your site
  - Unique visits
  - Page views
  - Pages per visit

### Domain Names & Hosting
- Domain name: your web address
- Web hosting: so people can see your site you must upload it t a wb server
- Bandwidth: amount of data the hosing company will send to your site's visitors
- Backups: check whether hosting company will perform backups on your site
- Hosted services: online services that allow you to point your domain name to their servers

## MDN article - audio and video elements
- HTML5 comes with new options to embed media in documents ```<video>``` and ```<audio>```
- These come with their own APIs for controlling playback: ```HTMLMediaElement```
- The ```<video>``` element can have ```<source>``` elements so that different formats can be loaded depending on the browser viewing the site
- ```<visibility>``` control can be set to hidden or visible
- Based on event listeners and event handlers

## Chapter 9 - Flash (HTML book,  pg. 201-206)
- How Flash works: 
  - Flash authoring environment is used to create movies
  - The .fla file is exported to .swf format to use in a page
  - Then the .swf file is used in your web page using JavaScript

[<==Back>](../README.md)