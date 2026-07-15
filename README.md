# rachelmakes.store

Static site hosted on GitHub Pages: embeds a JotForm on the home page and
serves simple redirect pages.

## Structure

| File | Purpose |
|---|---|
| `index.html` | Home page with the embedded JotForm |
| `redirect-template.html` | Copy this to add a new redirect (instructions inside) |
| `404.html` | Shown for unknown URLs |
| `CNAME` | Tells GitHub Pages to serve the site at rachelmakes.store |

## Adding a redirect

To make `rachelmakes.store/instagram` redirect somewhere:

1. Create a folder named `instagram` with a copy of `redirect-template.html`
   renamed to `index.html` (i.e. `instagram/index.html`).
2. Replace `https://example.com` with the destination URL in all three places.
3. Commit and push — live in about a minute.

## One-time setup

### 1. Enable GitHub Pages

On GitHub: **Settings → Pages → Build and deployment**, set Source to
"Deploy from a branch", branch `main`, folder `/ (root)`. Save.

### 2. Point the domain (Squarespace)

In Squarespace: **Settings → Domains → rachelmakes.store → DNS Settings**,
add these records:

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | jfbisson4.github.io |

Delete any existing A/CNAME records on `@` and `www` that point to
Squarespace, or they will conflict.

### 3. Turn on HTTPS

Back in GitHub **Settings → Pages**: once the custom domain shows a green
check (DNS can take up to an hour to propagate), tick **Enforce HTTPS**.
