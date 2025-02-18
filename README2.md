# Documentation for dark and light mode
* If the "Toggle Dark Mode" button is not working, it’s likely due to one of the following reasons:

  - JavaScript is not properly linked or executed.

  - The CSS for dark mode is not correctly applied.

  - The button or JavaScript code has errors.

* Let’s fix this step by step:

# Step 1: Ensure JavaScript is Linked
Make sure your JavaScript code is properly linked in your HTML file. Add the following <script> tag just before the closing </body> tag:

* html:
```
  <script>
  const toggleButton = document.getElementById('theme-toggle');
  toggleButton.addEventListener('click', () => {
    document.body.classList.toggle('dark-mode');
  });
  </script>
```
* Alternatively, if you’re using an external JavaScript file, link it like this:
html:
```
    <script src="script.js"></script>
```
# Step 2: Verify CSS for Dark Mode
Ensure your CSS for dark mode is correctly defined. Here’s the updated CSS:
CSS:
```
    ---/* Light mode (default) */
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
      color: #333;
    }
    
    header {
      background: #333;
      color: #fff;
      padding-top: 30px;
      min-height: 70px;
      border-bottom: #77aaff 3px solid;
    }
    
    ---/* Dark mode */
    body.dark-mode {
      background-color: #333;
      color: #f4f4f4;
    }
    
    body.dark-mode header {
      background-color: #222;
    }
    
    body.dark-mode section h2 {
      color: #77aaff;
    }
```

# Step 3: Debug the JavaScript
If the button still doesn’t work, check the browser console for errors (right-click → Inspect → Console). Common issues include:

Element not found: Ensure the button has the correct id="theme-toggle".

JavaScript errors: Ensure there are no typos or syntax errors in your JavaScript code.
javascript:-
```
document.addEventListener('DOMContentLoaded', () => {
  const toggleButton = document.getElementById('theme-toggle');
  if (toggleButton) {
    toggleButton.addEventListener('click', () => {
      document.body.classList.toggle('dark-mode');
    });
  } else {
    console.error('Button with id "theme-toggle" not found!');
  }
});
```
This code ensures the JavaScript runs only after the DOM is fully loaded and checks if the button exists.
# Step 4: Full HTML Example
Here’s the complete HTML with the button and JavaScript:
html:-
```
  <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Your Name - Technical Support Specialist</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <div class="container">
      <h1>Your Name</h1>
      <p>Technical Support Specialist</p>
      <p>Detail-oriented and customer-focused professional with [X years] of experience.</p>
    </div>
  </header>

  <button id="theme-toggle">Toggle Dark Mode</button>

  <section id="summary">
    <div class="container">
      <h2>Professional Summary</h2>
      <p>Detail-oriented and customer-focused Technical Support Specialist with [X years] of experience providing Level 1 technical support in fast-paced, international environments. Skilled in troubleshooting operating systems (Windows, macOS, Linux), resolving basic technical issues, and escalating complex problems with detailed reports. Proven ability to handle high call volumes (3,000–4,000 annually) while maintaining excellent client satisfaction. Fluent in English with strong communication skills and a passion for delivering efficient, resourceful solutions.</p>
    </div>
  </section>

  <!-- Add other sections here -->

  <footer>
    <div class="container">
      <p>Contact: [Your Email Address] | [Your Phone Number]</p>
    </div>
  </footer>

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const toggleButton = document.getElementById('theme-toggle');
      if (toggleButton) {
        toggleButton.addEventListener('click', () => {
          document.body.classList.toggle('dark-mode');
        });
      } else {
        console.error('Button with id "theme-toggle" not found!');
      }
    });
  </script>
</body>
</html>
```
# Step 5: Test the Button
Open your website in a browser.

Click the "Toggle Dark Mode" button.

The background and text colors should switch between light and dark modes.
# Step 6: Debugging Tips
If the button still doesn’t work, check the browser console for errors.

Ensure the id="theme-toggle" matches the getElementById call in JavaScript.

Make sure the CSS for .dark-mode is correctly defined and applied.

Here’s the corrected and complete JavaScript code:
```
