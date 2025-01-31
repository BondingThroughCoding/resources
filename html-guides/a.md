---
layout: default
title: Anchor Tag Guide
---

# The Magic Portal: Using `<a>`! 🪄

The `<a>` tag creates clickable links - like secret doorways to other pages or places! Perfect for connecting stories, games, and adventures. Let's become link wizards! 🧙

## What's an Anchor Tag? ⚓

Your webpage's teleporter:
- Creates clickable links 🔗
- Can go to other pages or same page spots 📄
- Works like a magic portal! 🌀

### Let's Build Portals! 🚪
Add `<a>` tags to create links. Try making a space adventure map below! 🚀

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Portal Workshop 🌌</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<!DOCTYPE html>
<html>
  <head>
    <title>Space Adventure Map</title>
  </head>
  <body>
    <h1>Explore the Galaxy!</h1>
    <p>Choose your destination:</p>
    <ul>
      <li><a href="#mars">Visit Mars</a></li>
      <li><a href="#moon">Explore the Moon</a></li>
      <li><a href="#jupiter">Fly to Jupiter</a></li>
    </ul>
    
    <h2 id="mars">Mars</h2>
    <p>Meet the Martian robots!</p>
    
    <h2 id="moon">Moon</h2>
    <p>Jump in low gravity!</p>
    
    <h2 id="jupiter">Jupiter</h2>
    <p>See the giant red spot!</p>
  </body>
</html>
</textarea>
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

## Why `<a>` Rocks! 🤘

1. **Page Connector**: Links different pages together 🔗
2. **Section Jumper**: Moves within same page 🎯
3. **Resource Linker**: Opens files or emails 📎
4. **Accessibility Helper**: Helps screen readers navigate ♿

### Link Tricks 🎩
- Use `href="#id"` for same-page jumps
- Add `target="_blank"` to open in new tab
- Link to emails with `mailto:`
- Create phone links with `tel:`

## Pro Tips for Link Legends 🏅

- Always include `href` attribute
- Use descriptive link text
- Test all links to make sure they work
- Add `title` attribute for tooltips
- Keep external links secure with `https`

What awesome links will YOU create? A dinosaur map? Robot directory? Show us in the playground! 🦖🤖