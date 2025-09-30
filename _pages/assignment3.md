---
layout: page
title: Assignment 2
permalink: /assignment2/
---

## Assignment 2: Generative Pattern

Using for loops, create a repeating pattern in a grid-style composition. Your sketch should use a two dimensional for loop to draw a repeating series of forms. These forms should become more complex as they advance further down the Y axis of the screen. Use this piece of early code-based art as inspiration:

![Schotter](https://pbs.twimg.com/media/FdHA1F2X0AEj-uq.jpg:large)
[Schotter by Georg Nees (1968-1970)](https://collections.vam.ac.uk/item/O221321/schotter-print-nees-georg/)

Some aspect of your sketch should be responsive to the mouse position. Using either conditionals or mapping, modify the color or transformation settings of the shapes in relation to the mouse (using mouseX, mouseY and/or mouseIsPressed variables). Some possibilities:
- Your shapes switch from circles to squares when the mouse is pressed
- The shapes are translated or rotated by an increasing amount depending on the mouseY position
- The mouseX position shifts the color composition
- The rotation or translation of the shapes is animated when the mouse button is pressed down
- Etc

You may want to follow the following steps to complete your project:
- First, create the basis for your pattern as a single instance. Try to constrain this drawing to around 100px by 100px. It will be useful to use translation so that you can draw your shape around the point 0,0.
- Then, repeat your shapes using a for loop on the x axis
- Create a two dimensional for loop, repeating your shapes down the Y axis as well.
- Once you have a repeating pattern that fills the entire canvas, experiment with ways of shifting the color, style or transformation of the shapes as they advance down the Y axis
- Experiment with ways of incorporating mouse input to manipulate an aspect of the drawing (color, size of certain elements, transformations, etc).


**Evaluation:**

**Creative**: For full points, your sketch should represent a unique exploration of different repeating forms. Color should be integrated in your composition in a considered way. Your project should not merely replicate the composition of the example, but should reflect aesthetic intention of your own.

**Technical**:
For full points, your sketch should make use of multiple drawing functions. It should use a two-dimensional for loop to render repeating forms. It should make use of variable incrementation to create a compositional dynamic that intensifies along the Y axis. It should use conditionals and mouse inputs to modify or animate the composition.

Due Wednesday, October 1st at 2pm. Please share the URL to your assignment's GitHub repo and the assignment's GitHub.io site on [Brightspace](https://brightspace.nyu.edu/d2l/lms/dropbox/user/folder_submit_files.d2l?db=1083264&grpid=0&isprv=&bp=0&ou=502947).