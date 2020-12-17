# Reading 14 - CSS Transformations/Transitions/Animations and Psychological Safety

## CSS Transforms
- CSS3 offers new ways to position and alter elements with the ```transform``` property (two different settings: 2D and 3D)
- Include vendor prefixes at this point to gain best support across all browsers (-webkit, -moz, -o)

### 2D Rotate:
- ```rotate``` value provides ability to rotate an element from 0 to 360 degrees, positive value will rotate clockwise, negative will rotate counterclockwise. Note: the default point of rotation is the center of the element
- Using the ```scale``` value within the ```transform``` property allows you to change the appeared size of an element. Default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than 1 makes an element appear larger
- Can use the ```scaleX``` and ```scaleY``` values to scale the height and width
- ```translate``` value like that of relative positioning
- ```skew``` used to distort elements on the horizontal axis (```skewX```), vertical axis (```skewY```) or both. Distance calculation of the skew value is measured in units of degrees
- To combine multiple ```transform``` declarations, list the transform values within the property one after the other without commas
- To change the origin position, use ```transform-origin```, which can accept one or two values
- Perspective of an element can be set two different ways: ```perspective``` value within the ```transform``` property on individual elements, or using the ```perspective``` element on the parent element presiding over child elements being transformed. 
- Perspective can be set as none or a length measurement 
- Can also set ```perspective-origin``` the same way as ```transform-origin```

### 3D Rotate:
- With 3D transforms, have three new transform values ```rotateX```, ```rotateY```, and ```rotateZ```
- Using ```scaleZ``` 3D transform elements can be scaled on the z axis
- The ```translateZ``` value is added as well
- Skew is the one 2D transform that cannot be transformed on 3D scale
- To allow nested elements to transform in their own 3D plane, use ```transform-style``` property with the ```preserve-3d``` value

## CSS Transitions and Animations
- Transitions provide a change from one state to another
- Animations can set multiple points of transition upon different keyframes

### Transitions
- For a transition to take place, an element must have a change in state and different styles must be identified for each state. Easiest way for determing styles for different states is by using :hover, :focus, :active, and :target pseudo-classes
- Four transition properties in total:
  1. ```transition-property```
  1. ```transition-duration```
  1. ```transition-timing-function```
  1. ```transition-delay```
- ```transition-property```: determines exactly what properties will be altered. If multiple properties need to be transitioned they may be comma separated, or the keyword value all may be used to transition all properties of an element
- Not all properties can be transitioned, only properties that have an identifiable hallfway point
- ```transition-duration```: duration in which a transition takes place, value can be set using general timing values including seconds (s) and milliseconds (ms), and can also be in fractional measurements
- ```transition-timing-function```: used to set the speed in which a transition will move, a few common values are linear, ease-in, ease-out, ease-in-out
  - linear: identifies a transition moving in a constant speed from one state to another
  - ease-in: starts slowly and speeds up
  - ease-out: starts quickly and slows down
  - ease-in-out: starts slowly, speeds up in middle, slows down again before ending
- ```transition-delay```: sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing

### Animations
- Used when more control is needed, transitions need to have multiple states. Animations pick off where transitions leave off
- Animation keyframes: set multiple points at which an element should undergo a transition use the ```@keyframes``` rule. This rule includes the animation name, breakpoints, and the properties intended to be animated.
- The ```@keyframes``` rule must be vendor prefixed
- Need to declare ```animation-name``` and ```animation-duration```
- Once you have set the name and duration, animations behave similarly to transitions. They include a duration, timing function, and delay if desired
- Customizing animations can be used to declare the number of times an animation runs, as well as the direction in which the animation completes
- Animation iteration: ```animation-iteration-count``` can include either an integer (specific number of times to repeat) or inifite keyword
- Animation direction: ```animation-direction``` which can have values of normal, reverse, alternate, and alternate-reverse
- Animation play state: ```animation-play-state``` allows an animation to be played or paused using the running and paused keywords
- Animation fill mode: ```animation-fill-mode``` identifies how an element should be styled either before, after, or before and after an animation is run. Accepts four keyword values: none, forwards, backwards, and both

## CSS3 Transitions - 8 Examples
1. Fade in: great way to emphasize functionality or draw attention to a call to action. First, set initial state, next you set the change.
1. Change color: set the div's class to color and specify the color you want.
1. Grow and shrink: can use the CSS transform to enlarge, set div class to grow.
1. Rotate elements: can set div class to rotate, add in transform rotation.
1. Square to circle: very popular at the moment, can be done in the reverse as well. In CSS can be done by transitioning the border-radius property.
1. 3D shadow: work well to give a user feedback on their interactions. Effect is achieved by adding a box shadow, then moving the element on the x axis using the transform and translate properties.
1. Swing: moving an element to the right and left, takes a bit more code.
1. Inset border: example is a ghost button or button with no background and a heavy border. Can transition in a border using an inset box shadow.

## What Google Learned - Psychological Safety
- Group norms typicaly override individual proclivities and encourage deference to the team.
- What distinguishes the good team from the dysfunctional groups was how teammates treated one another. The right norms could raise a group's collective intelligence, wheras the wrong norms could hobble a team.
- Equality in distribution of conversational turn-taking.
- High average social sensitivity - skilled at intuiting how others felt based on their tone of voice, expressions, and other nonverbal cues.
- Psychological safety: sense of confidence that the team will not embarrass, reject or punish someone for speaking up.
- Team climate characterized by interpersonal trust and mutual respect in which people are comfortable being themselves.
- The behaviors that create psychological safety - conversational turn-taking and empathy - are part of the same unwritten rules we often turn to, as individuals, when we need to establish a bond.
- The be fully present at work, to feel "psychologically safe", we must know that we can be free enough, sometimes, to share the things that scare us without fear of recriminations.

[<==Back>](README.md)