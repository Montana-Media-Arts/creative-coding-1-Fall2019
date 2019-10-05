---
title: Class Selectors
module: 7
jotted: true
---

# Class Selectors

In the previous section, we added styles by using inline styles, embedded styles and external style sheets.  

In our styles, we were general to all span tags.  However, what if we wanted to find a specific tag or apply a style to a number of different tags?  That is where we uses classes and ID's in style.  We will use style sheets from now on.

Here's an example of an HTML page.

```html
    <html>
        <title>Class Example</title>
        <head>
            <link rel="stylesheet" type="text/css" href="mainstyle.css">
        </head>
        <body>
            <span class="blueColor">New Color</span>
            <br>
            <span>Same Color</span>
            <br>
            <a href="http://www.amazon.com" class="blueColor">Amazon</a>
        </body>
    </html>
```

```html
    .blueColor{
        text-color:blue;
        text-family:arial;
        text-size:24px;
    }
```

Notice in this example, the CSS has a name `.blueColor`.  This applies the blue color, changes the font type and the size of the `span` tag and an `a` (anchor) tag.  They both turned blue while the other span tag without the class name did not.

We can get even more specific by doing something like this.

```html
    span.blueColor{
        text-color:blue;
        text-family:arial;
        text-size:24px;
    }
```

Now, only span tags with the class `blueColor` will change.  No other tags will work.

<!-- video -->


