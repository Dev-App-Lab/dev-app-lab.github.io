# Apps landing page

A single static landing page showcasing all my iOS apps. No build tools —
just `index.html` and `css/style.css`.

## Preview locally

Open `index.html` in a browser, or run a tiny server:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Editing apps

Each app is one `<a class="card">…</a>` block inside the `.grid` div in `index.html`.
To add a new app, copy a card and update:

- the App Store `href`
- the icon `src` (get the 512px icon from `https://itunes.apple.com/lookup?id=APP_ID`, field `artworkUrl512`)
- the tag, name, and description

## Deploying

Any static host works:

- **GitHub Pages** — push this repo to GitHub, then Settings → Pages → deploy from `main`.
- **Netlify / Vercel / Cloudflare Pages** — connect the repo; no build command, output dir is the repo root.

To use a custom domain, add it in your host's settings and point the DNS
(A/CNAME records) as instructed.
