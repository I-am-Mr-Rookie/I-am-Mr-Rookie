# Frontend notes

## What existed before

No frontend. This is a GitHub profile repository: just `README.md` (the profile shown on github.com/I-am-Mr-Rookie) and `REVIEW_FIXES.md`. It had no HTML, templates, framework, package manifest or build step.

## What was created

- `docs/index.html`: a single static profile page. There are no dependencies, no build step and no JavaScript. It has the same content as `README.md`: intro, the two featured projects (AgriSense, PDF → LaTeX), how I build, tools, and collaborate.
  - **Location:** `docs/` because GitHub Pages can publish straight from `main` → `/docs`.
  - **Design:** a warm editorial look. Body text is Crimson Pro and the header and labels are Source Code Pro, both loaded from Google Fonts with system fallbacks. The page uses a narrow reading width, thin divider lines, and a button with a hard offset shadow.
  - **Responsive:** one column with a fluid title size. The project detail rows (focus, stack, start) stack on narrow screens.
  - **Accessibility:** skip link, landmark elements, labelled sections and nav, visible focus outlines, and support for `prefers-reduced-motion`. Light and dark palettes follow `prefers-color-scheme`, and every text/background pair meets WCAG AA (lowest is 5.6:1).
- `FRONTEND_NOTES.md`: this file.

`README.md` was not changed. If you edit the README, update `docs/index.html` by hand too; nothing keeps them in sync.

## How to run

Open `docs/index.html` in a browser, or serve it:

```sh
python3 -m http.server -d docs 8000   # then visit http://localhost:8000
```

To publish: repo **Settings → Pages → Deploy from a branch → `main` / `/docs`**.
