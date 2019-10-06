---
title: ID Selectors
module: 7
jotted: true
---

# ID Selectors

Another way in which we can select a tag is by their ID if they have an id attribute defined. The HTML page might look like this.

```html
    <html>
        <title>Class Example</title>
        <head>
            <link rel="stylesheet" type="text/css" href="mainstyle.css">
        </head>
        <body>
            <span id="specificColor">New Color</span>
            <br>
            <span>Same Color</span>
            <br>
            <a href="http://www.amazon.com" id="specificLink">Amazon</a>
        </body>
    </html>
```

And the CSS might look like this.

```html
    #specificColor{
        color:blue;
        text-family:arial;
        text-size:24px;
    }

    #specificLink{
        color:red;
        text-family:arial;
        text-size:28px;
    }
```

This time, the color and the size of the text specific to the ID because of the `#`.

<!-- video -->