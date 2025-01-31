---
layout: default
title: Image Tag Guide
---

# Magic Windows: Using `<img>` to Show Pictures! 🖼️

The `<img>` tag is like a photo frame for your webpage - perfect for showing cute animals, space adventures, or your latest drawings! Let's become picture wizards! 🧙♂️

## What's an Image Tag? 🧐

Meet your new art supplies:
- **`<img>`**: The magic window that displays pictures
- **`src`**: The "address" telling where to find the picture
- **`alt`**: A secret description for screen readers

### Let's Create Magic! ✨
Images need two special ingredients: _src_ for the picture location and _alt_ for description. Try adding a dancing robot in the playground below! 🤖

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Picture Workshop 🎨</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<img src="/assets/cat.jpg">
<style>
  img {
    border: 3px solid #ff6b6b;
    border-radius: 20px;
    box-shadow: 5px 5px 10px pink;
    width: 200px;
    height: 200px;
    object-fit: cover;
  }
</style></textarea>
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

## Why Images Rule! 🌟


1. **Story Power**: Show instead of tell! 🎭
2. **Mood Magic**: Set happy/spooky/silly vibes 🎃
3. **Memory Help**: Remember information better 🧠
4. **Accessibility**: _Alt text_ helps everyone understand ♿

### Image Tricks 🎩
- Resize with _width_ and _height_ attributes
- Make circular photos with _border-radius: 50%_
- Add hover effects that make images jump! 
- Create photo galleries with multiple `<img>` tags

## Pro Tips for Image Wizards 🔮

- Always use _alt_ text - it's like a picture description
- Keep images small for fast loading 🚀
- Use .jpg for photos, .png for transparent images
- Never stretch images - they get pixelated! 🧊
- Try _lazy-loading_ for long pages 📜

What amazing images will YOU add? A roaring dinosaur? Floating astronaut? Show us in the playground! 🚀