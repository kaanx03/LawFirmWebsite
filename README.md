# Çadırcı Hukuk — Law Firm Website

A static law firm website for **Av. Abdurrahman Eray ÇADIRCI**, based in Şanlıurfa, Turkey. Built with plain HTML, CSS, and vanilla JavaScript. Deployed on [Netlify](https://www.netlify.com/).

**Live:** [hukukwebsite.netlify.app](https://hukukwebsite.netlify.app)

![screenshot](https://github.com/user-attachments/assets/bd750b7f-bdc6-45a8-8215-4675e496ebcf)

---

## Features

- **Hero section** with auto-advancing image slider
- **About section** with lawyer profile and credentials
- **Services section** — Ceza, Tazminat, Gayrimenkul, Aile, Ticaret Hukuku, Danışmanlık
- **Blog** — dynamically loaded from `blog.json`, with category filtering and detail pages
- **Contact** — WhatsApp quick-message form, Google Maps embed, office info
- **Newsletter** via Netlify Function → Telegram notification
- Mobile-first responsive design, iOS-compatible navbar

---

## Project Structure

```
hukukSitesi/
├── css/
│   ├── base.css          # CSS variables, reset, shared utilities
│   ├── components.css    # Navbar, hero, sections, footer, buttons
│   ├── responsive.css    # All media queries
│   ├── blog-styles.css   # Blog list page styles
│   └── blog-detail.css   # Blog detail page styles
├── js/
│   ├── components.js     # Loads navbar/footer HTML, initialises navigation
│   └── script.js         # All page interactivity (slider, form, blog, etc.)
├── components/
│   ├── navbar.html       # Shared navigation component
│   └── footer.html       # Shared footer + WhatsApp button component
├── images/               # Banner and blog images
├── netlify/
│   └── functions/
│       └── newsletter.js # Netlify Function — sends subscriber email to Telegram
├── index.html            # Home page
├── blog.html             # Blog list page
├── blog-detail.html      # Blog post detail page
├── blog.json             # Blog post data
└── logo.ico
```

---

## Getting Started

No build step required. Open `index.html` directly in a browser, or serve locally:

```bash
# Python
python -m http.server 8000

# Node
npx serve .
```

### Netlify Functions (newsletter)

Set the following environment variables in your Netlify dashboard:

| Variable | Description |
|---|---|
| `TELEGRAM_BOT_TOKEN` | Telegram bot API token |
| `TELEGRAM_CHAT_ID` | Chat ID to receive newsletter notifications |

---

## License

MIT License

Copyright (c) 2025 Kaan

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
