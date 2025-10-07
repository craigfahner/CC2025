---
layout: page
title: Assignment 4
permalink: /assignment4/
---

## Assignment 4: Object Factory

There are two different concepts you may use for this assignment:

**Object Kitchen**:

Imagine a restaurant that serves a particular type of food - sushi, ramen, pizza, sandwiches, etc. Create a p5.js sketch that produces images of these food items and displays them to the canvas, using a class that accepts different parameters that affect the appearance of the food items. For instance, a "pizza" class might consider the following parameters:

* type of pizza (which ingredients)
* size of pizza
* number of toppings
* x position
* y position

Your class should generate objects that produce a drawing of a unique food item that plots different ingredients (pepperoni, mushrooms, etc) according to the provided parameters. You should use the translate() function and push() and pop() to position the food items on the canvas. It is up to you to determine how your food item class will assemble and draw the "ingredients", though I recommend using some of the following functions:

* random()
* dist()
* cos(), sin() - polar coordinates
* translate() and rotate()

Your class should contain conditionals that draw the food item differently depending on the "order" specified in the class' constructor. Your class should be able to generate at least three different variations on the food item (eg, cheese, pepperoni, mushroom pizzas).

Once you’ve created your food item class, create a simple sketch that renders food items of varying types and sizes to the canvas. Here are some options for doing this:

* create a new randomized food item object on mousePressed(), rendering the item at the mouse position
* * for a gold star, have the food items disappear when they are clicked on, using the Array.splice function.
* create a new randomized food item object once every second using the second() function
* create a new food item object at a random position when different keyboard events are detected (a pepperoni pizza when the “p” key is pressed, for instance)
* feel free to implement animations in your project, moving the objects around using noise(), lerp() or atan().

**Alternative concept: Robot Generator**:

Same parameters as above, but a character generator instead of a "food" generator.  Create a character generator that uses classes and objects to create a character. I recommend using geometric forms to create character designs that resemble a “robot”, but you’re welcome to take this in your own direction as well.

Your character generator should create different variations of the same type of character. You can think of this as similar to an avatar generator for a video game where you can select different options for clothing, hair, etc. Create at least four parameters that will change the color and form of different components of your character. Same requirements as above, except this will generate variations of a character.

**Technical**: For full points, your sketch should meet all of the above outlined technical requirements. It should contain a functioning food item / character class that generates dynamic objects. It should make use of the random() function, the translate() function, conditionals, arrays, for loops and at least one of the following additional functions: dist(), cos() and sin(), mousePressed(), keyPressed(), second(). Your code should run without any errors, and should be thoroughly commented. **You may not use any functions that have not yet been explored in this class. Any inclusions of external code will be ignored.**

**Creative**: Your project should be a unique exploration of the above constraints. Your food/character item class should generate graphical compositions that are aesthetically considered. Your ingredients should be constrained to the area of your food item/your character's physical features should be properly positioned and aesthetically considered. Your method of rendering should be aesthetically considered and unique. For full points, your project should go beyond the basic requirements outlined above, reflecting a creative intention that is unique to you.

Due Wednesday, October 22nd at 1pm. **An in-progress version is due October 15th, which should have the following elements completed:**
- A "static" example of your food items should be drawn to the canvas, and should be responsive to transform functions (ie, translating your object to 200,200 should center the object at 200,200)
- Your concept should be developed

