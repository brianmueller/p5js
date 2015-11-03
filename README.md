# [p5.js](http://p5js.org/) tutorial
### _Using code to make interactive art_
_Brian Mueller_

---
## Introduction
* `p5.js` is a JavaScript library modeled after `Processing`, a Java library
 * _all JavaScript syntax rules apply_
* runs nicely in an HTML page

---
## Getting Started
* **template**: use [tiny.cc/p5template](https://gist.githubusercontent.com/bmuellerhstat/bd0ca8ce27961f9c264d/raw/5bdc81a80b9ff726949078905b9c0d64b528215b/p5-template.html) to get started
 * using offline? make sure you download the [p5.js](http://p5js.org/download/) file
 * you can also fork/clone this repo
* IDEs 
 * **[Atom](http://atom.io/)** (live preview)
 * **[Cloud9](http://c9.io/)** (cloud based, semi-live preview)
 * **[Nitrous](http://www.nitrous.io/)** (requires using `python -m SimpleHTTPServer -p 3000`)
* sandbox: **[jsbin.com](http://jsbin.com/)**
* native IDE: [p5js](http://p5js.org/download/) > editor  

---
## Understanding the Structure
* `function setup(){}` is called **once** on load  
* `function draw(){}` is called **60 times per second**
   * you can change this with `frameRate(#)`
* `createCanvas(w,h)` sets the size of your sketch (px)
 * optional: you can use `displayWidth` and `displayHeight` (or `windowWidth` and `windowHeight`)

---
## Shapes
* the 4 basic shapes
 * `point(x,y)`
 * `line(x1,y1,x2,y2)`
 * `rect(x,y,w,h)`
   * **draws from the top-left corner**
    * default "mode" is `rectMode(CORNER)`
    * `rectMode(CENTER)` **draws from the center**
    * `rectMode(CORNERS)` uses diagonal corners: `rect(x1,y1,x2,y2)`
    * see [documentation](http://p5js.org/reference/#/p5/rect) for rounded edges
 * `ellipse(x,y,w,h)`
   * **draws from the center**
    * default "mode" is `ellipseMode(CENTER)`
    * can also use `ellipseMode(CORNER)` and `ellipseMode(CORNERS)` _(similar to_ `rectMode()`_)_
* other shapes
 * `triangle`, `quad`rilateral, etc. (see [documentation](http://p5js.org/reference/))

---
## Color
* **color theory**
 * min = `0` _(none of that color)_
 * max = `255` _(100% of that color)_
 * three values represent RGB values, i.e. `(255,0,0)` means red _(no green or blue)_
 * one value represents grayscale (all RGB values are equal `(150) = (150,150,150)`
 * `0` = black, `255` = white
* **color commands**: the setting will be applied to _all future shapes_ until the setting is changed again
 * `fill(R,G,B,[A])` sets the interior color
   * `[A]` is an optional "alpha" (opacity) argument
 * `stroke(R,G,B,[A])` sets the outline color
 * `strokeWeight(#)` sets the outline thickness (px)
 * `background(R,G,B)` sets the color of the background
   * use inside `function setup(){}` to run once
   * use inside `function draw(){}` to "wipe" the background for each frame

---
## Variables
* **global** variables must be declared _outside_ of all functions
 * their scope is visible inside & outside all functions
* **local** variables are declared _inside_ a function
 * their scope is limited to that specific function
* **system** variables are reserved keywords for values such as the `width` and `height` of the canvas

---
## Interaction
* `mouseX` and `mouseY` are system variables that contain the coordinates of the user's mouse
* `function mousePressed(){}` is called when the user clicks the mouse
* `function keyPressed(){}` is called when the user presses a key

Read more in the [documentation](http://p5js.org/reference/) under **Events** (including mobile: `touchX`, `touchY`, etc).

---
## Conditionals
```javascript
if (condition){
  // code
} else if (condition){
  // code
}
else {
  // default
}
```

---
## Loops
```javascript
while (condition) {
  // code
}
```
```javascript
do {
  // code
} while (condition);
```
```javascript
for (var i = 0; i < num; i++) {
  // code
}
```
---
## Functions
```javascript
// defining your function
function myFunction(optional parameters){
  // code
}

// calling your function
myFunction(arguments);
```

---
## Arrays
```javascript
var arrayName = [item1, item2, ...];
arrayName[1]; // returns item2
```

---
## Examples
* [Random Circles](random-circles.html)
* [Ghost](ghost.html)
* [Flower (relative position)](flower-relative-position.html)
* [Flower dilation](flower-dilation.html)
* [Interaction & Loops](interaction-loop.html)
* [Interaction & Graffiti](interaction-graffiti.html)
* [Circle Orb](circle-orb.html)
* [Kuku Kube](http://brianmueller.github.io/kuku-kube/) [[mobile](http://brianmueller.github.io/kuku-kube/mobile)]
* [Pong](pong.html)
