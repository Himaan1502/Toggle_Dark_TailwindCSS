# Dark Mode Toggle with TailwindCSS

This repository contains a basic example script for toggling dark mode using TailwindCSS. The HTML structure includes a button that allows users to switch between light and dark themes. TailwindCSS classes are utilized to apply styling to the elements in both light and dark modes.

## Features

- **Dark Mode Toggle**: A button that toggles the dark mode by adding or removing the `dark` class on the `document.documentElement`.
- **Styled with TailwindCSS**: Uses TailwindCSS utility classes for styling components in both light and dark themes.
- **Lightweight JavaScript**: JavaScript function with a minimal event listener to switch between themes.

## Structure

The example includes:
1. A `div` container that demonstrates both dark and light styling.
2. A `button` that triggers the toggle between light and dark modes.
3. JavaScript to manage the dark mode toggle by manipulating the `classList` on the root element.

## Usage

1. **HTML**: The main container (`div`) is styled with TailwindCSS classes for both `light` and `dark` themes.
   - Example: `bg-white dark:bg-black` will apply a white background in light mode and a black background in dark mode.

2. **JavaScript**: 
   - Adds an event listener to the toggle button.
   - Toggles the `dark` class on `document.documentElement` to switch themes.
   - Displays a simple alert on each button click to confirm the action.

3. **Button**: `Toggle Dark Mode` button which, when clicked, will add or remove the `dark` class on the `document.documentElement`, enabling the dark mode styles.

## Installation and Usage

1. Make sure you have TailwindCSS set up in your project. You can follow the setup guide on the [TailwindCSS website](https://tailwindcss.com/docs/installation).
2. Copy the HTML, CSS, and JavaScript code provided into your project.
3. Open the HTML file in your browser and click the `Toggle Dark Mode` button to see the effect.

## Example Code

### HTML & JavaScript

```html
<!-- Theme Dark: -->
<div class="m-10 rounded-lg bg-white px-6 py-8 shadow-xl ring-1 ring-slate-900/5 dark:bg-black">
  <h3 class="text-base font-medium tracking-tight text-slate-900 dark:text-white">This is a Text Element</h3>
  <p class="mt-2 text-sm text-slate-500 dark:text-blue-100">This is a paragraph tag element</p>

  <button
    id="toggleDark"
    class="text-blue-900 px-4 py-2 text-sm font-medium mt-8 bg-blue-100 rounded-md hover:bg-blue-300"
    onclick="document.documentElement.classList.toggle('dark')"
  >
    Toggle Dark Mode
  </button>
</div>

<script type="text/javascript">
  document.addEventListener("DOMContentLoaded", () => {
    const toggleDark = document.getElementById('toggleDark');
    toggleDark.addEventListener('click', function() {
      if (document.documentElement.classList.contains('dark')) {
        document.documentElement.classList.remove('dark');
      } else {
        document.documentElement.classList.add('dark');
      }
      alert("Dark mode toggled!");
    });
  });
</script>
