--- 
layout: default
title: Selectors Guide
author: Caitlyn Muscat
---

# Attribute Selectors

Attrubute Selectors are used to determine what you want to change. This allows you to design specific aspects of your page in any way you want, without changing any of the HTML. 


## Examples 

To change the text color of our paragraphs, we can use attribute selectors like this: 

```css
p {
    color: blue; 
}
```

The curly braces `{}` are used to 'hold' whatever CSS rules we want to apply to the paragraph, which, in this example, is denoted by `p`. Don't forget to put the `;` at the end of your properties, otherwise your code won't work!

I can also list multiple HTML sections that I want to style. It will look a bit like this: 

```css
h1, h2, p {
    color: red; 
}
```

If you want to know more about the `Attribute Selectors` feature, you can go to the links at [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors) or [w3schools](https://www.w3schools.com/css/css_attribute_selectors.asp). Both of these sites give excellent examples of how the attribute selector feature works, with plenty of examples on how to use them. 