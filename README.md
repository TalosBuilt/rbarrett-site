# rbarrett.co

Personal portal site. Static HTML/CSS/JS. Deployed via GitHub Pages.

## Access Tiers

| Tier | Path | Deployed | Indexed |
|---|---|---|---|
| Public | `/`, `/projects/` | Yes | Yes |
| Semi-private | `/p/*` | Yes | No (robots.txt + noindex) |
| Private | — | Never | Never |

Semi-private pages are non-indexed static placeholders. They are not secure.
Do not place sensitive information on any deployed page.

## Structure

```
rbarrett-site/
├── index.html           # Public portal home
├── style.css            # Shared stylesheet
├── script.js            # Minimal JS
├── robots.txt           # Disallow /p/ from crawlers
├── assets/img/          # Images and static assets
├── projects/
│   └── index.html       # Public project listing
└── p/                   # Semi-private placeholders (not indexed)
    ├── pat/index.html
    ├── ku/index.html
    └── fam/index.html
```

## Deployment

GitHub Pages → root of `main` branch. Custom domain: `rbarrett.co`.

No build step. No dependencies. Push and done.

## Content Rules

- Tier 1 public pages: only information safe to be permanently public.
- Tier 2 /p/ pages: treat as readable by anyone with the URL. No sensitive content.
- Private operational content stays off this repo entirely.
