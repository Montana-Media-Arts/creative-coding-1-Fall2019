---
title: Accessing HTML Tags
module: 8
jotted: true
---

# Accessing HTML Tags

One of the most useful things that JavaScript can do is access HTML tags and change their content.  Look at the example below to see how that is done.

```js
    document.getElementById("myTag").innerHTML = "New Text";
```
If you were to have an HTML page like the following, the JavaScript above would change the tag that has the id "myTag".

```html
    <html>
        <body>
            <span id="myTag">This is my favorite text</span>
        </body>
    </html>
```

So, where does it go?

Remember where we put the style tags?  Yes?  Those went in the head.  JavaScript can also go in the head.

The tricky part though is that HTML is read from top to bottom.  So, if you put the JavaScript from above in the head as is, it won't find the span tag because it doesn't exist yet!  Oh no!

So, we have to do something like this.

```html
    <html>
        <body>
            <span id="myTag">This is my favorite text</span>
        </body>

        <script>
             document.getElementById("myTag").innerHTML = "New Text";
        </script>
    </html>
```

Now, the span tag is created and then the JavaScript line will go through and update the text so that it says "ew Text".  Try it and see if you get that too.

What is we make a mistake though? Remember earlier when I said if you forget a semi-colon, things could go bad. What if we don't get the capitalization correct or what if spell something wrong?

Try that.  Put this into your web page.

```html
    <html>
        <body>
            <span id="myTag">This is my favorite text</span>
        </body>

        <script>
             dcument.getElementById("myTag").innerHTML = "New Text";
        </script>
    </html>
```

Open your web page.  What do you see?  Does it help you determine what went wrong?  There is a fix for this.  It's in the browser settings.  To access those in Chrome follow these steps.

1. Click on the three verticl dots in the upper right hand corner.
2. Navigate to **More Tools**->**Developer Tools**
3. Click on the console tab. This shows you the error and where it is in your code.  Nice!


We can also use another command to write to the console.  It's called console.log.

Try this now.

```html
    <html>
        <body>
            <span id="myTag">This is my favorite text</span>
        </body>

        <script>
             console.log("I am in the console!");
        </script>
    </html>
```

Open your web page. It won't show anything in the page. However, if you go to the console in the Developer Tools again, you will see the message from the console.log.  This is a nice way to find out what is happening in your JavaScript code.

Next, let's talk about variables in JavaScript.

<!-- video -->