---
title: Variables
module: 10
jotted: true
---

# Variables

wait a minute, we have already done this right?  Yes! We did thsi in JavaScript.  Since p5.js is just a JavaScript library we can create variables just the same.

For example, they might look like this.

```html
    var myFavoriteNumber = 42;
    function setup()
    {
        createCanvas(800,600);
    }
    
    function draw()
    {
        background(120);
        println(myFavoriteNumber);
    }
```

What do you see?  Well you won't see anything on the screen, but you will see the number in your console down below.

What if we want to do something with our variables?  We can add to our variables like this.

```html
    var myFavoriteNumber = 42;
    function setup()
    {
        createCanvas(800,600);
    }
    
    function draw()
    {
        background(120);
        myFavoriteNumber++;
        println(myFavoriteNumber);
    }
```

Did you notice the change to **myFavoriteNumber**?  It gets incremented by 1.  It can be written like this too.

```html
    myFavoriteNumber = myFavoriteNumber + 1;
```

They both mean the same thing. This is what is happening.  One is added to the previous value of myFavoriteNumber and then it is assigned back to myFavoriteNumber.  There are three ways in which we can do the same thing. Here is what they look like.

```html
    myFavoriteNumber++;
    myFavoriteNumber = myFavoriteNumber + 1;
    myFavoriteNumber += 1;
```

They all mean the same thing.  Keep in mind that **myFavoriteNumber++** only happens when incrementing by 1.  If you want to increase by another number, you can only use the latter two.

## Scope

Another thing to notice is that **var myFavoriteNumber** is declared above the setup() function.  That means it can be seen in the setup and draw functions as well as any other methods that we might define.

If we declare a variable inside of a method like this.

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
        println(i);
    }
```

What this means is that the variable **i** will exist in the for loop but when it terminates the variable goes awy.

Did you notice the difference between create a variable like myFavoriteNumber compared to myFavoriteColor.  The first one contained a number while the second contains a string.  This is important when declaring a number you do not need double-quotes **""** while if you declare a string, it needs to be in double-quotes.

```html
    var name = "John Cena";
    var age = 67;
```

What would a variable look like in our main sketch?

```html

var red = 123;
var green = 39;
var blue = 21;

function setup()
{

    createCanvas(800,600);
}

function draw()
{
    background(red,green,blue);

}
```

As you can see, the varibles **red**, **green**, and **blue** are **declared** at the top and then used in the **background** function in the draw function.  

If we change the variables in draw like we did earlier to our favorite number we should see something really interesting.  Try this sketch.

```html

var red = 123;
var green = 39;
var blue = 21;

function setup()
{

    createCanvas(800,600);
}

function draw()
{
    background(red,green,blue);
    red++;
    green++;
    blue++;
}
```

Did you see something change?  Cool huh?  Let's continue.