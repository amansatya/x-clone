# x-clone

A simple, static Twitter-like (X) UI clone built with HTML and Tailwind CSS.

This repository is a front-end prototype of a minimal "Twitter/X" feed UI — a fast way to learn Tailwind layouts, practice responsive design, or use as a static mock for design and testing.

---

## Table of Contents

- [Demo / Screenshots](#demo--screenshots)
- [Features](#features)
- [Built With](#built-with)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Quick Try (CDN)](#quick-try-cdn)
    - [Recommended — Local Dev with Tailwind CLI / PostCSS](#recommended--local-dev-with-tailwind-cli--postcss)
    - [Run Locally](#run-locally)
- [Project Structure](#project-structure)
- [Deployment (Optional)](#deployment-optional)
- [Browser Support & Accessibility Notes](#browser-support--accessibility-notes)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)

## Demo / Screenshots

If you have a hosted demo (for example via GitHub Pages), add the link here.

## Features

- Responsive feed layout similar to Twitter/X
- Post cards with avatar, username, handle, timestamp, and content
- Sidebar/navigation area and simple header
- Built with HTML and Tailwind CSS (no JavaScript required for the core UI)
- Lightweight and easy to customize via Tailwind config

## Built With

- **HTML** — markup & structure
- **Tailwind CSS** — utility-first CSS framework
- **Optional** Node.js + Tailwind CLI / PostCSS for building production CSS

## Getting Started

### Prerequisites

**For the CDN quick-try:** only a modern web browser.

**For local development and production build:**
- Node.js (>= 14 recommended)
- npm or yarn (for installing Tailwind and build tools)

### Quick Try (CDN)

If you just want to preview the UI without installing anything, you can use the Tailwind CDN in the HTML.

1. Open `index.html` (or the main HTML file) in a browser.
2. If the project already references Tailwind via CDN, you should see styled UI.
3. If not, add the following inside the `<head>` to test quickly (not recommended for production):

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
```

**Note:** The CDN build is fine for prototyping but is not tree-shaken and will be large for production.

### Recommended — Local Dev with Tailwind CLI / PostCSS

For a production-ready workflow and to keep CSS small, use Tailwind CLI or PostCSS + tailwindcss.

#### Example Setup (Tailwind CLI)

1. Initialize npm and install dev dependencies:

```bash
npm init -y
npm install tailwindcss @tailwindcss/cli
```

2. Create an entry CSS (e.g., `src/input.css`) with:

```css
@import "tailwindcss";
```

3. Build the CSS:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

Or add convenient npm scripts in `package.json`:

```json
"scripts": {
  "dev": "npx tailwindcss -i ./src/input.css -o ./src/output.css --watch",
  "build": "npx tailwindcss -i ./src/input.css -o ./src/output.css --minify"
}
```

4. Include the built CSS in your HTML:

```html
<link rel="stylesheet" href="/src/input.css">
```

### Run Locally

1. Clone the repository:

```bash
git clone https://github.com/amansatya/x-clone.git
cd x-clone
```

2. If using the build workflow above, install dev dependencies and run `npm run dev` to generate styles.

3. Serve the folder and open it in your browser:

**Python:**

```bash
python -m http.server 8000
```

Open http://localhost:8000

**Node (http-server):**

```bash
npx http-server -p 8000
```

Open http://localhost:8000

**VS Code:**

Use the "Live Server" extension and click "Go Live".

## Project Structure

A typical structure for this repo might look like this (adjust paths to match your actual repo layout):

```
x-clone/
├── index.html              # main page (entry)
├── src/
│   ├── input.css           # Tailwind entry CSS (if using build)
│   └── output.css          # built stylesheet (generated)
├── assets/
│   └── images/             # avatars, icons, screenshots
├── package.json            # npm config (if using Node.js)
├── package-lock.json       # npm lock file (if using Node.js)
└── README.md               # this file
```

## Deployment (Optional)

This is a static HTML/CSS site and can be hosted on:

- **GitHub Pages** Push the built `index.html` and `src/output.css` to the `main` branch and enable Pages (or use `gh-pages` branch).
- **Netlify / Vercel / Cloudflare Pages** Connect the repository and configure build commands (e.g., `npm run build`) and publish the output folder.
- If using Tailwind build step, configure the build command and publish the folder containing `index.html` and `dist/`.

## Browser Support & Accessibility Notes

- Designed for modern evergreen browsers (Chrome, Firefox, Edge, Safari).
- Use semantic HTML (`<header>`, `<nav>`, `<main>`, `<article>`) to improve accessibility.
- Ensure `alt` attributes are present for images (avatars, icons).
- Test keyboard navigation and color contrast for accessibility (Tailwind's defaults are accessible but custom colors must be checked).

## Contributing

Contributions are welcome! Suggested workflow:

1. Fork the repo.
2. Create a feature branch: `git checkout -b feature/awesome-improvement`
3. Make changes and commit.
4. Open a pull request describing what you changed and why.

When opening issues or PRs, include:

- A clear title
- Steps to reproduce (if a bug)
- Screenshots or GIFs when relevant
- Browser and OS information for UI issues

## License

This repository currently does not include a license file. If you want others to be able to reuse your code, consider adding a license (for example, MIT).

To add an MIT license, create a `LICENSE` file with the MIT text and add your name and year.

## Contact

**Repository:** https://github.com/amansatya/x-clone

If you'd like, I can:
- Commit this README to the repository
- Add a `package.json` and Tailwind build config
- Add a GitHub Pages workflow or instructions for deployment
- Draft a `LICENSE` file (MIT)
- Add sample screenshots and a live demo

## Acknowledgements

- Any UI inspiration or tutorial links can go here.
- Icons: mention any icon sets used (Heroicons, Feather, Font Awesome) if present.
- **Tailwind CSS** — utility-first styling that powers the UI.