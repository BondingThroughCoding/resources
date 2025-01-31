---
layout: default
title: Ordered List Guide
---

# Understanding the `<ol>` Tag: Creating Numbered Lists 🌟

Ordered lists are like magic staircases for your ideas - each step gets its own automatic number! Perfect for recipes, game instructions, or ranking your favorite superheroes! 🦸

## What Are Ordered Lists? 🤔

Think of them as numbered lunchboxes:
- **`<ol>`** = The lunchbox container (Ordered List)
- **`<li>`** = Your list items (Like snacks inside!)

### Let's Build a List! 🧱
Start with `<ol>`, add `<li>` items between, and close with `</ol>`. Try making a cookie recipe in the demo below!

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Playground: Make Your Own List 🎮</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<ol>
  <li>Mix flour and eggs</li>
  <li>Add chocolate chips</li>
  <li>Bake at 350°F</li>
</ol></textarea>
    <iframe id="preview" style="border:none;"></iframe>
  </div>
</div>

<script>
  // Same script as previous example
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

## Why Love Ordered Lists? ❤️

1. **Auto-Numbers**: Browsers count for you! 🔢
2. **Secret Codes**: Try `type="A"` for ABC lists or `type="I"` for Roman numerals!
3. **Start Anywhere**: Use `start="5"` to begin counting from 5
4. **Listception**: Put lists inside lists! (Add `<ol>` inside an `<li>`)

## Pro Tips for List Masters: 🏆

- Always close your `</li>` tags! 🚨
- Mix with `<ul>` for combo lists (numbers + bullets)
- Make rainbow lists with CSS `color: rainbow;` 🌈
- Screen readers ♥️ ordered lists for accessibility

Now go make some awesome numbered lists! What will YOU create first? 🚀