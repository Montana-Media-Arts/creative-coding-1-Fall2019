---
title: Moving Simple Shapes
module: 10
jotted: true
---

# Moving Simple Shapes

Remember in the last section how to created the new variables and then used them to print out numbers and change colors?  What else can we do?  The better question is why?

Let's look at this example.

```html

var red = 123;
var green = 39;
var blue = 21;

var x = 100;
var y = 200;
var diameter = 50;
function setup()
{

    createCanvas(800,600);
}

function draw()
{
    background(red,green,blue);
    circle(x,y,diameter);
}
```
Do you see your background with a circle?  I hope so!

This is all fine, but you are probably saying, "How is this any different from before?";

Glad you asked!  Let's make a small change and see what happens.

```html

var red = 123;
var green = 39;
var blue = 21;

var x = 100;
var y = 200;
var diameter = 50;
function setup()
{

    createCanvas(800,600);
}

function draw()
{
    background(red,green,blue);
    circle(x,y,diameter);
    x++;
}
```

Run the preceding code and see what happens.

Did the circle move?  Which way? Why?

What if we did the same to **y**?  Which way would it go?

## Adding a second moving shape

That is crazy!  We just made a simple shape move.  What if we added a second one?

```html

var red = 123;
var green = 39;
var blue = 21;

var x = 100;
var y = 200;
var diameter = 50;
function setup()
{

    createCanvas(800,600);
}

function draw()
{
    background(red,green,blue);
    circle(x,y,diameter);
    circle(x,y,diameter);
    x++;
}
```

Do you get two circles?  Oh dang!  You don't right?  You just see one.

## Viewing the second shape

Well, technically you do, but you only get to see one because the other one is on top of the first one becaues they are at the same x,y coordinate and the same diameter. How can I prove it to you?  I know you are skeptics.

```html

var red = 123;
var green = 39;
var blue = 21;

var x = 100;
var y = 200;
var diameter = 50;
function setup()
{

    createCanvas(800,600);
}

function draw()
{
    background(red,green,blue);
    circle(x,y,diameter);
    fill(red,green,blue);
    circle(x,y,25);
    x++;
}
```

What do you see?  I kept the second circle in the same location, reduced the size and gave it a color - that is what the fill does.

There you go!  Okay so if you let it run long enough they should just cruise right off the screen.  But what if we don't want that?  What if I say, make it so that it stops at the edge.  What are you doing to do?

Let's go to the next section and find out!