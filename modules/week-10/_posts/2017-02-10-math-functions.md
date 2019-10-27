---
title: Math functions
module: 10
jotted: false
---

# Math functions

So, what is the Math function that we used before?  Random right?  When we wanted a random number, it looked like this.

```html
    number1 = Math.floor(Math.random() * 10);
```

Remember, the Math.random() returns a number between 0 inclusive and 1 exclusive. That means that it goes all way up to .99999999 but never gets to 1.  That is why we multiply it by some number and then use another Math function called floor, which returns the largest integer that is less than or equal to the number returned.  

For example, if you have the following.

```html
    Console.log(Math.floor(3.03));
```

You will see 3.

If you the following.

```html
    Console.log(Math.floor(3.94));
```

You will also see 3.

So, we are getting a random number between 0 and 1 multiplying the number by ten, and then we get the floor to return an integer that will become our random number.

How can we use it in our previous code?

Let's start with where we left off.

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

This time though, let's assign movement a random value.  To do that, we are going to assign it inside the setup function.  Now the code looks like this.

```html

var red = 123;
var green = 39;
var blue = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement;

function setup()
{
    createCanvas(800,600);
    movement = Math.floor(Math.random() * 10);
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

Now, movement will be a variable speed between 0 and 9 because Math.random could return 0.  Then, if we multiply by 10, it will still be zero.  Then, if we take the floor of that, it will always be zero. Uh oh. What if I want to have at least some speed?

Let's change our code one more time.

```html

var red = 123;
var green = 39;
var blue = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement;

function setup()
{
    createCanvas(800,600);
    movement = Math.floor(Math.random() * 10) + 1;
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

If you look at our random statement, I now add at least 1 to it.  So, if I get a zero, it will be assigned a 1, and now our range is between 1 and 10.  Try and see if it works!

There are so many more math functions at your disposal in p5.js.  Here is the link to them.  Try them out.

[p5.js Math Functions](https://p5js.org/reference/#group-Math)

With that, let's talk about homework for this week.