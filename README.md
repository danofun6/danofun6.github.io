# Canon Stone Website

Static website for [Canon Stone](https://www.peakconsults.com) — operations and technology advisory.

## Deployment (GitHub Pages)

### Setup

1. Push this repo to GitHub as `<username>.github.io`
2. The site auto-deploys from `master` branch root — no configuration needed for `*.github.io` repos

### Custom Domain (Cloudflare)

The site is served via Cloudflare with a custom domain. Update the `CNAME` file with your domain.

**DNS Records in Cloudflare:**

| Type  | Name  | Content                        |
|-------|-------|--------------------------------|
| CNAME | www   | `<username>.github.io`         |
| CNAME | @     | `<username>.github.io`         |

> If using Cloudflare proxy (orange cloud), SSL mode should be set to **Full** or **Full (Strict)**.

### File Structure

```
├── index.html        # Home page
├── services.html     # Services page
├── about.html        # About page
├── contact.html      # Contact page
├── CNAME             # Custom domain for GitHub Pages
├── css/
│   └── style.css     # All styles
└── js/
    └── main.js       # Mobile nav, animations, form handler
```

### Tech Stack

- Pure HTML/CSS/JS — no frameworks, no build step
- Source Serif 4 + Inter (Google Fonts)
- Mobile responsive, accessibility-focused (skip link, ARIA, focus rings)
- Editorial typography with drop caps, Roman numerals, and hairline rules
- Contact form via [Formspree](https://formspree.io)

### Local Development

Open `index.html` in a browser, or serve locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
