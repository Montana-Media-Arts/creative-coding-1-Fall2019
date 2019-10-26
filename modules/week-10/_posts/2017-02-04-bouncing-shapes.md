---
title: Bouncing Shapes
module: 10
jotted: true
---

# Bouncing Shapes

Now, that you know how to make the shape stop, how to we make it go the opposite way when it hits the wall?

Let's start where we left off.

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
    if(x <= 800)
    {
        x+=7;
    }
    
}
```

The trick is that we need the x to go the opposite way.  How do we make the shape go to the left?  If adding to the x made it go to the right, then... yes, subtracting makes it go to the left.  Remember everything starts at 0,0 in the upper left hand corner.  So, all we are doing is adding or subtracting to make this work.

So, what if we did this?

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
    if(x <= 800)
    {
        x+=7;
    }
    else
    {
        x-=7;
    }
    
}
```

Does this work?  What did you see?  Why did it just wiggle?  It actually did go back 7 pixels but then when the draw was called again, it was less than or equal to 800 and then it tries to go to the right and then it does this little dance over and over.  How can we make it work?

Instead of trying to just add or subject directly. What if we added all the time, but don't focus on the adding, but rather, what we are adding.  We are going to make a couple of changes.  Check out this code.

```html

var red = 123;
var green = 39;
var blue = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement = 7;

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
    if(x <= 800)
    {
       
    }
    
     x+=movement;
}
```

If you run this code, it will work just as did before where the circles will continue forever.  Notice, I created a new variable **movement** and added that insted of 7.  What about the if statement?  Here is where the magic is going to happen.

```html

var red = 123;
var green = 39;
var blue = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement = 7;

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
    if(x >= 800)
    {
       movement*=-1;
    }
    
     x += movement;
}
```

Did you notice the changes?  I did two things.  I switched the direction of the relational  operator from less than or equal to and made it greater than or equal to.  The second thing I did was multiple movement by -1.  Why would I do that.  Okay this break it down.

```html
    if(x >= 800)
    {

    }

    x += movement;
```

I changed this part so that the code in the if statement happens when I am equal to or beyond my right border.  What happens in there?  Now, the big reveal.

```html

    movement *= -1;

```

This is where the magic happens.  This is where the movement gets multiplied by negative 1. After that happens, movement is added back to the x variable.  However, now movement is -7 and movement doesn't get multiplied by -1 again because x is not greater or equal to 800.

Cool right?  However, what about the other side?  Do you think you can do it?


