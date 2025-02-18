# ResumeWeb
Web Resume Code


# Add Interactivity with JavaScript (Optional)
You can add JavaScript to make your website more interactive. For example, you can include a button to toggle dark mode:
*HTML:
<button id="theme-toggle">Toggle Dark Mode</button>

* javascript:
const toggleButton = document.getElementById('theme-toggle');
toggleButton.addEventListener('click', () => {
  document.body.classList.toggle('dark-mode');
});
