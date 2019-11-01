---
title: Conditionals
module: 11
jotted: false
---


# Conditionals

These are control structures that help us make decisions when our code runs.

## if statements

These are the most basic conditional statements.  They always evaluate to something that is true or false.

```html
    if(3 == 5)
    { // opening curly brace
        // body of the if statement
        console.log("I am in the if statement");
    }// closing curly brace
```

In this if statements, if 3 equals 5 then, the body of the if runs.  In this instance, the console.log will not run. However, if we chane the if statement to something like this.


```html
    if(3 == 3)
    { // opening curly brace
        // body of the if statement
        console.log("I am in the if statement");
    }// closing curly brace
```

Then, the console.log runs.

Keep in mind, we want to use variables whenever we can.

You might want something like this.


```html
    if(a == b)
    { // opening curly brace
        // body of the if statement
        console.log("I am in the if statement");
    }// closing curly brace
```

Now, a could be 3 and b equal to 5. In that case, the if statement would fail and then the code skips the body if statement and runs the code. However, if a = 3 and b = 3, then it evaluations to true.

How do we apply this to our new example?

```html
    var x = 50;
    var y = 50;
    var diameter = 25;
    function setup()
    {
        createCanvas(800,600);
    }
    function draw()
    {
        background(0);
        fill(24,200,29);
        circle(x,y,diameter);
        if(x <= 300)
        {
            x+=10;
        }
        if(y <= 300)
        {
            y+=3;
        }
        if(diameter <= 300)
        {
            diameter+=8;
        }
        
    }
```

## if/else statements

We looked at this last week and it's good to revisit before we add more.  With if statements, we can also have the other case.  We can think of it like this.  If something is true, then do something (the thing in the curly braces under the if), **else** do something else (it will have its own curly braces).

The syntax looks like this.

```html
    var a = 5;
    var b = 3;
    
    if(a == b)
    {
        console.log("a equals b");
    }
    else
    {
        console.log("a does not equal b");
    }
```

How did we do it in our project?

```html
    var x = 50;
    var y = 50;
    var diameter = 25;
    function setup()
    {
        createCanvas(800,600);
    }
    function draw()
    {
        background(0);
        fill(24,200,29);
        circle(x,y,diameter);
        if(x <= 300)
        {
            x+=10;
        }
        else
        {
            x-=20;
        }
        if(y <= 300)
        {
            y+=3;
        }
        else
        {
            y-=6;
        }
        if(diameter <= 300)
        {
            diameter+=8;
        }
        else
        {
            diameter-=16;
        }
        
    }
```

Remember this behavior?  It looks a little funky right? It was when we were trying to get our shape to bounce and we just put in an else statement that said if we weren't greater than the width (or height), then subject.  That didn't work so we had to create a new variable that would multiply by a negative one to speed and then add that to the shape.  

So, how can we effectively use an if/else statement?

What if we did something like this.

```html
    var a = 5;
    var b = 3;
    
    if(a == b)
    {
        console.log("a equals b");
    }
    else
    {
        console.log("a does not equal b");
    }
```

How did we do it in our project?

```html
    var x = 50;
    var y = 50;
    var diameter = 25;
    function setup()
    {
        createCanvas(800,600);
    }
    function draw()
    {
        background(0);
        fill(24,200,29);
        circle(x,y,diameter);
        if(x <= 300)
        {
            x+=10;
        }
        else
        {
            x = 50;
        }
        if(y <= 300)
        {
            y+=3;
        }
        else
        {
            y = 50;
        }
        if(diameter <= 300)
        {
            diameter+=8;
        }
        else
        {
            diameter = 25;
        }
        
    }
```

Now that's more interesting right?  (or could cause a seizure depending your sensitivity).

What about else ifs?  What is that?

## if/else if

