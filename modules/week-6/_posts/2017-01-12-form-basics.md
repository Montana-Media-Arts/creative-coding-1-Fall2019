---
title: HTML Forms
module: 6
jotted: true
---

# HTML Forms

What are HTML forms?  Well, if you have ever purchased anything online or filled out an application online or signed up for an email, your social media account or more, you have filled out a form.  Forms are just a way for us to gather data from the end-user.  Keep in mind there are some principles to which we should adhere.

First, we want to adhere to standards. Use the component for their intended use.  Use checkboxes for multiple selections and radio buttons for various choices, but only one correct one.

Aso, use dropdown lists, use those to control the input gathered.  We are going to first focus on creating forms and what tags are required. Then, we will add a look and feel to them and add a little functionality to them.

Here is an example of a simple form.

```html
<html>
    <title>My first page</title>
    <body>
        
        <form action="nextPage.html" type="Post">
            First Name: <input type="fName"><br>
            Last Name: <input type="lName"><br>
            <button id="mySubmit">Submit</button>
        </form>
    </body>
</htmL>

```

Look what we did here!  We created a basic yet pretty bland form!  So, challenge yourself to add more fields. Did it work?  Great!


<div id="jotted-demo-1" class="jotted-theme-stacked"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-1"), {
    files: [
        {
            type: "js",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/120_CreativeCoding/master/lecture_code/06/07_map_01/sketch.js"
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

