---
layout: default
title: Link Tag Guide
---

# The Super Connector: Using `<link>`! 🌉

The `<link>` tag is like a magic bridge that connects your webpage to cool stuff - like stylesheets, icons, and fonts! Let's become connection champions! 🏆

## What Does `<link>` Do? 🤝

Your webpage's best friend for:
- Adding website clothes (CSS stylesheets) 👗
- Creating tab icons (favicons) 🌟
- Using special fonts 🖋️
- Connecting to other resources 🌐

### Let's Build Bridges! 🌈
Add a `<link>` inside `<head>` to connect resources. Try changing your page's outfit below! 👕

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Connection Station 🚂</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<head>
  <title>Fashionable Page</title>
  <link rel="stylesheet" href="./example.css">
</head>
<body>
  <h1>🌈 Style Changer!</h1>
  <p>Edit the link above to make me fabulous!</p>
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

## Why `<link>` Rocks! 🎸

1. **Outfit Changer**: Switch stylesheets like costumes! 🦸
2. **Icon Maker**: Add custom tab icons (favicons) 🌠
3. **Font Wizard**: Use cool fonts from the internet ✨
4. **Organizer**: Keep your code clean and tidy 🧹

### Link Tricks 🎩
- Change `rel="stylesheet"` to `rel="icon"` for favicons
- Use Google Fonts by linking their stylesheets
- Add multiple links for different purposes
- Make printed versions with `rel="print"`

## Pro Tips for Link Legends 🏅

- Always put `<link>` in the `<head>` section
- Use `type="text/css"` for stylesheets
- Favicons work best as `.ico` files
- Keep external CSS in separate files
- Try `rel="preload"` for faster loading 🚀

What awesome connections will YOU make? A dinosaur-themed stylesheet? Space font? Show us in the playground! 🦖🚀