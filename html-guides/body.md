---
layout: default
title: "HTML Body Tag Guide"
---

# Understanding the `<body>` Tag: The Heart of Your Webpage

The `<body>` tag is where the main content of your webpage goes. It's everything your visitors see when they visit your site!

## What is the `<body>` Tag?

The `<body>` tag contains all the visible parts of the webpage. Everything that appears on the screen, from text and images to buttons and videos, lives inside the `<body>` tag. If you want people to see something on your page, you put it inside the `<body>`.

### Here's what goes inside the `<body>` tag:
- **Text** – Paragraphs, headings, lists, and other text content.
- **Images** – Pictures you want to show on the page.
- **Links** – Hyperlinks that take visitors to other pages.
- **Forms, Buttons, and Other Interactive Elements** – These let users interact with your page.

### Example:
```html
<body>
  <h1>Welcome to My Webpage!</h1>
  <p>This is where all the fun happens.</p>
  <img src="image.jpg" alt="A cool image">
  <a href="https://example.com">Visit my favorite website!</a>
</body>
```
{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>HTML Demo: &lt;h1&gt;-&lt;h6&gt;</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<div class="container">
  <h1>Welcome to My Webpage</h1>
  <p>This is the main section of my webpage.</p>
</div></textarea>
    <iframe id="preview" style=" border: none;"></iframe>
  </div>
</div>

  <script>
    var textarea = document.getElementById('code');
    var initialContent = textarea.value;
    
    document.querySelector('.reset-button').addEventListener('click', function() {
      editor.setValue(initialContent);
      updatePreview();
    });


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

### Why is it important?
The `<body>` tag is where the magic happens! Without it, there would be no visible content on your webpage. It's where you get to be creative and build the parts of your site that people interact with. Everything your users see, click, or read comes from inside the `<body>` tag.


