---
title: Basic Structure of CSS
module: 7
jotted: false
---

# Basic Structure of CSS

In it's most basic form, CSS looks like this.

![selector](../imgs/selector.gif)

These are described as follows.

1. The selector points to the HTML element you want to style.

2. The declaration block contains one or more declarations separated by semicolons.

3. Each declaration includes a CSS property name and a value, separated by a colon.

4. A CSS declaration always ends with a semicolon, and declaration blocks are surrounded by curly braces. 

source - w3schools.com

For example, you might have a style that looks like this.

```html
body {
  bgcolor: pink;
  text-align: center;
}
```

1. body is the **selector**
2. bgcolor and text-align are part of the **declaration**.  Their part is the **CSS property name** and are located in the **declaration block** They are separated by a semi-colon **important!** and the declaration block is surrounded by **{ }** braces.
3. Finally, **pink** and **center** are also part of the **declaration** but are the **values** of the properties.

<!-- video -->