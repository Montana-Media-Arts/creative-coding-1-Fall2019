---
title: Adding Text
module: 9
jotted: false
---

# Adding Text

Adding text on the your page is not too difficult.  We have to use the text function.  It looks like this.

```html
function setup() {
  createCanvas(400,400);
}

function draw() {
    background(220);
    text('Hello there!', 10, 30);
}
```

This prints the words **Hello there!** to the screen at location x-location 10 and y-location 30.

Notice how it's not too big though?  We can change the size of the font, but using the textSize function.  It looks like this.

```html
function setup() {
  createCanvas(400,400);
}

function draw() {
    background(220);
    textSize(32);
    text('Hello there!', 10, 30);
}
```

Now, you see that the text is much larger and readable.. well at least for me since I cannot see that well. Okay, now you are ready for your homework!