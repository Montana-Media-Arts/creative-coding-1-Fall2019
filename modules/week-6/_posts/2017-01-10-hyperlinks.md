---
title: Hyperlinks and Images
module: 6
jotted: true
---

# Hyperlinks and Images

## Hyperlinks

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

Keep in mind that you have to have two pages named *secondpage.html* and *firstpage.html* respectively.


<!-- video -->

## Images

If you want to make images appear and they are on your computer, make sure you have a folder for all your .html files and your `.png, .jpg, .gif` files.  Then, you can reference your images directly without a path.  If you create an images folder inside of your main folder, you may have to do something like this.

```html
<html>
    <title>My first page</title>
    <body>
        <img src="../images/myimage.jpg">
    </body>
</htmL>

```

Did you see the `..`?  That tells the computer to go up a directory and then look into the images folder for your file.  It should work in a file you create as long as everything is in the same folder.  Watch the video below for more information.

<!-- video -->

