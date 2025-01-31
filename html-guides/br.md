---
layout: default
title: Line Break Guide
---

# Bouncing Lines with `<br>`! 🎪

The `<br>` tag is like a trampoline for your words - it lets you jump to a new line without starting a new paragraph! Perfect for poems, addresses, or making text dance! 💃

## What's a Line Break? 🤸

Meet your text bouncer:
- **`<br>`**: Creates instant line jumps
- No closing tag needed (it's a lone wolf! 🐺)
- Works like an "Enter" key for web pages! ⏎

### Let's Make Text Bounce! 🏀
Add `<br>` wherever you want a line break. Try writing a space poem below! 🚀

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Line Break Gymnasium 🤸</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<p>
  Twinkling stars up high<br>
  Shooting comets zooming by<br>
  Alien waves hello<br>
</p></textarea>
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

## Why Line Breaks Rock! 🌟

1. **Poetry Power**: Create haikus or rap lyrics! 🎤
2. **Address Magic**: Format locations neatly 🏠
3. **Song Lyrics**: Keep verse structures intact 🎶
4. **Quick Skips**: Add space without new paragraphs 🚀

### Breakdancing Tricks 💫
- Stack multiple `<br>` for bigger gaps
- Combine with _&nbsp;_ for special spacing
- Use in forms for better alignment
- Make vertical lists without bullets

## Pro Tips for Break Masters 🏆

- Don't overuse - paragraphs are better for big text! 📚
- Great for short line separations (like addresses)
- Never use for layout - CSS is better for that 🎨
- Screen readers pause slightly at `<br>`
- Try _line-height_ in CSS for consistent spacing

What cool text layout will YOU create? A robot song? Pizza recipe steps? Show us in the playground! 🍕