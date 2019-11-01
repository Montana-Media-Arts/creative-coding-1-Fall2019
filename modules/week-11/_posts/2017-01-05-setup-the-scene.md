---
title: Setup the Scene
module: 11
jotted: false
---

# Setup the Scene

I find in programming that often is it is useful to have some context indicating why I am creating something.  That is why  I had you create a self-portrait. Now, we are going to create some interactive art using events.

Have any of you played Spore?  Let's make something like that.  (minus the nicer graphics). We will use simple shapes to reduce the complexity.

First, let's setup our scene.

```html
    var x = 50;
    var y = 50;
    var diameter = 25;
    void setup()
    {
        createCanvas(800,600);
    }
    void draw()
    {
        background(0);
        fill(24,200,29);
        circle(x,y,diameter);
    }
```

Here we just created a simple black background and added a greenish circle to it.

We know how to make it move right?

```html
    var x = 50;
    var y = 50;
    var diameter = 25;
    void setup()
    {
        createCanvas(800,600);
    }
    void draw()
    {
        background(0);
        fill(24,200,29);
        circle(x,y,diameter);
        x+=10;
    }
```

That moves our circle to the right because we are adding to x.  Remember that x,y and diameter are variables.  We are just changing (or can change) the values stored in those variables which makes them really useful.  Yes?  Good!

Hopefully you also found out that if you change x and y and diameter at the same time, some really interesting things happen.  This will be the starting point for this week.

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
        x+=10;
        y+=3;
        diameter+=8;
    }
```

Fun! Where do we go from here? Let's talk about conditions.  What are those? if, if/else and if/else if statements.  We have seen the first two, but maybe not the third one. We will look at those.