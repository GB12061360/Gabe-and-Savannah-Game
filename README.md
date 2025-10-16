# Gabe & Savannah – Team Bear

A small single page virtual companion prototype for Gabe and Savannah. The game runs entirely in the browser using vanilla JavaScript and Tailwind via the CDN build.

## Getting started

1. Serve the project with any static file server (service workers require an HTTP origin):
   ```bash
   python -m http.server 4173
   ```
2. Visit `http://localhost:4173` in your browser.
3. The app stores progress in `localStorage`. Use your browser dev tools to clear the storage if you want to reset the save file.

## Development notes

- Tailwind is loaded with the official Play CDN so all utility classes declared in the markup are available without a build step.
- A service worker is registered automatically in supported browsers to provide a basic offline experience using the files listed in `service-worker.js`.
- The main gameplay logic lives inside `index.html` in the large inline script. The code is organized into small helper functions (rendering, state management, modals, etc.) so it can be edited without a bundler.

## Project structure

```
.
├── index.html          # Game UI, state management, and modals
├── manifest.json       # PWA manifest used by the service worker
├── service-worker.js   # Simple offline-first cache strategy
└── README.md           # You're reading it
```

Happy caretaking!
