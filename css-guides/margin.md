--- 
layout: default
title: Margin Guide
author: Caitlyn Muscat
---

# Margin

In CSS we can use `margin` to make space around the outside of the border of something. This can be the border of an image, or the border of a textbox. Margin can use percentages or pixels to provide a measurement. This is usually really useful for helping organise things on a page, or making a bit of space between the elements so the page is easier to read. Here's a visual of what a margin actually looks like: 

<!-- make a visual to put here -->

## Example

If I wanted to add some space around a paragraph of text on my webpage, it would look something like this: 

```css
p {
    margin: 10px; 
}
```

A neat feature of margin is that I can specify what part of the margin (top, right, bottom, left) I want to change. So the design I've demonstrated above, can also look like this!

```css
p { 
    margin-top: 10px; 
    margin-left: 10px; 
    margin-bottom: 10px;
    margin-right: 10px; 
}
```

If you want to know more about the `margin` feature, you can go to the links at [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) or [w3schools](https://www.w3schools.com/css/css_margin.asp). Both of these sites give excellent examples of how the margin property works, with plenty of examples on how to use it, and how the feature looks on a website. 