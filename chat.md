NotebookLM (https://notebooklm.google.com/notebook/28e801cb-3210-4c8a-8dc6-56a91d3a6ce0)
2025-03-22

create code to show an ellipse that moves with keyboard

```
let ellipseX;
let ellipseY;
let moveSpeed = 5; // Adjust for faster or slower movement

function setup() {
  createCanvas(400, 400);
  // Initialize the ellipse in the center of the canvas
  ellipseX = width / 2;
  ellipseY = height / 2;
}

function draw() {
  background(220);
  // Draw the ellipse at its current position
  ellipse(ellipseX, ellipseY, 50, 50);
}

function keyPressed() {
  // Check which key was pressed and update the ellipse's position
  if (keyCode === LEFT_ARROW) {
    ellipseX -= moveSpeed; // Move left
  } else if (keyCode === RIGHT_ARROW) {
    ellipseX += moveSpeed; // Move right
  } else if (keyCode === UP_ARROW) {
    ellipseY -= moveSpeed; // Move up
  } else if (keyCode === DOWN_ARROW) {
    ellipseY += moveSpeed; // Move down
  } else if (key === 'r' || key === 'R') {
    // Reset the ellipse to the center if 'r' or 'R' is pressed [1]
    ellipseX = width / 2;
    ellipseY = height / 2;
  }
}
```

now add code to make the ellipse wrap around the canvas

```
let ellipseX;
let ellipseY;
let moveSpeed = 5; // Adjust for faster or slower movement
let ellipseDiameter = 50; // Added variable for clarity

function setup() {
  createCanvas(400, 400);
  // Initialize the ellipse in the center of the canvas
  ellipseX = width / 2;
  ellipseY = height / 2;
}

function draw() {
  background(220);

  // **Handle horizontal wrap-around**
  if (ellipseX < 0 - ellipseDiameter / 2) {
    ellipseX = width + ellipseDiameter / 2;
  } else if (ellipseX > width + ellipseDiameter / 2) {
    ellipseX = 0 - ellipseDiameter / 2;
  }

  // **Handle vertical wrap-around**
  if (ellipseY < 0 - ellipseDiameter / 2) {
    ellipseY = height + ellipseDiameter / 2;
  } else if (ellipseY > height + ellipseDiameter / 2) {
    ellipseY = 0 - ellipseDiameter / 2;
  }

  // Draw the ellipse at its current position
  ellipse(ellipseX, ellipseY, ellipseDiameter, ellipseDiameter);
}

function keyPressed() {
  // Check which key was pressed and update the ellipse's position
  if (keyCode === LEFT_ARROW) {
    ellipseX -= moveSpeed; // Move left
  } else if (keyCode === RIGHT_ARROW) {
    ellipseX += moveSpeed; // Move right
  } else if (keyCode === UP_ARROW) {
    ellipseY -= moveSpeed; // Move up
  } else if (keyCode === DOWN_ARROW) {
    ellipseY += moveSpeed; // Move down
  } else if (key === 'r' || key === 'R') {
    // Reset the ellipse to the center if 'r' or 'R' is pressed
    ellipseX = width / 2;
    ellipseY = height / 2;
  }
}
```

now add code so that the entire ellipse is always visible in the canvas. when part of the ellipse goes off on one side, the corresponding part should show up on the opposite side.

```
let ellipseX;
let ellipseY;
let moveSpeed = 5; // Adjust for faster or slower movement
let ellipseDiameter = 50; // Variable for the ellipse diameter

function setup() {
  createCanvas(400, 400);
  // Initialize the ellipse in the center of the canvas
  ellipseX = width / 2;
  ellipseY = height / 2;
}

function draw() {
  background(220);

  // **Handle horizontal wrap-around (entire ellipse visible)**
  if (ellipseX < 0) {
    ellipseX = width;
  } else if (ellipseX > width) {
    ellipseX = 0;
  }

  // **Handle vertical wrap-around (entire ellipse visible)**
  if (ellipseY < 0) {
    ellipseY = height;
  } else if (ellipseY > height) {
    ellipseY = 0;
  }

  // Draw the ellipse at its current position
  ellipse(ellipseX, ellipseY, ellipseDiameter, ellipseDiameter);
}

function keyPressed() {
  // Check which key was pressed and update the ellipse's position
  if (keyCode === LEFT_ARROW) {
    ellipseX -= moveSpeed; // Move left
  } else if (keyCode === RIGHT_ARROW) {
    ellipseX += moveSpeed; // Move right
  } else if (keyCode === UP_ARROW) {
    ellipseY -= moveSpeed; // Move up
  } else if (keyCode === DOWN_ARROW) {
    ellipseY += moveSpeed; // Move down
  } else if (key === 'r' || key === 'R') {
    // Reset the ellipse to the center if 'r' or 'R' is pressed
    ellipseX = width / 2;
    ellipseY = height / 2;
  }
}
```

that's not what I meant. I don't want the ellipse to jump from one side to another, but whenever a part of the ellipse disappears on one side, that same part should show up on the opposite side.

```
let ellipseX;
let ellipseY;
let moveSpeed = 5; // Adjust for faster or slower movement
let ellipseDiameter = 50; // Variable for the ellipse diameter

function setup() {
  createCanvas(400, 400);
  // Initialize the ellipse in the center of the canvas
  ellipseX = width / 2;
  ellipseY = height / 2;
}

function draw() {
  background(220);

  // Draw the main ellipse
  ellipse(ellipseX, ellipseY, ellipseDiameter, ellipseDiameter);

  // **Handle horizontal wrap-around**
  if (ellipseX < 0) {
    ellipse(ellipseX + width, ellipseY, ellipseDiameter, ellipseDiameter); // Draw on the right
  } else if (ellipseX > width) {
    ellipse(ellipseX - width, ellipseY, ellipseDiameter, ellipseDiameter); // Draw on the left
  }

  // **Handle vertical wrap-around**
  if (ellipseY < 0) {
    ellipse(ellipseX, ellipseY + height, ellipseDiameter, ellipseDiameter); // Draw on the bottom
  } else if (ellipseY > height) {
    ellipse(ellipseX, ellipseY - height, ellipseDiameter, ellipseDiameter); // Draw on the top
  }

  // **Handle corner cases (when wrapping happens in both directions)**
  if (ellipseX < 0 && ellipseY < 0) {
    ellipse(ellipseX + width, ellipseY + height, ellipseDiameter, ellipseDiameter); // Bottom right
  } else if (ellipseX < 0 && ellipseY > height) {
    ellipse(ellipseX + width, ellipseY - height, ellipseDiameter, ellipseDiameter); // Top right
  } else if (ellipseX > width && ellipseY < 0) {
    ellipse(ellipseX - width, ellipseY + height, ellipseDiameter, ellipseDiameter); // Bottom left
  } else if (ellipseX > width && ellipseY > height) {
    ellipse(ellipseX - width, ellipseY - height, ellipseDiameter, ellipseDiameter); // Top left
  }
}

function keyPressed() {
  // Check which key was pressed and update the ellipse's position
  if (keyCode === LEFT_ARROW) {
    ellipseX -= moveSpeed; // Move left
  } else if (keyCode === RIGHT_ARROW) {
    ellipseX += moveSpeed; // Move right
  } else if (keyCode === UP_ARROW) {
    ellipseY -= moveSpeed; // Move up
  } else if (keyCode === DOWN_ARROW) {
    ellipseY += moveSpeed; // Move down
  } else if (key === 'r' || key === 'R') {
    // Reset the ellipse to the center if 'r' or 'R' is pressed
    ellipseX = width / 2;
    ellipseY = height / 2;
  }
}
```

that kind of works. there are some corner case bugs. can it be refactored to use a class to make the code cleaner and easier to debug?

```
class WrappingEllipse {
  constructor(x, y, diameter, moveSpeed) {
    this.x = x;
    this.y = y;
    this.diameter = diameter;
    this.moveSpeed = moveSpeed;
  }

  move() {
    if (keyIsDown(LEFT_ARROW)) {
      this.x -= this.moveSpeed;
    }
    if (keyIsDown(RIGHT_ARROW)) {
      this.x += this.moveSpeed;
    }
    if (keyIsDown(UP_ARROW)) {
      this.y -= this.moveSpeed;
    }
    if (keyIsDown(DOWN_ARROW)) {
      this.y += this.moveSpeed;
    }
  }

  handleWrapAround() {
    // Handle horizontal wrap-around
    if (this.x < 0) {
      ellipse(this.x + width, this.y, this.diameter, this.diameter); // Draw on the right
    } else if (this.x > width) {
      ellipse(this.x - width, this.y, this.diameter, this.diameter); // Draw on the left
    }

    // Handle vertical wrap-around
    if (this.y < 0) {
      ellipse(this.x, this.y + height, this.diameter, this.diameter); // Draw on the bottom
    } else if (this.y > height) {
      ellipse(this.x, this.y - height, this.diameter, this.diameter); // Draw on the top
    }

    // Handle corner cases
    if (this.x < 0 && this.y < 0) {
      ellipse(this.x + width, this.y + height, this.diameter, this.diameter); // Bottom right
    } else if (this.x < 0 && this.y > height) {
      ellipse(this.x + width, this.y - height, this.diameter, this.diameter); // Top right
    } else if (this.x > width && this.y < 0) {
      ellipse(this.x - width, this.y + height, this.diameter, this.diameter); // Bottom left
    } else if (this.x > width && this.y > height) {
      ellipse(this.x - width, this.y - height, this.diameter, this.diameter); // Top left
    }
  }

  draw() {
    ellipse(this.x, this.y, this.diameter, this.diameter); // Draw the main ellipse
    this.handleWrapAround(); // Handle drawing the wrapping ellipses
  }

  resetToCenter() {
    this.x = width / 2;
    this.y = height / 2;
  }
}

let myEllipse;
let moveSpeed = 5;
let ellipseDiameter = 50;

function setup() {
  createCanvas(400, 400);
  myEllipse = new WrappingEllipse(width / 2, height / 2, ellipseDiameter, moveSpeed);
}

function draw() {
  background(220);
  myEllipse.move();
  myEllipse.draw();
}

function keyPressed() {
  if (key === 'r' || key === 'R') {
    myEllipse.resetToCenter();
  }
}
```

again, this only works when the center of the ellipse has gone out of the canvas. it should work even when a tiny part of it goes off the side

```
class WrappingEllipse {
  constructor(x, y, diameter, moveSpeed) {
    this.x = x;
    this.y = y;
    this.diameter = diameter;
    this.radius = diameter / 2; // Calculate the radius
    this.moveSpeed = moveSpeed;
  }

  move() {
    if (keyIsDown(LEFT_ARROW)) {
      this.x -= this.moveSpeed;
    }
    if (keyIsDown(RIGHT_ARROW)) {
      this.x += this.moveSpeed;
    }
    if (keyIsDown(UP_ARROW)) {
      this.y -= this.moveSpeed;
    }
    if (keyIsDown(DOWN_ARROW)) {
      this.y += this.moveSpeed;
    }
  }

  handleWrapAround() {
    // Handle horizontal wrap-around
    **if (this.x - this.radius < 0)** {
      ellipse(this.x + width, this.y, this.diameter, this.diameter); // Draw on the right
    **} else if (this.x + this.radius > width)** {
      ellipse(this.x - width, this.y, this.diameter, this.diameter); // Draw on the left
    }

    // Handle vertical wrap-around
    **if (this.y - this.radius < 0)** {
      ellipse(this.x, this.y + height, this.diameter, this.diameter); // Draw on the bottom
    **} else if (this.y + this.radius > height)** {
      ellipse(this.x, this.y - height, this.diameter, this.diameter); // Draw on the top
    }

    // Handle corner cases
    if (this.x - this.radius < 0 && this.y - this.radius < 0) {
      ellipse(this.x + width, this.y + height, this.diameter, this.diameter); // Bottom right
    } else if (this.x - this.radius < 0 && this.y + this.radius > height) {
      ellipse(this.x + width, this.y - height, this.diameter, this.diameter); // Top right
    } else if (this.x + this.radius > width && this.y - this.radius < 0) {
      ellipse(this.x - width, this.y + height, this.diameter, this.diameter); // Bottom left
    } else if (this.x + this.radius > width && this.y + this.radius > height) {
      ellipse(this.x - width, this.y - height, this.diameter, this.diameter); // Top left
    }
  }

  draw() {
    ellipse(this.x, this.y, this.diameter, this.diameter); // Draw the main ellipse
    this.handleWrapAround(); // Handle drawing the wrapping ellipses
  }

  resetToCenter() {
    this.x = width / 2;
    this.y = height / 2;
  }
}

let myEllipse;
let moveSpeed = 5;
let ellipseDiameter = 50;

function setup() {
  createCanvas(400, 400);
  myEllipse = new WrappingEllipse(width / 2, height / 2, ellipseDiameter, moveSpeed);
}

function draw() {
  background(220);
  myEllipse.move();
  myEllipse.draw();
}

function keyPressed() {
  if (key === 'r' || key === 'R') {
    myEllipse.resetToCenter();
  }
}
```

hmmm. something is wrong. if the ellipse wraps around more than 2 times it disappears.

```
class WrappingEllipse {
  constructor(x, y, diameter, moveSpeed) {
    this.x = x;
    this.y = y;
    this.diameter = diameter;
    this.radius = diameter / 2; // Calculate the radius
    this.moveSpeed = moveSpeed;
  }

  move() {
    if (keyIsDown(LEFT_ARROW)) {
      this.x -= this.moveSpeed;
    }
    if (keyIsDown(RIGHT_ARROW)) {
      this.x += this.moveSpeed;
    }
    if (keyIsDown(UP_ARROW)) {
      this.y -= this.moveSpeed;
    }
    if (keyIsDown(DOWN_ARROW)) {
      this.y += this.moveSpeed;
    }
  }

  handleWrapAround() {
    // Repeatedly handle horizontal wrap-around
    while (this.x - this.radius < 0) {
      this.x += width;
    }
    while (this.x + this.radius > width) {
      this.x -= width;
    }

    // Repeatedly handle vertical wrap-around
    while (this.y - this.radius < 0) {
      this.y += height;
    }
    while (this.y + this.radius > height) {
      this.y -= height;
    }

    // Now that the main ellipse is within bounds, draw the wrapping ellipses for visual continuity

    // Handle horizontal wrapping for drawing
    if (this.x - this.radius < 0) {
      ellipse(this.x + width, this.y, this.diameter, this.diameter); // Draw on the right
    } else if (this.x + this.radius > width) {
      ellipse(this.x - width, this.y, this.diameter, this.diameter); // Draw on the left
    }

    // Handle vertical wrapping for drawing
    if (this.y - this.radius < 0) {
      ellipse(this.x, this.y + height, this.diameter, this.diameter); // Draw on the bottom
    } else if (this.y + this.radius > height) {
      ellipse(this.x, this.y - height, this.diameter, this.diameter); // Draw on the top
    }

    // Handle corner cases for drawing
    if (this.x - this.radius < 0 && this.y - this.radius < 0) {
      ellipse(this.x + width, this.y + height, this.diameter, this.diameter); // Bottom right
    } else if (this.x - this.radius < 0 && this.y + this.radius > height) {
      ellipse(this.x + width, this.y - height, this.diameter, this.diameter); // Top right
    } else if (this.x + this.radius > width && this.y - this.radius < 0) {
      ellipse(this.x - width, this.y + height, this.diameter, this.diameter); // Bottom left
    } else if (this.x + this.radius > width && this.y + this.radius > height) {
      ellipse(this.x - width, this.y - height, this.diameter, this.diameter); // Top left
    }
  }

  draw() {
    ellipse(this.x, this.y, this.diameter, this.diameter); // Draw the main ellipse
    this.handleWrapAround(); // Handle drawing the wrapping ellipses
  }

  resetToCenter() {
    this.x = width / 2;
    this.y = height / 2;
  }
}

let myEllipse;
let moveSpeed = 5;
let ellipseDiameter = 50;

function setup() {
  createCanvas(400, 400);
  myEllipse = new WrappingEllipse(width / 2, height / 2, ellipseDiameter, moveSpeed);
}

function draw() {
  background(220);
  myEllipse.move();
  myEllipse.draw();
}

function keyPressed() {
  if (key === 'r' || key === 'R') {
    myEllipse.resetToCenter();
  }
}
```

why does the ellipse blink when it wraps from left to right?

hold my beer....
```
class MovingEllipse {
  constructor(x, y, diameter, moveSpeed) {
    this.x = x;
    this.y = y;
    this.diameter = diameter;
    this.moveSpeed = moveSpeed;
  }

  move() {
    if (keyIsDown(LEFT_ARROW)) {
      this.x -= this.moveSpeed;
    }
    if (keyIsDown(RIGHT_ARROW)) {
      this.x += this.moveSpeed;
    }
    if (keyIsDown(UP_ARROW)) {
      this.y -= this.moveSpeed;
    }
    if (keyIsDown(DOWN_ARROW)) {
      this.y += this.moveSpeed;
    }

    this.x = (this.x + width) % width;
    this.y = (this.y + height) % height;
  }

  draw() {
    ellipse(this.x, this.y, this.diameter, this.diameter);
  }

  resetToCenter() {
    this.x = width / 2;
    this.y = height / 2;
  }
}

class WrappingEllipse {
  constructor(x, y, diameter, moveSpeed) {
    this.els = [];
    for (let i = 0; i < 5; i++) {
      this.els.push(new MovingEllipse(x, y, diameter, moveSpeed));
    }
  }

  move() {
    for (let el of this.els) {
      el.move();
    }
  }

  resetToCenter() {
    for (let el of this.els) {
      el.resetToCenter();
    }
  }

  draw() {
    push();
    translate(-width, 0);
    this.els[0].draw();

    translate(2*width, 0);
    this.els[1].draw();
    pop();

    push();
    translate(0, -height);
    this.els[2].draw();

    translate(0, 2*height);
    this.els[3].draw();
    pop();

    this.els[4].draw();
  }
}

let myEllipse;
let moveSpeed = 5;
let ellipseDiameter = 80;

function setup() {
  createCanvas(400, 400);
  myEllipse = new WrappingEllipse(
    width / 2,
    height / 2,
    ellipseDiameter,
    moveSpeed
  );
}

function draw() {
  background(220);
  myEllipse.move();
  myEllipse.draw();
}

function keyPressed() {
  if (key === "r" || key === "R") {
    myEllipse.resetToCenter();
  }
}
```
