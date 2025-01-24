--- 
layout: default
title: Border Guide
author: Caitlyn Muscat
---

# Border

`border` is a property that allows you to stylise the border of contents that have the border element. This means that you get to stylize the outlines of paragraphs, tables and images. It can have values of solid, dashed or dotted, just to name a few. Within the `border` property, there are some sub-elements that allow for further border design.

To find out more about `border`, you can visit the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/border) or [w3schools](https://www.w3schools.com/css/css_border.asp)

### Border Color 

`border-color` kinda just does what it sounds like it does - it changes the color of the border. You can give it multiple types of values, in fact, the same type of values you can give to the `color` property! These are words, like `white`, `blue` or `purple`, or they can be hex values, like `#ffffff` or `#000000`. You can also give them rgb values like rgb(255,255,255) or rgb(156,33, 72). 

To find out more about `border-color`, you can visit the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color) or [w3schools](https://www.w3schools.com/css/css_border_color.asp)

### Border Collapse

`border-collapse` is a bit of a different property. It's usually used for tables, and tells the CSS to either allow cells to share borders, or to keep the borders separate. If the borders are shared, then its just one line, but, if they arent shared, each cell has its own individual border. If you want to see a visual representation of this property, check out the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse) for `border-collapse`. 

If you'd like more details, you can also look at the [w3schools](https://www.w3schools.com/cssref/pr_border-collapse.php) page. 

### Border Width 

`border-width` is another element that sounds like what it does. It changes the width of the border around content like a paragraph or image, or within tables. We can give it `percentage` values, or `px` values, which is short for pixels. 

To find out more about `border-width`, you can visit the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width) or [w3schools](https://www.w3schools.com/cssref/pr_border-width.php)

## Example

If I wanted to write a bit of code that incorporated all of these properties, it might look something like this! 

```css
table {
    border: solid; 
    border-color: pink; 
    border-collapse: collapse; 
}

td {
    border: solid; 
    border-color: purple; 
}

tr, th {
    border: dotted; 
    border-color: yellow; 
    border-width: 5px; 
}
```


