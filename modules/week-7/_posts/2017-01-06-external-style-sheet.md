---
title: External Style Sheets
module: 7
jotted: true
---

# Adding CSS to HTML

## External Style Sheets

The last way in which we can apply a style is through an **external** style sheet.

What does it look like?

**External Style Sheet**

```html
span{
    text-color:white;
    background-color:red;
}
```

Note that when you save this in a separate page, it has to be called something like `mainstyle.css`.  It always ends with a `.css` extension.

Now, we can apply assign it to a page like this.

```html
    <html>
        <title>External Style Sheet</title>
        <head>
            <link rel="stylesheet" type="text/css" href="mainstyle.css">
        </head>
    </html>
```

A couple of things to note.  The `rel` is the relationship attribute.  The `type` specifies the type of file.  Finally, the `href` which should look familar is where the file is located. Remember if it defined like it is above, it has to be in the same folder.  Otherwise, you need to add the correct path.

We use style sheets so that we can apply a style sheet to many pages.  Then, if we want to make a change, we can change it in one file and apply it everywhere.

So, when you have all three types of styles on your page, which style is applied?  It always goes in this order.

1. Inline styles first
2. Embedded
3. External
4. Browser

Yes, that's right the browser has it's own style sheet.  If you are interested, take a look around and you can find and change your brower's style sheet. Fun right?

<!-- video -->