---
layout: default
title: Body Tag Guide
---

# The Story Stage: Using `<body>`! 🎭

The `<body>` tag is like a stage for your webpage - it's where all the action happens! Perfect for showing text, pictures, and games. Let's become web storytellers! 📖

## What's the `<body>` Tag? 🎪

Your webpage's main area:
- Shows everything visitors see 👀
- Holds text, images, and more 🖼️
- Works like a blank canvas 🎨
- Comes after the `<head>` section 🧠

### Let's Build a Stage! 🛠️
Add content inside `<body>` to make your page come alive. Try creating a space adventure below! 🚀

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Story Stage Workshop 🎬</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<body>
  <h1>Welcome to Space!</h1>
  <p>Explore the galaxy with me:</p>
  <ul>
    <li>Visit Mars</li>
    <li>Meet aliens</li>
    <li>Find space treasure</li>
  </ul>
</body></textarea>
    <iframe id="preview" style="border:none;"></iframe>
  </div>
</div>

<script>
  // Standard interactive script
  var textarea = document.getElementById('code');
  var initialContent = textarea.value;
  
  document.querySelector('.reset-button').addEventListener('click', function() {
    editor.setValue(initialContent);
    updatePreview();
  });

  var editor = CodeMirror.fromTextArea(document.getElementById('code'), {
    mode: 'xml',
    lineNumbers: true,
    theme: 'dracula',
    matchBrackets: true
  });

  function updatePreview() {
    var iframe = document.getElementById('preview');
    var content = editor.getValue();
    var doc = iframe.contentWindow.document;
    doc.open();
    doc.write(content);
    doc.close();
  }

  editor.on('change', updatePreview);
  updatePreview();
</script>
{% endraw %}

## Why `<body>` Rocks! 🤘

1. **Content Home**: Holds all visible elements 🏠
2. **Story Space**: Perfect for articles, games, and more 📚
3. **Interactive Zone**: Add buttons, forms, and videos 🎮
4. **Accessibility Base**: Helps screen readers navigate ♿

### Body Building Blocks 🧱
- Headings (`<h1>` to `<h6>`)
- Paragraphs (`<p>`)
- Lists (`<ul>`, `<ol>`, `<li>`)
- Images (`<img>`)
- Links (`<a>`)

## Pro Tips for Body Builders 🏗️

- Always put content inside `<body>`
- Use proper tags for each content type
- Keep your structure logical
- Test on different screen sizes
- Add alt text for images

What awesome story will YOU tell? A dinosaur discovery? Robot adventure? Show us in the playground! 🦖🤖