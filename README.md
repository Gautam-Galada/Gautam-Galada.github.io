# Gautam-Galada.github.io

Personal site of Gautam Galada, served by GitHub Pages at <https://gautam-galada.github.io>.
Plain HTML and one stylesheet: no build step, no frameworks.

## Pages

| File | Page |
|---|---|
| `index.html` | Home: profile, research statement, bio, selected work, news |
| `research.html` | Research threads, publications, and "Things I don't know about" |
| `projects.html` | Projects, grouped by theme |
| `writing.html` | Substack essays |
| `experience.html` | Timeline of roles and education, most recent first |
| `404.html` | Not-found page |
| `articles.html` | Redirect to `writing.html` for old links |

## Assets

- `assets/style.css`: the whole design system ("Paper & Ink"): colour tokens for light and dark, type, layout, and phone styles.
- `assets/theme.js`: the light/dark toggle. The site follows the device setting until a reader presses the toggle.
- `assets/img/profile.jpg`, `assets/favicon.svg`, `assets/cv.pdf`.

## Editing

Each list has an HTML comment above it showing the block to copy:

- **News**: `index.html`, the `News` list. Most recent first.
- **Publications**: `research.html`.
- **Open questions**: `research.html`, under "Things I don't know about".
- **Projects**: `projects.html`, inside the right group.
- **Posts**: `writing.html`.
- **Roles**: `experience.html`. Add `class="now"` to an ongoing role.

## Preview locally

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy

GitHub Pages serves the `main` branch root. Push to `main` and the site updates within a few minutes.
