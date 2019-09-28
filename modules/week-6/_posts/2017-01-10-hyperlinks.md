---
title: Hyperlinks
module: 6
jotted: true
---

# Hyperlinks

Hyperlinks have been around since the beginning of HTML4 and continue today. They are the bedrock of web pages as they take us places.  They have a similar structure to image tags, and they look like this.

```html
<a href="mypage.html">Link to somewhere</a>
```

The `<a>` tag is called the anchor tag.  It tells us that there will be a link there.  The `href` is the attribute that indicates where you are going to go.  So in the previous instance, if we clicked on the *Link to somewhere*, it would take us to the *mypage.html* page.

So, how does the whole page look?

```html
<html>
    <title>My first page</title>
    <body>
        <a href="secondpage.html>Go to my other page</a>
    </body>
</htmL>

```

Whereas on the second page, you might have something that looks like this.

```html
<html>
    <title>My second page</title>
    <body>
        <a href="firstpage.html>Go to my first page</a>
    </body>
</htmL>

```

Keep in mind that you have to have two pages named *secondpage.html* and *firstpage.html* respectively.  How do we do that?  Continue, and I will show you!


<div id="jotted-demo-1" class="jotted-theme-stacked"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-1"), {
    files: [
        {
            type: "js",
            hide: false,
            url:""
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

