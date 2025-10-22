# dirty-autobattler — index.html

This repository contains a lightweight HTML-based autobattler game. The entry point is `index.html`. This README explains what the project is, how to run it locally, where to find configuration and assets, and how to contribute.

## Table of contents
- [About](#about)
- [Play (quick start)](#play-quick-start)
- [Run locally](#run-locally)
- [Controls & gameplay](#controls--gameplay)
- [Configuration & customization](#configuration--customization)
- [Development tips](#development-tips)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## About
dirty-autobattler is an HTML-only demo/autobattler game project. It is small and intended to be run directly in the browser. The project uses only client-side code (HTML, CSS, and JavaScript inside `index.html`) so there's no build step required.

## Play (quick start)
1. Clone or download this repository.
2. Open `index.html` in a modern web browser (Chrome, Firefox, Edge, Safari).
3. The game should start or present a main menu — follow on-screen prompts.

For the most reliable experience, serve the files over HTTP (see "Run locally" below). Some browsers restrict certain features when files are opened using the `file://` protocol.

## Run locally
Recommended minimal options:

- Using Python (works if Python 3.x is installed):
  - From the project root:
    - python -m http.server 8000
  - Then open: http://localhost:8000/index.html

- Using Node (http-server):
  - Install once: npm install -g http-server
  - Start: http-server -p 8000
  - Open: http://localhost:8000/index.html

- Or simply double-click `index.html` to open in your browser (may work but some browsers impose local-file restrictions).

## Controls & gameplay
Controls and exact gameplay mechanics are implemented inside `index.html`. Typical interactions in browser-based autobattlers:
- Mouse / touch:
  - Click / tap units or UI elements to place/select.
  - Drag if dragging is implemented (see in-file comments).
- Keyboard (if implemented):
  - P — pause/resume
  - R — restart
  - Number keys — quick-select or hotbar (if supported)

If controls differ, refer to the top of `index.html` for comments describing the control scheme and constants.

## Configuration & customization
- Many small games keep configuration near the top of `index.html`. Look for clearly labeled constants such as spawn rates, health/damage values, or toggles for debug logging.
- To change visuals, edit inline CSS or referenced asset paths.
- To add or replace sprites/audio, update assets referenced by `index.html`.

Before editing, create a copy or branch to keep changes safe.

## Development tips
- Use a live-reload extension or a simple static server (see "Run locally") to auto-refresh while editing.
- Open the browser DevTools (Console) to inspect logs, errors, and debug output.
- If you add more files (JS/CSS/assets), consider moving heavy logic into separate files for maintainability.

## Troubleshooting
- Blank screen:
  - Check the browser console for JavaScript errors.
  - Ensure files are served over HTTP if the game uses fetch/XHR or module imports.
- Audio or images not loading:
  - Confirm asset filenames and paths in `index.html`.
- Performance issues:
  - Try a different browser or reduce visual effects in the code.

## Contributing
Contributions are welcome. Typical ways to contribute:
- Open issues describing bugs or feature requests.
- Submit a pull request with a clear description and rationale.
- Keep changes small and focused; document any new configuration options.

If you'd like me to add contribution templates, issue templates, or a development checklist, I can draft those next.

## License
This project is provided under the MIT License (if you prefer a different license, update this section accordingly). Add a LICENSE file to the repo to make the license explicit.

## Author
Tuxhedoh — https://github.com/Tuxhedoh

## Where to look in `index.html`
- Top of file: configuration constants and comments.
- Inline comments: small projects often include usage notes and debug keys.
- Assets: referenced near CSS/JS blocks or within `<img>`/`<audio>` elements.

Enjoy playing and extending dirty-autobattler!
