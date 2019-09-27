---
title: What is HTML?
module: 6
jotted: true
---

# HTML

I always find it userful to define what it is we are doing before we use it.  So what is HTML?

HTML stands for Hyper Text Markup Language

Is it an actual programming language?  No

It's a markup language which means it can be displayed a web browser, but it is not compiled. It's an important distinction because that means it doesn't go down to the machine code level. If you aren't completely convinced at this point, don't worry! I am just priming you for a later discussion.  Needless to say, just think of HTML as a way to make stuff show up in the browser.  So, let's try it out.  What does it look like?

```html
<html>

</html>
```

Notice the `<html>` starts with a `<` symbol and then ends with a `>` symbol.  The tag, in this case `html` goes between the two angle brackets.  Then, as you see, the tag always ends with `</html>`  This is called the closing tag.

So, move to the next section to see the basic structure.

<!-- video -->



Now, you try this below.  You can copy and paste the code into the section below, and see what it does.

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
