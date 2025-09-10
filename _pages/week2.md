---
layout: page
title: Week 2
permalink: /week2/
---

## Week 2 Activities

- GitHub refresher and Brightspace submission
- AI Discussion
- Human computer exercise
- [Getting to know the p5.js reference](https://p5js.org/reference/)
- "Hello world" - basic JavaScript syntax

---

### JavaScript basics

- [An introduction to client-side scripting](https://idmp5.github.io/intro/javascript/)

Your basic template for p5.js looks like this:

```
function setup() {
  createCanvas(windowWidth, windowHeight);
  
}

function draw() {
  
}
```

Even though this template doesn't render any graphics or "do anything", we can see some key components of JavaScript syntax here:

**function** is a keyword that declares a given *block* of code as carrying out a particular task in our program. Blocks of code are enclosed by curly brackets (**{** and **}**)

In p5.js, all programs (or "sketches" in p5 lingo) have a **setup** and **draw** function. **Setup** is a function that is called once when your program starts. You use it to do things like set the size and background of your canvas, and other initialization tasks.

**Draw** is a function that, by default, loops forever after setup finishes running. We use it to do things like handling interactions and animating graphics. Most of your actual designing and coding happens in the **draw** loop, at least for now.

Inside our template's `setup` function, we see an indented line of code that reads `createCanvas(windowWidth, windowHeight);`

This is a built-in function of p5.js that creates a drawing context (or *canvas*) in the browser, according to a specified width and height. Beyond functions that are *declared* as setup and draw, there are numerous built-in functions in p5.js and JavaScript that do things like draw shapes, handle interactions, and more.

These functions are typically formatted like so: `functionName(parameter1, parameter2, parameter3);`. Functions always appear with parentheses following their name – this is how we know they are functions and not *variables*, which we will learn about later. Within the parentheses, we find *parameters*, which are like the settings for our function. For instance, a *circle* function takes parameters setting its size and position, like so: `circle(50, 100, 25);`, which places a circle at the coordinate 50,100 which is 25 pixels in size. In the `createCanvas(windowWidth, windowHeight);` function, we are providing parameters that set the width and height of the canvas to be created. In this instance, we are using a pair of *system variables* that are built-in to p5js, which pass through the current width and height of the browser window: `windowWidth` and `windowHeight`. The order that parameters are specified inside the parentheses is important! To know what parameters are expected, and in what order, refer to the [p5.js reference](https://p5js.org/reference/).

Experiment with the **[circle](https://p5js.org/reference/p5/circle/)** function, placing it inside of the **draw** loop. Use different numbers for the different parameters, keeping in mind that the first paramater is the x (horizontal) position, the second is the y (vertical) position, and the third parameter is the size (diameter in pixels).

You should get used to **commenting** your code. Comments are written using the double-slash notation, and can be placed at the end of any line of code (or on a blank line of code). We use comments to make notes in our code to explain how things are working - they help make code more readable, and help us to recall what we were thinking about when we were working on something. Here's an example of commenting:

```
function setup() { // this block of code runs ONCE at the beginning
  createCanvas(windowWidth, windowHeight);
  
}

function draw() { // after setup has run, the code in the draw block runs as a loop forever
  
}
```

[Here](https://github.com/craigfahner/CC2025-cef9489/blob/main/week2/sketch.js) is a link to the code I wrote during class, if you need to catch up!

---


### For Next Week

Read over the following tutorials:

- [P5.js intro](https://idmp5.github.io/p5/p5-intro/)
- [Shapes and Colors](https://idmp5.github.io/p5/drawing/)
- [Coordinates and Shapes](https://archive.p5js.org/learn/coordinate-system-and-shapes.html)
- [Color and Form](https://openprocessing.org/sketch/2003621) - follow every step of this tutorial!

In your week2 folder, modify the sketch.js file, adding at least two more shapes to the code you created in class. Use comments in your sketch. Commit and push your code to your GitHub repo, making some notes in the week2 readme.md folder documenting what you have added.