---
layout: default
title: "HTML Body Tag Guide"
---

# Understanding the `<link>` Tag: Connecting Your Webpage to the World

The `<link>` tag helps you connect your webpage to other resources, like stylesheets, icons, or external files. It's a special tag that doesn't display anything directly on your page, but it makes your page work and look better!

## What is the `<link>` Tag?

The `<link>` tag is used to connect your HTML document to other files. Most commonly, it links your webpage to a CSS stylesheet, which controls how your webpage looks. It can also be used to add icons or other resources that improve your page.

### Here's what you'll typically use the `<link>` tag for:
- **Linking to a CSS file** – This tells the webpage where to find the style rules for how things should look.
- **Adding a favicon** – The little icon that appears on the browser tab next to the title.
- **Connecting to other external resources** – Like web fonts or other files that your page needs.

### Example:
```html
<head>
  <link rel="stylesheet" href="styles.css">
  <link rel="icon" href="favicon.ico">
</head>
```
   In the example above:

- The first `<link>` connects to a CSS file (styles.css) that controls how the page looks.
- The second `<link>` adds a small icon (favicon.ico) that shows up in the browser tab.

### Why is it important?
The `<link>` tag is important because it allows you to connect your webpage to external resources like stylesheets and icons, which help make your page look amazing and work properly. Without the `<link>` tag, your webpage might look plain and not have the cool features you want!