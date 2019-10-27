---
title: Bounce Forever
module: 10
jotted: true
---

# Bounce Forever

We made the circles come back from the right side, but what if we want them to continue forever?  We have to make the circle switch directions when it hits the left side.

Let's start where we left off.

```html

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement = 13;
// this function is called only once
function setup()
{

    createCanvas(800,600);
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    fill(255);
    circle(x,y,diameter);
    fill(redColor,greenColor,blueColor);
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

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement = 13;
// this function is called only once
function setup()
{

    createCanvas(800,600);
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    fill(255);
    circle(x,y,diameter);
    fill(redColor,greenColor,blueColor);
    circle(x,y,25);
    if(x >= 800)
    {
       movement*=-1;
    }
    if(x <= 0)
    {
        movement *= -1;
    }
     x += movement;
}
```

Does it work?  Yeah!  Wait, though. Something feels a little off.  See how there is a duplicated section of code?  We don't want that.  How do we make that better?

We are going to introduce what is called **Logical Operators**.  There are three of them, **AND**, **OR**, and **NOT**.  In code, they look like this **&&** for AND, **||** for OR and **!** for NOT. Remember NOT?  We did that earlier. Yes!

To combine the previous if statements, we have to think about this in English again.  When do we need movement to switch directions?  We can say if the circle is greater than or equal to 800 or if the circle is less than or equal to zero.  Wait!  Did you see the keyword?  **OR**.  Since we know what symbols to use, we can write the code above to look like this.

```html

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement = 13;
// this function is called only once
function setup()
{

    createCanvas(800,600);
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    fill(255);
    circle(x,y,diameter);
    fill(redColor,greenColor,blueColor);
    circle(x,y,25);
    if(x >= 800 || x <= 0)
    {
       movement *= -1;
    }

     x += movement;
}
```

Doesn't that make you feel better? It makes me feel better.  Now the duplicated code is gone.  We want to reduce duplicated code so that if we need to make a change, we only have to change it in one place.

If you look at the if statement with the OR symbol in it, only one of those conditions must be true.  When meeting one of the conditions, then movement is multiplied by -1.  If it's going to the right, it will be multiplied by -1 to make 7 become -7.  If it's moving to the left and we get to zero or below zero, multiplying negative one to movement causes the value to go from -7 to 7.  Pretty cool, right?

The circles should go back and forth forever.  If you want only the edge of the circles to hit the screen border, change the if statement.  Do you think you can figure that part out?  I think you can!

What math functions are out there that we can use?  Continue and find out!