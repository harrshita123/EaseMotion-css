# Menu Native Dark Mode Support

## Description
This PR adds native OS-level dark mode support to the `menu` component using `@media (prefers-color-scheme: dark)` and CSS Custom Properties (variables). This ensures that the component gracefully shifts to a low-strain, dark-themed aesthetic whenever the user enables dark mode on their device, improving accessibility and saving battery on OLED screens.

## Usage
Include the component as usual. It automatically reacts to OS-level Light/Dark mode settings without requiring JavaScript theme toggles.

## Changes
- `style.css`: 60+ lines adding CSS variables and `prefers-color-scheme` media queries.
- `demo.html`: Demo testing layout with light/dark adaptive background.
- `README.md`: Describes the feature.
\nFixes #55139\n