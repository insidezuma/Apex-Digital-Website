# Mntolo Agency

A modern, minimalist luxury marketing agency website built with pure HTML, CSS, and JavaScript — no frameworks, no dependencies, no build step.

![Mntolo Agency Preview](https://img.shields.io/badge/Status-Live-gold?style=flat-square) ![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

---

## Overview

**Mntolo Agency** is a digital marketing agency that specialises in helping physical retail stores build powerful online presences. This website serves as the agency's primary marketing and lead-generation platform.

### Services Featured
- Search Engine Optimisation (SEO)
- Social Media Management
- Paid Advertising (Google & Meta)
- Web Development

---

## Features

- **Zero dependencies** — pure HTML, CSS, and vanilla JS
- **Custom animated cursor** with follower effect
- **Scroll-triggered reveal animations** via IntersectionObserver
- **Sticky navigation** that transforms on scroll
- **Infinite marquee** with hover-to-pause
- **Responsive design** — mobile, tablet, and desktop
- **Contact form** with loading/success states
- **Luxury dark aesthetic** — obsidian tones with gold accents
- **Performance-first** — no JavaScript frameworks, no unused CSS

---

## Project Structure

```
mntolo-agency/
├── index.html          # Main HTML page
├── css/
│   └── style.css       # All styles (CSS variables, responsive)
├── js/
│   └── main.js         # Cursor, scroll, menu, form logic
└── README.md
```

---

## Getting Started

### Option 1 — Open directly in browser

```bash
git clone https://github.com/YOUR_USERNAME/mntolo-agency.git
cd mntolo-agency
open index.html        # macOS
# or
start index.html       # Windows
# or
xdg-open index.html    # Linux
```

### Option 2 — Local dev server (recommended)

Using Python (built-in):

```bash
# Python 3
python -m http.server 8000

# Then visit http://localhost:8000
```

Using Node.js (if installed):

```bash
npx serve .
# Then visit http://localhost:3000
```

---

## Deployment

This is a static site — it can be deployed anywhere.

### GitHub Pages (free, recommended)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your site will be live at `https://YOUR_USERNAME.github.io/mntolo-agency/`

### Netlify

1. Drag and drop the project folder at [netlify.com/drop](https://netlify.com/drop)
2. Your site is live instantly with a shareable URL

### Vercel

```bash
npx vercel
```

---

## Customisation

### Colours
All colours are CSS custom properties in `:root` inside `css/style.css`:

```css
:root {
  --obsidian:  #0a0a0a;   /* Page background     */
  --gold:      #c9a84c;   /* Primary accent       */
  --gold-light:#e2c07b;   /* Headings / italic    */
  --ivory:     #f5f0e8;   /* Primary text         */
  --text-dim:  #7a7670;   /* Secondary text       */
}
```

### Fonts
Google Fonts are loaded in `<head>` of `index.html`. Current pairing:
- **Cormorant Garamond** — headings & serifs
- **Montserrat** — body & UI text

Replace the `<link>` tag and update the `--font-serif` / `--font-sans` variables to change fonts.

### Contact Form
The form currently simulates submission with a `setTimeout`. To connect a real backend, replace the `setTimeout` block in `js/main.js` with a `fetch()` call to your preferred endpoint (e.g. Formspree, Netlify Forms, or your own API).

```js
// Example using Formspree
const response = await fetch("https://formspree.io/f/YOUR_ID", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify(Object.fromEntries(new FormData(contactForm))),
});
```

---

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome 80+ | ✅ Full |
| Firefox 80+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 80+ | ✅ Full |
| Mobile browsers | ✅ Full (cursor hidden on touch) |

---

## License

MIT License — free to use, modify, and distribute.

---

*Built with precision by Mntolo Agency.*
