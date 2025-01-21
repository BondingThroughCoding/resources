---
layout: default
title: Heading Tag Guide
---

# Understanding the `<h1>` to `<h6>` Tags: Creating Headings for Your Webpage

The `<h1>` to `<h6>` tags are used to create headings on your webpage. They help organize your content, making it easy to read and understand. Headings also tell search engines what your page is about!

## What are Heading Tags?

Headings are like titles or subtitles for different sections of your webpage. HTML gives you six levels of headings, from `<h1>` (the biggest and most important) to `<h6>` (the smallest and least important). Each level has a different size, which helps show the structure of your content.

### How They Look:

- **`<h1>`**: The largest and most important heading.
- **`<h2>`**: The second-largest heading, great for subsections.
- **`<h3>` to `<h6>`**: Smaller headings, used for further sub-sections or details.

### Example:
{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>HTML Demo: &#96;&lt;h1&#96;&gt;-&#96;&lt;h6&#96;&gt;</div>
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
  h1 {color: #ff5733;}
  h2 {color: #33aaff;}
  h3 {color: #178859;}
  h4 {color: #ffaa33;}
  h5 {color: #aa33ff;}
  h6 {color: #666;}
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

### Visual Hierarchy Example:

If this were a book:

`<h1>` would be the book title.
`<h2>` would be chapter titles.
`<h3>` would be section titles inside a chapter.
`<h4>` to `<h6>` would be used for smaller subsections.

### Why are Headings Important?

- Organize Content: Headings break up your content into sections, making it easier to read.
- Search Engine Optimization (SEO): Search engines like Google use headings to understand what your page is about.
- Accessibility: Headings help screen readers navigate your page, making it more accessible.

### Pro Tips:

- Use only one `<h1>` per page for the main title.
- Use headings in order: `<h1>` first, then `<h2>`, and so on.
- Don’t skip levels (e.g., don’t go from `<h1>` to `<h3>` directly).


