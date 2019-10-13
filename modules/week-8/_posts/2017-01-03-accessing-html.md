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

Now, the span tag is created and then the JavaScript line will go through and update the text so that it says "New Text".  Try it and see if you get that too.

<div id="jotted-demo-1" class="jotted-theme-stacked"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-1"), {
    files: [
        {
            type: "html",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/441-WebTech/master/lecture_code/02/01/01_js_in_html.html"
        }
    ],
    showBlank: false,
    showResult: false,
    runScripts: true,
    plugins: [
        { name: 'ace', options: { "maxLines": 50 } },
        // { name: 'console', options: { autoClear: true } },
    ]
});
</script>
