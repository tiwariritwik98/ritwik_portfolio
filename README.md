# Ritwik Tiwari — Portfolio

Personal portfolio site for Ritwik Tiwari (PMO Analyst · Program Governance & Delivery).
Plain static HTML/CSS/JS — no build step, no framework. Hosted on GitHub Pages.

## Structure

```
index.html              ← the portfolio (edit this directly)
neighborly.html         ← unused legacy case study (not linked from the site)
sarpanch-samvaad.html   ← unused legacy case study (not linked from the site)
assets/
  img/                  ← images (covers, hero photo, texture)
  fonts/                ← Archivo Black, Space Grotesk, Space Mono (self-hosted)
  js/                   ← gsap + scrolltrigger (animation), image-slot, dc-runtime
.nojekyll               ← tells GitHub Pages to serve files as-is
```

Which image is which:
- `img/proj-2-cover-v3.png` — Sarpanch Samvaad section cover
- `WhatsApp Image 2026-07-07 at 2.36.37 PM.jpeg` — hero photo (referenced directly from `index.html`)
- `img/hero-cta-mic.png`, `img/proj-1-cover-v2.png`, `img/shot-*.png` — leftover assets from the original template, no longer referenced

## Editing

Everything on the page is normal HTML in `index.html`:

- **Text** (bio, experience, skills, AI tools, etc.) — edit it directly in `index.html`.
- **AI Portfolio links** — in the `#ai-tools` section, each tool is an `<a class="tool" href="...">`.
- **Links** — email/phone/social links are in the contact section near the bottom.
- **Images** — drop a replacement into `assets/img/`, or change the `src` reference.
- **Accent colour / theme** — near the bottom of `index.html` there's a `<script type="text/x-dc" data-props="...">` tag holding `theme` (dark/light) and `accent` colour. Change the values there.

> `neighborly.html` and `sarpanch-samvaad.html` are legacy single-file exports from the original template (all their content is packed inside a compressed bundle). They aren't linked from `index.html` and aren't hand-editable — safe to ignore or delete.

## Preview locally

Just open `index.html` in a browser. For a 100%-accurate preview (matching the hosted site), serve the folder over HTTP, e.g.:

```
npx serve      # then visit the printed local URL
```

## Publish / update (GitHub Pages)

After the repo is on GitHub with Pages enabled, updating the live site is:

```
git add -A
git commit -m "Update portfolio"
git push
```

The site rebuilds automatically within a minute or so.
