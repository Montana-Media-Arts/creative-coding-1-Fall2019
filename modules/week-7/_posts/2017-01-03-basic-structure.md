---
title: Basic Structure of CSS
module: 7
jotted: false
---

# Basic Structure of CSS

In its most basic form, CSS looks like this.

![selector](../imgs/selector.gif)

The description is as follows.

1. The selector points to the HTML element you want to style.

2. The declaration block contains one or more declarations separated by semicolons.

3. Each declaration includes a CSS property name and a value, separated by a colon.

4. End CSS declarations with a semicolon

5. Surround declaration blocks by curly braces

source - w3schools.com

For example, you might have a style that looks like this.

```html
body {
  bgcolor: pink;
  text-align: center;
}
```

1. body is the **selector**
2. bgcolor and text-align are part of the **declaration** and is the **CSS property name**.  The **declaration block** contains the declarations separated by a semicolons **important!**. The declaration block is surrounded by **{ }** braces.
3. Finally, **pink** and **center** are also part of the **declaration** but are the **values** of the properties.
<!-- video -->