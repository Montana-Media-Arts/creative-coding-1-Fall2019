---
title: More form elements
module: 6
jotted: true
---

# More form elements

<!-- dropdowns -->

One of the most common form elements is the drop-down list.  It looks something like this.

```html
<select>
  <option value="apples">Apples</option>
  <option value="oranges">Oranges</option>
  <option value="grapes">Grapes</option>
  <option value="pineapple">Pineapple</option>
</select>
```
These allow us to restrict what the user can choose and helps us make sure we get data exactly the way we want it. If we use a text box for everything, then our users could type anything they wanted.  For example, they might say `Apple`, or `aPpple`, or `APPLE` and that would be bad.

<!-- video -->

<!-- radio -->
What other items can you find in forms?  I spoke of radio buttons and checkboxes in an earlier section.  How would you implement a radio button list?

```html
<input type="radio" name="color" value="blue">Blue<br>
<input type="radio" name="color" value="red">Red<br>
<input type="radio" name="color" value="green">Green<br>
<input type="radio" name="color" value="purple">Purple
```
<!-- video -->

<!-- checkboxes -->
Finally, let's look at checkboxes and the role they play in forms.  They allow us to select multiple items in a list.  We see these most often when a form asks us what our interests are.  It may look something like this.

```html
<h2>What kind of bikes do you like?</h2>
<input type="checkbox" name="mountain" value="mountain">Mountain<br>
<input type="checkbox" name="road" value="road">Road<br>
<input type="checkbox" name="cross" value="cross" checked>Cross<br>
<input type="checkbox" name="fattire" value="fattire" checked>Fat Tire<br>
<input type="checkbox" name="gravel" value="gravel" checked>Gravel<br>
```

Feel free to experiment with these.

<a href='http://www.silverleaf-consulting.com/CodeEditor/' target="_new">Click here for an Interactive HTML editor</a>

<!-- video -->

Next, let's incorporate some of these items into our homework.