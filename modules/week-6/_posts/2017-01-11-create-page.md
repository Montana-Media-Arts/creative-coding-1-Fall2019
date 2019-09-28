---
title: Create a page
module: 6
jotted: true
---

# Create a page

I am so excited that you made it this far!  You are learning the basics of HTML well. One crucial step is to learn how to create and save it to view the page in a browser.

You have a couple of options:

1. If you have Visual Studio Code installed
   1. Choose File -> New File
   2. Add your HTML code (refer back to the previous sections if you need a sample)
   3. Choose File -> Save
   4. Once the dialog appears, type in your name and then, put `.html`  This extension tells your computer to use your default web browser to open this file. 
2. If you have Atom, Notepad, Notepad++, or any other editing program, you can do the essentially the same thing.  Just remember to save it with the `.html` extension and it should work.

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

Next up, we are going to take a look at HTML forms.  What are those?  I bet you have used these a lot!