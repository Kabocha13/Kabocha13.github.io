# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **static website** (a Japanese portfolio plus standalone HTML games/quizzes). There is no build system, package manager, backend, or dependency manifest — every page is a single self-contained `.html` file with inline CSS/JS. External libraries (Tailwind CDN, AOS, Google Fonts) are loaded from CDNs at runtime, so an internet connection is needed for full styling.

### Pages
- `index.html` — portfolio homepage (`下田一颯 - Portfolio`); links out to the other pages/projects.
- `economics_quiz_platform_single.html`, `keizai2026-05.html`, `tishiki2026-06.html` — interactive quiz/exam platforms.
- `play.html`, `3045.html` — standalone games/tools.
- `AI-NATIONAL-LAB.md` — legal text (privacy policy / terms) for a separate app; not part of the site.

### Run (development)
Serve the repo root with any static file server, then open a page in the browser:

```
python3 -m http.server 8000
# then visit http://localhost:8000/index.html
```

There is nothing to install. The site is published via GitHub Pages, so treat the repo root as the web root.

### Lint / test / build
There are **no** lint, test, or build steps — this is plain static HTML. Verify changes by loading the affected page in a browser and interacting with it.
