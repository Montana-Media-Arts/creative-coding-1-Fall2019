---
title: Setup and Draw
module: 9
jotted: true
---

# Setup and Draw

These are the two main functions in p5.js.  They are the most important and are built into this library.

## function setup()

The setup function is the first function called and is called only once.  createCanvas is another built-in function that sets up the main window that allows us to draw.

It looks like this.

```html
    createCanvas(300,500);
```

There are some important things to notice. Hopefully, the look isn't  too mysterious. **createCanvas** is the name of the function.  We know it's a function because of the **()** and the first **parameter**, **300** is the width, while the second parameter, **500** is the height and then, don't forget the **;** semicolon.

To make the canvas appear, add the createCanvas to setup function.  It looks like this.

```html
    function setup()
    {
        createCanvas(300,500);
    }
```

Why do we put the createCanvas function in the setup? We only want to create the canvas one time.

Give this a try and see what it looks like.

Did you get a canvas appear in your web browser? Good!

## function draw()

What about the draw function?  What makes it so special?  We know that setup is called only once when the script runs, but with draw, it is called continously.

What have we seen so far? We have done this.

```html
function draw()
{
    background(220);
}
```

If the background is called repeatedly, then the background is called over and over.  How can we tell though? Remember when talked about writing information to the screen?  We can write to the console.log to prove that the draw is called multiple times.  Let's try it.

```html
function draw()
{
    background(220);
    console.log("hi");
}
```

Open your Developer Options and see what it says in the console?

What did you see?

Now, let's actually do something fun on the screen.
