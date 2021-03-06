---
title: Making Shapes Stop
module: 10
jotted: true
---

# Making Shapes Stop

Last time, we left off with this.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
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
    x++;
}
```

Now, we have to make the shapes stop.  But how?

This where we come back to our **conditional** statements.

What was the one that we used the most in our math game? I hope you don't have bad dreams about that still.

If we think about it in English, we want the circles to move until we hit the right side of the wall.  Where is the right side of the screen border?  If we look at the createCanvas, it tells us.

It is the width.  Which one is that?  Is it the **800** or the **600**?

... It is the **800**, you are correct!

So, how does this look?

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
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
    if(x < 800)
    {
        x++;
    }
}
```

What happened above? I created an if statement and said if it is less than 800 than continue moving; otherwise, the if statement will be false, and the x will no longer get bigger.  If you want to make it go faster then, do this.  Keep in mind that **<** sign is called a relational operator. The opposite is **>** and stands for "greater than."

I could have done this, too, right?  Does this work? What are we doing? We use the **!** which means **NOT** equal in this case.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
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
    if(x != 800)
    {
        x+=10;
    }
}
```

Run this.  Does it still work?  Why?  

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
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
    if(x != 800)
    {
        x+=13;
    }
}
```

How about now?  Why or why not? 

Remember, in the preceding if statement, it has to equal precisely 800 for it to stop. Otherwise, it will continue.  The **!=** is the equality operator, whereas the **==** is the equality operator and **=** is the assignment operator.  Be careful of those different operators!

But I do want the circle to move to the end. If the code remains strictly less than, then it won't get to the end of the screen.  Fixing this problem requires combining both the relational and equality operator together.  Now the symbols look like this **<=**.  The two symbols together mean "less than or equal to."  The opposite being **>=** or "greater than or equal to."

```js
var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
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
    if(x <= 800)
    {
        x+=13;
    }
}

```
Now it works.  Whew!

<a href="https://umontana.zoom.us/recording/share/BmOT3ZrOfih8D_UU5RMm2AO1tzZIWEvRdbj4OKJg1SGwIumekTziMw" target="_new" style="font-family:Ariel; font-size:32px;">Click here for this section's Video</a>