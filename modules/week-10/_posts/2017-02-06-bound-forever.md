---
title: Bounce Forever
module: 10
jotted: true
---

# Bounce Forever

We made the circles come back from the right side, but what if we want them to continue forever?  We have to make switch direction when it hits the left side.

Let's start where we left off.

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

What is the condition for which we want to check?  It should be when we are less than or equal to zero.  Why?  That is our left side.  What?!!

So, we could do what we did before.

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
       movement *= -1;
    }
    if(x <= 0)
    {
        movement *= -1;
    }
    
     x += movement;
}
```

Does it work?  Yeah!  Wait though... something feels a little off.  See how there is duplicated code?  We don't want that right?  How do we make that better?

We are going to introduce what is called **Logical Operators**.  There are three of them, **AND**, **OR**, and **NOT**.  In code, they look like this **&&** for AND, **||** for OR and **!** for NOT.

In order to combine the previous if statements, we have to think about this in English again.  When do we need movement to switch directions.  We can say if the circle is greater than or equal to 800 or if the circle is less than or equal to zero.  Wait!  Did you see the key word?  **OR**.  Since we know what symbols to use, we can write the code above to look like this.

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
    if(x >= 800 || x <= 0)
    {
       movement *= -1;
    }

     x += movement;
}
```
Doesn't that make you feel better? It makes me feel better.  Now the duplicated code is gone.  We want to reduce duplicated code so that if we need to make a change, we only have to change it one place.

If you look at the if statement with the OR in it, only one of those conditions has to be true and then movement is multiplied by -1.  If it's going to the right, it will be multiplied by -1 to make 7 become -7.  If it's moving to the left and we get to zero or below zero, movement is again multiplied by negative 1 and now movement goes from -7 to 7.  Pretty cool right?

The circles should go back and forth forever.  If you want the circles to only hit the edge, and not go beyond, you will need to do something to the if statement.  Do you think you can figure that part out?  I will leave that to you.

What math functions are out there that we can use?  Continue on and find out!