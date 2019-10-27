---
title: Variables
module: 10
jotted: true
---

# Variables

Wait a minute; we have already done this, right?  Yes! We did this in JavaScript.  Since p5.js is just a JavaScript library, we can create variables just the same.

For example, they might look like this.

```html
    var myFavoriteNumber = 42;
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
        background(120);
        console.log(myFavoriteNumber);
    }
```

What do you see?  Well, you won't see anything on the screen, but you will see the number in your console down below.

What if we want to do something with our variables?  We can add to our variables like this.

```html
    var myFavoriteNumber = 42;
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
        background(120);
        myFavoriteNumber++;
        console.log(myFavoriteNumber);
    }
```

Did you notice the change to **myFavoriteNumber**?  It gets incremented by 1.  It can be written like this too.

```html
    myFavoriteNumber = myFavoriteNumber + 1;
```

They both mean the same thing. First, the value of one gets added to the previous value of myFavoriteNumber, and then it is assigned back to myFavoriteNumber.  There are three ways in which we can do the same thing. Here are the different choices.

```html
    myFavoriteNumber++;
    myFavoriteNumber = myFavoriteNumber + 1;
    myFavoriteNumber += 1;
```

They all mean the same thing.  Keep in mind that **myFavoriteNumber++** only happens when incrementing by 1.  If you want to increase by another number, you can only use the latter two.

## Scope
Another thing to notice is how I declare **var myFavoriteNumber** above the setup() function.  That means it can be seen in the setup and draw functions as well as any other methods that we might define.

Declaring a variable inside of a method looks like this.

```html
    
    function doSomething()
    {
        var myFavoriteColor = "blue";
    }
    
```

This variable, **var myFavoriteColor** can be seen only in the doSomething() function.

You can also declare variables in loops like this.

```html
    for(var i = 0; i < 5; i++)
    {
        console.log(i);
    }
```

What this means is that the variable **i** will exist in the for loop, but when it terminates, the variable goes away.

Did you notice the difference between creating a variable like myFavoriteNumber compared to myFavoriteColor?  The first one contains a number while the second contains a string.  These differences are important to understand.  When declaring a number, you do not need double-quotes **""**. Conversely, if you declare a string, it needs to be in double-quotes.

```html
    var name = "John Cena";
    var age = 67;
```

What would a variable look like in our main sketch?

```html

var redColor = 123;
var greenColor = 39;
var blueColor = 21;
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
}
```

As you can see, the variables **redColor**, **greenColor**, and **blueColor** are **declared** at the top and then used in the **background** function in the draw function.  

If we change the variables in the draw function as we did earlier to our favorite number, we should see something exciting.  Try this sketch.

```html

var redColor = 123;
var greenColor = 39;
var blueColor = 21;
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
    redColor++;
    greenColor++;
    blueColor++;
}
```

Did you see something change?  Cool huh?  Let's continue.

<a href="https://umontana.zoom.us/recording/share/PZlDzWSN5QEWJeGrbYz1XnZTPBFOlfmqgQ-wc2bN3XSwIumekTziMw" target="_new" style="font-family:Ariel; font-size:32px;">Click here for this section's Video</a>