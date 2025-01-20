---
layout: default
title: Background Color Guide
author: Caitlyn Muscat
---

# Background Color

`background-color` is a CSS property that allows you to change the background color of a webpage within your website. To change the colors, you can use the word i.e. 'White', the hex value, `#ffffff` , or the rgb value: `rgb(255,255,255)`.

## Example

Say I wanted to change the background color of the header of my website, I can use the following piece of code:

```css
h1 {
    background-color: rgb(150, 0, 255);
}
```

This code tells my website that I am changing the background color of my header, `h1`, to purple using rgb values!

If you want to know more about the `background-color` property, you can go to the links at [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color) or [w3schools](https://www.w3schools.com/cssref/pr_background-color.php). Both of these sites give excellent examples of the background-color CSS property that are interactive, and allow you to change and alter the values to see how the property works. 

{% raw %}

<div class="demo-container">
  <div class="controls">
    <div class="color-option" contenteditable="true">background-color: red;</div>
    <div class="color-option" contenteditable="true">background-color: #E16036;</div>
    <div class="color-option" contenteditable="true">background-color: rgb(239, 208, 158);</div>
    <div class="color-option" contenteditable="true">background-color: rgba(38, 28, 21, 0.7);</div>
    <div class="color-option" contenteditable="true">background-color: hsl(202, 78%, 67%);</div>
    <div class="color-option" contenteditable="true">background-color: hsla(65, 96%, 66%, 0.7);</div>
  </div>
  <div class="display-box" id="display-box"></div>
</div>

<style>
  .demo-container {
    display: flex;
    align-items: center;
    gap: 20px;
    background-color: #f7f7f7;
    padding: 20px;
    border-radius: 8px;
  }
  .controls {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  .color-option {
    cursor: pointer;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    text-align: center;
    background-color: #fff;
    color: #333;
    transition: background-color 0.3s, color 0.3s;
  }
  .color-option:hover {
    background-color: #e0e0e0;
    color: #000;
  }

  .color-option:empty:before {
    content: "Edit color code";
    color: #aaa;
  }
  .display-box {
    flex: 1;
    height: 300px;
    border: 1px solid #ccc;
    background-color: #b22222;
    transition: background-color 0.5s ease;
  }
  .error{
    outline: 2px solid red;
  }
</style>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const colorOptions = document.querySelectorAll('.color-option');
    const displayBox = document.getElementById('display-box');

    colorOptions.forEach(option => {
      // Handle input event for editable divs
      option.addEventListener('input', () => {
        let newColor = option.textContent.trim();
        
        // Remove 'background-color' and trim the semicolon
        newColor = newColor.replace(/^background-color:\s*/i, '').replace(/;$/, '').trim();
        
        // Convert the color to RGB and check if it's valid
        const rgbColor = convertToRGB(newColor);

        if (isValidColor(rgbColor) || isValidColor(newColor)) {
          displayBox.style.backgroundColor = newColor;
            option.classList.remove("error")

        } else {
          displayBox.style.backgroundColor = 'transparent'; // Reset display box color
          option.classList.add("error")
        }
      });

      // Handle click event for color options
      option.addEventListener('click', () => {
        let newColor = option.textContent.trim();
        
        // Remove 'background-color' and trim the semicolon
        newColor = newColor.replace(/^background-color:\s*/i, '').replace(/;$/, '').trim();
        
        // Convert the color to RGB and check if it's valid
        const rgbColor = convertToRGB(newColor);
        
        if (isValidColor(rgbColor) || isValidColor(newColor)) {
          displayBox.style.backgroundColor = newColor;
            option.classList.remove("error")

        } else {
          displayBox.style.backgroundColor = 'transparent'; // Reset display box color
          option.classList.add("error")

        }
      });
    });

    function isValidColor(color) {
      const testDiv = document.createElement('div');
      testDiv.style.backgroundColor = color;
      return testDiv.style.backgroundColor === color;
    }

    // Function to convert Hex, HSL/HSLA to RGB
    function convertToRGB(color) {
      let rgb = null;
      
      // Check if the color is in hex format
      if (/^#[0-9A-Fa-f]{6}$|^#[0-9A-Fa-f]{3}$/.test(color)) {
        rgb = hexToRGB(color);
      }
      // Check if the color is in HSL or HSLA format
      else if (/^hsl\(\d+(\.\d+)?\s*,\s*\d+%?\s*,\s*\d+%?\)$/.test(color) || /^hsla\(\d+(\.\d+)?\s*,\s*\d+%?\s*,\s*\d+%?\s*,\s*(0|1|0?\.\d+)\)$/.test(color)) {
        rgb = hslToRGB(color);
      }
      // Check if the color is in RGB or RGBA format
      else if (/^rgb\(\d{1,3},\s*\d{1,3},\s*\d{1,3}\)$/.test(color) || /^rgba\(\d{1,3},\s*\d{1,3},\s*\d{1,3},\s*(0|1|0?\.\d+)\)$/.test(color)) {
        rgb = color;
      }

      return rgb;
    }

    // Function to convert Hex to RGB
    function hexToRGB(hex) {
      let r = 0, g = 0, b = 0;
      if (hex.length === 4) {
        r = parseInt(hex[1] + hex[1], 16);
        g = parseInt(hex[2] + hex[2], 16);
        b = parseInt(hex[3] + hex[3], 16);
      } else if (hex.length === 7) {
        r = parseInt(hex[1] + hex[2], 16);
        g = parseInt(hex[3] + hex[4], 16);
        b = parseInt(hex[5] + hex[6], 16);
      }
      return `rgb(${r}, ${g}, ${b})`;
    }

    // Function to convert HSL/HSLA to RGB
    function hslToRGB(hsl) {
      let [h, s, l, a] = hsl.replace(/[a-zA-Z()]/g, '').split(',').map(val => val.trim());
      h = parseInt(h);
      s = parseInt(s) / 100;
      l = parseInt(l) / 100;
      a = a ? parseFloat(a) : 1;

      let c = (1 - Math.abs(2 * l - 1)) * s;
      let x = c * (1 - Math.abs(((h / 60) % 2) - 1));
      let m = l - c / 2;
      let r, g, b;

      if (h >= 0 && h < 60) {
        r = c;
        g = x;
        b = 0;
      } else if (h >= 60 && h < 120) {
        r = x;
        g = c;
        b = 0;
      } else if (h >= 120 && h < 180) {
        r = 0;
        g = c;
        b = x;
      } else if (h >= 180 && h < 240) {
        r = 0;
        g = x;
        b = c;
      } else if (h >= 240 && h < 300) {
        r = x;
        g = 0;
        b = c;
      } else {
        r = c;
        g = 0;
        b = x;
      }

      r = Math.round((r + m) * 255);
      g = Math.round((g + m) * 255);
      b = Math.round((b + m) * 255);

      return `rgb(${r}, ${g}, ${b})`;
    }
  });
</script>

{% endraw %}



