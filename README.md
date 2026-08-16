# SEO-AGENT Site Workspace

Local mirror of the GitHub repo `qari1001cc1-creator/Seo-Agent`.

Deployed live on Netlify: `https://seo-agent-me1.netlify.app/`

## Structure

```
site_workspace/              <- = repo root (eo-agent-site)
├── test_site/               <- Netlify publish directory (the actual website)
│   ├── index.html           PERFECT control page
│   ├── about.html           missing meta description (test issue)
│   ├── services.html        title > 60 chars + thin content (test issue)
│   ├── contact.html         missing H1 (test issue)
│   ├── blog/top-10-seo-tips.html      PERFECT blog page
│   ├── blog/web-design-trends.html    duplicate title + no-alt image + broken link
│   ├── privacy.html         very thin content (test issue)
│   ├── 404.html             custom 404 page
│   ├── sitemap.xml          all page URLs
│   ├── robots.txt           allow all + sitemap
│   ├── _redirects           pretty URLs for Netlify
│   ├── css/style.css        dark premium theme
│   └── assets/*.svg         images
├── DEPLOY.txt               Netlify deploy + SEO-AGENT linking guide
├── .gitignore
└── README.md
```

## Netlify settings
- **Publish directory**: `test_site`  (so the root `/` serves the homepage)
- **Build command**: none (static site)

## How SEO-AGENT edits this site
The Website Editor module (publisher.py) uses the GitHub API to:
1. Generate change proposals (new blog posts, SEO issue fixes, keyword updates)
2. Show them in the dashboard with diff previews
3. After confirmation -> commit + push to this repo
4. Netlify auto-redeploys -> changes go live

Keep this folder in sync with the GitHub repo. The dashboard compares local vs GitHub before publishing.