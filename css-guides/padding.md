--- 
layout: default
title: Padding Guide
author: Caitlyn Muscat
---

# Padding

`padding` is like `margin`’s younger sibling - it makes space around the content, but inside of the border. Padding can use percentages or pixels to provide a measurement. Once again, this can be really useful to add some extra space to the content in the page. Heres a visual of what padding looks like: 

<!-- put visual here -->

## Example

If I wanted to add some space to the padding around a paragraph of text on my webpage, it would look something like this: 

```css
p {
    padding: 10px; 
}
```

A neat feature of padding is that I can specify what part of the padding (top, right, bottom, left) I want to change. So the design I've demonstrated above, can also look like this!

```css
p { 
    padding-top: 10px; 
    padding-left: 10px; 
    padding-bottom: 10px;
    padding-right: 10px; 
}
```

If you want to know more about the `padding` feature, you can go to the links at [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) or [w3schools](https://www.w3schools.com/css/css_padding.asp). Both of these sites give excellent examples of how the padding property works, with plenty of examples on how to use it, and how the feature looks on a website. 