---
layout: default
title: Unordered List Guide
---

# Let's Master Bullet Lists with `<ul>`! 🔫

Unordered lists are like your favorite sticker collection - perfect for grouping cool stuff without numbers! Great for game power-ups, birthday wishlists, or alien spotting notes. 👽

## Bullet List Basics 🧠

Meet your new best friends:
- **`<ul>`** = Unordered List (think of it as a magic bubble wand)
- **`<li>`** = List Item (the awesome bubbles you blow!)

### Creating Your First List 🎨
Start with the `<ul>` magic wand, add `<li>` bubbles between, and close with `</ul>`. Try making a superhero toolkit in the playground below! 🦸

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Magic List Workshop ✨</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<ul>
  <li>Invisibility cloak</li>
  <li>Super-speed shoes</li>
  <li>Teleportation device</li>
</ul>
<style>
  li { 
    color: #ff69b4;
    font-family: 'Bubblegum Sans';
    font-size: 20px;
  }
</style></textarea>
    <iframe id="preview" style="border:none;"></iframe>
  </div>
</div>

<script>
  // Our reliable demo script
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

## Why Bullet Lists Are Awesome 💥

1. **Instant Organization**: No numbers needed - just pure fun! 🎉
2. **Style Playground**: Make hearts, stars, or pizza slice bullets! 🍕
3. **Mix & Match**: Combine with numbered lists for ultimate power ⚡
4. **Quick Reads**: Perfect for snack lists or game cheats! 🕹️

### Secret Bullet Tricks 🎩
- Change bullet shapes using CSS magic words like _circle_ or _square_
- Make emoji bullets by adding tiny pictures before list items
- Create list-ception by putting lists inside lists!
- Use rainbow colors with CSS color codes

## Pro Tips for List Champions 🏅

- Great for **groups of similar things** (like pizza toppings or superpowers)
- Keep items short - bullets love quick snack-sized info! 🍟
- Try adding _margin-left_ in CSS to control spacing
- Screen readers announce bullet lists specially - super helpful! ♿

What amazing list will YOU create? A dinosaur bucket list? Secret club rules? Show us in the playground! 🚀