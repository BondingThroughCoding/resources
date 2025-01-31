---
layout: default
title: Head Tag Guide
---

# The Secret Control Room: Using `<head>`! 🕵️

The `<head>` tag is like the brain of your webpage - it works behind the scenes to make your site awesome! Perfect for adding titles, styles, and secret instructions. 🤫

## What's the `<head>` Tag? 🧠

Meet your webpage's control center:
- **`<head>`**: The invisible helper (doesn't show on the page)
- Holds important stuff like the page title and styles
- Works like a wizard's spellbook! 🧙

### Let's Build a Control Room! 🛠️
Add a `<head>` section to your webpage. Try customizing your page's title and style in the playground below! ✨

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Control Room Workshop 🎛️</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<head>
  <title>My Awesome Space Page</title>
  <link src='./example.css'>
  <script src="./example.js"></script>
</head>
<body>
  <h1>Welcome to Space!</h1>
  <p>Explore the galaxy with me! 🚀</p>
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

## Why the `<head>` Rules! 👑

1. **Title Power**: Shows your page name in browser tabs 📑
2. **Style Magic**: Adds colors, fonts, and layouts 🎨
3. **Search Engine Help**: Tells Google about your page 🤖
4. **Secret Instructions**: Links scripts and meta info 🕶️

### Head Tricks 🎩
- Add a favicon for a cool tab icon
- Use _meta tags_ to describe your page
- Link external stylesheets for fancy designs
- Add scripts to make your page interactive

## Pro Tips for Head Masters 🏆

- Always include a `<title>` in your `<head>`
- Use `<style>` for internal CSS
- Keep `<head>` content organized
- Never put visible content inside `<head>`
- Try _meta charset="UTF-8"_ for special characters

What awesome page will YOU create? A dinosaur discovery site? Secret club portal? Show us in the playground! 🦖