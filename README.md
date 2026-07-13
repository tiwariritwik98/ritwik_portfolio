# Palak Makhija — Portfolio

Personal portfolio site for Palak Makhija (UI/UX Designer), plus two case studies.
Plain static HTML/CSS/JS — no build step, no framework. Hosted on GitHub Pages.

## Structure

```
index.html              ← the portfolio (edit this directly)
neighborly.html         ← Neighborly case study
sarpanch-samvaad.html   ← Sarpanch Samvaad case study
assets/
  img/                  ← images (covers, hover screenshots, texture)
  fonts/                ← Archivo Black, Space Grotesk, Space Mono (self-hosted)
  js/                   ← gsap + scrolltrigger (animation), image-slot, dc-runtime
.nojekyll               ← tells GitHub Pages to serve files as-is
```

Which image is which:
- `img/proj-1-cover-v2.png` — Neighborly card cover
- `img/proj-2-cover-v3.png` — Sarpanch Samvaad card cover
- `img/hero-cta-mic.png` — hero image
- `img/shot-nb-*.png` — Neighborly hover-preview screenshots
- `img/shot-chaupal / -schemes / -learning / -newpost.png` — Sarpanch hover-preview screenshots

## Editing

Everything on the page is normal HTML in `index.html`:

- **Text** (bio, project names, experience, etc.) — edit it directly in `index.html`.
- **Links** — e.g. the project cards use `href="neighborly.html"` / `href="sarpanch-samvaad.html"`; email/social links are in the contact section.
- **Images** — drop a replacement into `assets/img/` using the **same filename**, or change the `src` / `data-shots` reference.
- **Accent colour / theme** — near the bottom of `index.html` there's a `<script type="text/x-dc" data-props="...">` tag holding `theme` (dark/light) and `accent` colour. Change the values there.

> The two case-study files (`neighborly.html`, `sarpanch-samvaad.html`) are still single-file exports (all their content is packed inside). They render perfectly but aren't hand-editable the way `index.html` is — ask to have them de-bundled too if you want to edit them directly.

## Preview locally

Just open `index.html` in a browser. For a 100%-accurate preview (matching the hosted site), serve the folder over HTTP, e.g.:

```
python -m http.server      # then visit http://localhost:8000
# or
npx serve
```

## Publish / update (GitHub Pages)

After the repo is on GitHub with Pages enabled, updating the live site is:

```
git add -A
git commit -m "Update portfolio"
git push
```

The site rebuilds automatically within a minute or so.
