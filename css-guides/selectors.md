--- 
layout: default
title: Selectors Guide
---

# Selectors

Selectors are used to determine what you want to change. This allows you to design specific aspects of your page in any way you want, without changing any of the HTML. 


## Examples 

To change the text color of our paragraphs, we can use selectors like this: 

```

p {
    color: blue; 
}

```

The curly braces `{}` are used to 'hold' whatever CSS rules we want to apply to the paragraph, which, in this example, is denoted by `p`. Don't forget to put the `;` at the end of your properties, otherwise your code won't work!

I can also list multiple HTML sections that I want to style. It will look a bit like this: 

```
h1, h2, p {
    color: red; 
}

```