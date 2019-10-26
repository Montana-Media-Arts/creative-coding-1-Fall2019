---
title: Making Shapes Stop
module: 10
jotted: true
---

# Making Shapes Stop

Last time, we left off with this.

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

Now, we have to make the shapes stop.  But how?

This where we come back to our **conditional** statements.

What was the one that we used the most in our math game? I hope you don't have bad dreams about that still.

If we think about it in English, we want the circles to move until we hit the right side of the wall.  Where is the right side of the wall?  If we look at the createCanvas, it tells us.

It is the width.  Which one is that?  Is it the **800** or the **600**?

... It is the **800**, you are correct!

So, how does this look?

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
    if(x < 800)
    {
        x++;
    }
    
}
```

What happened above? I created an if statement and said, if it is less than 800 than continue moving, otherwise, the if statement will be false and the x will no longer get bigger.  If you want to make it go faster then, do this.  Keep in mind that **<** sign is called a relational operator. The opposite is **>** and stands for greater than.

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
    if(x < 800)
    {
        x+=10;
    }
    
}
```

I could have done this too right?

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
    if(x == 800)
    {
        x+=10;
    }
    
}
```

Run this.  Does it still work?  Why?

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
    if(x == 800)
    {
        x+=7;
    }
    
}
```

How about now?  Why or why not? 

Remember in the preceding if statement, it has to equal exactly 800 for it to stop. Otherwise, it will continue.  The **==** is the equality operator whereas the **=** is the assignment operator.  Be careful of that one!

But I do want the circle to move all the way to the end. If stay strictly less than, then it won't get there.  So, I will combine both the two together like this using another relational operator **<=** which means less than or equal to.  The opposite being **>=** or greater than or equal to.

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
Now it works.  Whew!

