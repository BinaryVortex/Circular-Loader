# Circular Loader

![Circular Loader Screenshot](./Screenshot%202024-07-09%20082809.png)

A minimal, lightweight circular loader built with pure HTML and CSS — no JavaScript required. Clean, easy to customize, and suitable for small projects, demos, or as a starter component for your UI.

## Demo / Preview

Open `index.html` in your browser (if included) to see the loader in action. The screenshot above shows the default size and color.

## Features

- Pure HTML & CSS (no JS)
- Small and easy to understand
- Smooth, hardware-accelerated animation
- Customizable size, color, thickness, and speed
- Works in modern browsers

## Installation

Clone or download this repository, then open `index.html` in your browser:

```bash
git clone https://github.com/BinaryVortex/Circular-Loader.git
cd Circular-Loader
# open index.html in your browser
```

## Usage

Place the loader markup where you want it:

```html
<!-- Add this where you want the loader -->
<div class="loader" role="status" aria-label="Loading"></div>
```

Example CSS (`style.css`):

```css
.loader {
  width: 80px;
  height: 80px;
  border: 8px solid rgba(0, 0, 0, 0.08);
  border-top-color: #3498db; /* change to customize color */
  border-radius: 50%;
  animation: spin 1s linear infinite;
  display: block;
  margin: 40px auto;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}
```

## Customization

- Size: change `width` and `height`.
- Thickness: change the `border` width (e.g., `4px`, `12px`).
- Color: change `border-top-color`.
- Speed: change `animation` duration (e.g., `0.6s` for faster, `1.5s` for slower).
- Centering: wrap the loader in a flex container for perfect centering.

Example center container:

```css
.center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
```

## Accessibility

- Use `role="status"` and `aria-label="Loading"` to communicate that this is a live status indicator.
- For long-running tasks, provide a text fallback (visually hidden) or an alternative progress indicator.

Visually-hidden helper:

```html
<span class="sr-only">Loading…</span>
```

```css
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0,0,0,0);
  white-space: nowrap;
  border: 0;
}
```

## Browser Support

Works across modern browsers that support CSS animations: Chrome, Firefox, Edge, Safari. No polyfills required.

## Examples & Variants

- Dual-color: use multiple pseudo-elements to create a two-toned spinner.
- Dotted: use repeating radial-gradients for dotted loaders.
- Pulsing: animate `opacity` or `transform` for a pulsing effect.

If you want, I can add a few variant CSS files demonstrating these styles.

## Contributing

Contributions welcome! Please open an issue for feature requests or bugs, or submit a pull request. When contributing, include a brief description of changes and update this README if needed.

## License

This repository currently has no license file. If you want to make the project open source and allow reuse, consider adding a license such as the MIT License. Example:

```
MIT License
Copyright (c) YEAR BinaryVortex
Permission is hereby granted...
```

Add a `LICENSE` file to the repository to make the choice explicit.

## Author

BinaryVortex

---

Made with ❤️ by BinaryVortex
