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
{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>HTML Demo: &#96;&lt;div&#96;&gt;</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<h1>Heading 1: Largest and Most Important</h1>
<h2>Heading 2: Slightly Smaller</h2>
<h3>Heading 3: Medium Size</h3>
<h4>Heading 4: Smaller Heading</h4>
<h5>Heading 5: Even Smaller</h5>
<h6>Heading 6: Smallest Heading</h6>
<style>
  h1 {color: red;}
  h2 {color: blue;}
  h3 {color: green;}
  h4 {color: orange;}
  h5 {color: purple;}
  h6 {color: black;}
</style></textarea>
    <iframe id="preview" style=" border: none;"></iframe>
  </div>
</div>

  <script>
    // Initialize CodeMirror
    var editor = CodeMirror.fromTextArea(document.getElementById('code'), {
      mode: 'xml',  // HTML, CSS, and JavaScript combined mode
      lineNumbers: true,  // Show line numbers
      theme: 'dracula',   // Theme of your choice
      matchBrackets: true // Highlight matching brackets
    });
    function updatePreview() {
      var iframe = document.getElementById('preview');
      var content = editor.getValue();  // Get the content from the editor
      var doc = iframe.contentWindow.document;

      // Write content to the iframe
      doc.open();
      doc.write(content);
      doc.close();
    }

    // Update the preview whenever the content in the editor changes
    editor.on('change', function() {
      updatePreview();
    });

    // Initial preview update
    updatePreview();

  </script>

{% endraw %}  

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