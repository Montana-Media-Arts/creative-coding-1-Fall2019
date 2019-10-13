---
title: Functions
module: 8
jotted: false
---

# Functions

If you recall when we changed the text in the span tag, we had to put the JavaScript script at the bottom so that it wouldn't give us an error.

What if we wanted to make it so that the JavaScript code didn't run automatically.  Insert **functions**.  You have seen them already.  You used them with **alert**, **log**, **write**, **getElementById**.  Now we are going to create one ourselves. 

Functions look like this.

```html
    function myFunction()
    {
        window.alert("Hi there!");
    }
```

We just created a function called **myFunction** and it contains one line of code which just so happens to be another window.alert.  However, it will not run unless we call myFunction somewhere.

One thing you might notice is that there are **{}** before and after the window.alert.  These indicate where the function body begins and ends.  Without them, the function doesn't work.

What does this look like in a full page?

```html
<html>
        <title>Variables</title>
        <head>
            <script>
                function displayFavoriteColor()
                {
                    var favoriteColor = "blue";
                    document.getElementById("myTag").innerHTML = "Favorite Color " + favoriteColor;
                }
                
            </script>
        </head>
        <body>
            <span id="myTag">This is my favorite text</span>
        </body>
    </html>
```

When you open this page. You should see just the original text since the function was never called.  How do we call this function.  Below is one way.

```html
<html>
        <title>Variables</title>
        <head>
            <script>
                function displayFavoriteColor()
                {
                    var favoriteColor = "blue";
                    document.getElementById("myTag").innerHTML = "Favorite Color " + favoriteColor;
                }
                
            </script>
        </head>
        <body onload="displayFavoriteColor();">
            <span id="myTag">This is my favorite text</span>
        </body>
    </html>
```

The function is called in the **onload** event of the body.  This event is just a special attribute of the body and allows us to call JavaScript functions.  Neat huh?

Now the text should be changed right when you open the page.

This is all fine and dandy, but what about getting information from a form or something like that? Move on and you will find out!