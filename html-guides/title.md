---
layout: default
title: Title Tag Guide
---

# Name Tag Magic: Using `<title>`! 🏷️

The `<title>` tag gives your webpage its special name - like a superhero's secret identity! It shows up in browser tabs and helps people find your page. Let's become naming ninjas! 🥷

## What's a Title Tag? 🎯

Your webpage's ID card:
- Shows in browser tabs 📑
- Appears in search results 🔍
- Helps bookmarking 📌
- Works like a book title for your page! 📚

### Let's Name Your Page! ✨
Add a `<title>` inside the `<head>` section. Try creating a space adventure name below! 🚀

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Name Workshop 🌟</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<head>
  <title>***Galaxy Explorer 3000***</title>
</head>
<body>
  <h1>🚀 Welcome Space Cadet!</h1>
  <p>Ready to explore the Milky Way?</p>
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

## Why Titles Rock! 🤘

1. **First Impression**: First thing people see in search results 👀
2. **Tab Organization**: Helps find your page among many tabs 📑
3. **Bookmark Friendly**: Makes saved pages easy to recognize 📌
4. **SEO Superpower**: Helps search engines understand your page 🤖

### Title Tricks 🎩
- Keep it short (like a good tweet!) 🐦
- Use important words first
- Add your website name at the end
- Make it exciting like a movie title! 🍿

## Pro Tips for Title Masters 🏆

- **Only one `<title>` per page** - No duplicates! 🚫
- **50-60 characters max** - Fits in search results 📏
- **Include keywords** - But keep it natural 🔑
- **Be unique** - Like your fingerprint! 👆
- **No emojis** (They look fun but can be messy in search results) 🚫🎉

What awesome name will YOU choose? "Dinosaur Discovery Zone"? "Robot Coding Camp"? Show us in the playground! 🦖🤖