# p5.js tutorial
_Brian Mueller_

---
## Getting Started
* **template**: use [NEEDS gist LINK] to get started
 * using offline? make sure you download the p5.js file
* IDEs
 * **Atom** (live preview)
 * **Cloud9** (cloud based, semi-live preview)
 * **Nitrous** (requires using `python -m SimpleHTTPServer -p 3000`)
* sandbox: **jsbin.com**
* native IDE: [NEEDS p5 LINK]
---
## Understanding the Structure
* `function setup(){}` is called **once** on load  
* `function draw(){}` is called **30 times per second** [CHECK FRAMERATE]
* `createCanvas(w,h)` sets the size of your sketch (px)
 * optional: you can use `displayWidth` and `displayHeight`

---
## Shapes
* the 4 basic shapes
 * `point(x1,y1)`
 * `line(x1,y1,x2,y2)`
 * `rect(x,y,w,h)`
   * **draws from the top-left corner**
   * default "mode" is `rectMode(CORNER)`
   * `rectMode(CENTER)` **draws from the center**
   * `rectMode(CORNERS)` uses diagonal corners: `rect(x1,y1,x2,y2)`
   * see documentation for rounded edges [NEEDS LINK]
 * `ellipse(x,y,w,h)`
   * **draws from the center**
   * default "mode" is `ellipseMode(CENTER)`
   * can also use `ellipseMode(CORNER)` and `ellipseMode(CORNERS)` _(similar to_ `rectMode()`_)_
* other shapes
 * triangle, quadrilateral, etc. (see documentation)

---
## Color
* **color theory**
 * min = `0` _(none of that color)_
 * max = `255` _(100% of that color)_
 * three values represent RGB values, i.e. `(255,0,0)` means red _(no green or blue)_
 * one value represents grayscale (all RGB values are equal `(150) = (150,150,150)`
 * so `(0)` = black, `(255)` = white
* **color commands**: the setting will be applied to _all future shapes_ until the setting is changed again
 * `fill(R,G,B,[A])` sets the interior color
   * `[A]` is an optional "alpha" (opacity) argument
 * `stroke(R,G,B,[A])` sets the outline color
 * `strokeWeight(#)` sets the outline thickness (px)

---
## Variables
* **global** variables must be declared _outside_ of all functions
 * their scope is visible inside & outside all functions
* **local** variables are declared _inside_ a function
 * their scope is limited to that specific function
* **system** variables are reserved keywords for values such as the `width` and `height` of the canvas

---
## Interaction
* `mouseX` and `mouseY` are system variables that use the coordinates of the user's mouse
* `function mousePressed(){}` is called when the user clicks the mouse
* `function keyPressed(){}` is called when the user presses a key

---
## Conditionals

---
## Loops

---
## Functions

---
## Arrays

---
## Objects

---
## Examples
