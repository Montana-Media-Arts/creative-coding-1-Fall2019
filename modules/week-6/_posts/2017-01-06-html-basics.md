---
title: HTML Basics
module: 6
jotted: false
---

# HTML Basics


What other tags do we need to make stuff show up?

```html
<html>
    <body>
        <h1>My first website</h1>
        <p></p>
        My stuff is really important.
        <br>
        How do you like them apples?
    </body>
</html>

```

What are these tags?

1. body tag - this tag surrounds all the tags that are to show up in the web browser window.
2. h1 - this is a header tag. There are headers 1-6 where h1 is the largest and h6 is the smallest
3. p - the p tag creates paragraph breaks
4. br - the br tag creates a simple line break

Now, you try this below.  You can copy and paste the code into the section below, and see what it does.

<!-- video -->

<div id="jotted-demo-1" class="jotted-theme-stacked" height="150px;"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-1"), {
    files: [
        {
            type: "js",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/120_CreativeCoding/master/lecture_code/06/02_modulo_01/sketch.js"
        },
        {
            type: "html",
            hide: true,
            url:"../../../p5_resources/index.html"
        }
    ],
    showBlank: false,
    showResult: true,
    plugins: [
        { name: 'ace', options: { "maxLines": 50 } },
        // { name: 'console', options: { autoClear: true } },
    ]
});
</script>


