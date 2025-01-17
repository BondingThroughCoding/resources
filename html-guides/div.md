---
layout: default
title: Heading Tag Guide
---

# Understanding the `<div>` Tag: The Box That Organizes Your Webpage

The `<div>` tag is one of the most useful tools in HTML! It’s like a container or a box that you can use to group content together and organize your webpage.

## What is the `<div>` Tag?

The `<div>` tag is short for "division." It’s used to divide your webpage into sections. You can use it to group related content together so you can style or organize it easily. Think of it as putting things into boxes to keep them neat!

### Why use `<div>`?

- **To group content** – You can wrap related elements, like text and images, into one section.
- **To apply styles** – By adding a class or ID to a `<div>`, you can style the entire section using CSS.
- **To layout your webpage** – You can create columns, sections, and more by using `<div>` tags.

### Example:
```html
<div class="container">
  <h1>Welcome to My Webpage</h1>
  <p>This is the main section of my webpage.</p>
</div>
```


In this example:

- The <div> groups the heading (<h1>) and the paragraph (<p>) together.
- A class called "container" is added to the <div>, which you can style with CSS.

### Styling with CSS:

You can use CSS to make the <div> look awesome! For example:
```html
<head>
  <style>
    .container {
      border: 2px solid blue;
      padding: 20px;
      background-color: lightyellow;
    }
  </style>
</head>
...
<body>
  <div class="container">
    <h1>Welcome to My Webpage</h1>
    <p>This is the main section of my webpage.</p>
  </div>
</body>
```
<h1>Welcome to My Webpage</h1>
<p>This is the main section of my webpage.</p>