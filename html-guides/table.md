---
layout: default
title: Table Tag Guide
---

# Building Awesome Tables with `<table>`! 🏗️

Tables are like digital LEGO grids - perfect for game scores, animal facts, or comparing your favorite snacks! Let's learn to build information castles! 🏰

## Table Building Blocks 🧱

Meet your construction crew:
- **`<table>`**: The foundation (holds everything together)
- **`<tr>`**: Table Row (horizontal layers)
- **`<td>`**: Regular Cells (basic building blocks)
- **`<th>`**: Header Cells (king blocks with crowns! 👑)

### Let's Construct! 🚧
Tables grow row by row. Try making a magic creature zoo in the playground below! 🦄

{% raw %}
<div class='demo-container'>
  <div class='demo-title'>
    <div>Table Workshop 🛠️</div>
    <div class='reset-button'>Reset</div>
  </div>
  <div class='code-container'>
    <textarea id="code" name="code">
<table>
  <tr>
    <th>Creature</th>
    <th>Superpower</th>
    <th>Snack</th>
  </tr>
  <tr>
    <td>Sparkle Unicorn</td>
    <td>Rainbow Magic</td>
    <td>Starlight Cookies</td>
  </tr>
  <tr>
    <td>Fire Dragon</td>
    <td>Lava Breath</td>
    <td>Spicy Peppers</td>
  </tr>
</table>
<style>
  table {
    border: 3px solid #ff6b6b;
    border-collapse: collapse;
    background: #fff5f5;
  }
  th {
    background: #4ecdc4;
    color: white;
    padding: 10px;
    font-family: 'Comic Sans MS';
  }
  td {
    padding: 8px;
    border: 1px dotted #ff9999;
    font-family: 'Bubblegum Sans';
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

## Why Tables Rock! 🤘

1. **Organize Anything**: From game stats to candy collections 🍭
2. **Header Power**: `<th>` cells automatically stand out! 💪
3. **Style Playground**: Add colors, borders, and cool fonts 🎨
4. **Screen Reader Friendly**: Helps everyone understand your data ♿

### Table Tricks 🎩
- Add _border-collapse_ in CSS to make smooth lines
- Use _padding_ to give cells breathing room
- Try _nth-child()_ magic to make rainbow rows 🌈
- Merge cells horizontally with _colspan_

## Pro Tips for Table Masters 🏆

- Always start with `<tr>` for new rows
- Use `<th>` for column titles
- Keep tables simple - like pizza boxes 🍕
- Add _caption_ tags for table titles
- Test on mobile - tables can be squishy! 📱

What amazing table will YOU build? A dinosaur fact chart? Video game leaderboard? Show us in the playground! 🚀