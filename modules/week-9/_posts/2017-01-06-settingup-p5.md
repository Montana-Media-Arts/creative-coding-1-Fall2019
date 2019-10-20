---
title: Using p5
module: 9
jotted: true
---

# Using p5.js

Using p5, we have a few options in which we can implement and use this library.

## Web Editor

The first way is by using the web editor on the p5js.org website.  Look for the button the home page that says **Start creating with the p5 Editor**

![Start Creating](../imgs/start.png "Start Creating")

Then, you can create sketches directly in the web, which is fantastic!  However, you need to be online for this to work.

Here is what the editor looks like.

![Editor](../imgs/editor.png "Editor")

If you click the start button, you won't see much but a 400x400 grey colored square.  If you change the numbers, you will see a different sized square if you change the create canvas numbers **Try it!**.  

If you change the number in the background, it will change the greyscale color.  You can put RGB colors in there too.  **Try it!**

What other options do we have though?  

## CDN

Remember when we used a CDN with Bootstrap?  You can do the same thing here.  It looks like this.

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.10.2/p5.js"></script>
```

How does this work in an html page?

```html
<html>
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.10.2/p5.js"></script>
    <script src="sketch.js"></script>
  </head>
  <body>
  </body>
</html>
```

Now, you may be saying, wait...from where did that sketch.js file come? And where is it located?

Here's the deal.  The sketch.js file is your file and it's located in the same director or folder as our html page.  It allows us to put all our p5.js code in a file we create and then we don't have to change our html page again.  It just makes things a little cleaner to read.

What might that file look like?

```html
function setup() {
  createCanvas(400,400);
}

function draw() {
  background(220);
}
```

Look familiar?  It should! It is the same code as what we say in the web editor. However, what was it with CDN's?  It means that we still have to be online.  So, what can we do to ensure that we can work on p5.js offline?

## Offline

We can download the library and then reference it.  What does that look like?

You can go to the download page and choose from a couple of options.

[Download page](https://p5js.org/download/)

If you look, you should see this.

![Download](../imgs/download.png "Download")

You have a couple of options, but if you right-click and download the p5.js or p5.min.js and then put that into a script tag, you will have an offline solution.  Here is what that looks like if you save the file in the same directory in the same place as your html file.

```html
<script src="p5.min.js"></script>
```

Where do we go from here? Now, that we have our initial set up done, we can focus on the setup and the draw.