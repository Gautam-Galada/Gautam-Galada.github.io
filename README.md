# Gautam-Galada.github.io

Personal portfolio site for Gautam Galada, hosted via GitHub Pages at [Gautam-Galada.github.io](https://Gautam-Galada.github.io).

## Structure

```
index.html          Home — profile, bio, news, quick links
articles.html       Articles — Substack writing
projects.html       Projects Garage — pinned projects, recent work, ideas log
gallery.html        Gallery — photos and longer reads
assets/
  style.css         Single shared stylesheet
  profile_placeholder.svg  Placeholder profile image (replace with profile.jpg)
  news.gif          Animated icon for news section
  photos/           Place gallery photos here
```

## Editing

- **Add news**: Edit `index.html`, find the `<!-- ADD NEW NEWS ITEMS HERE -->` comment.
- **Add articles**: Edit `articles.html`, copy the `article-item` block template in the comments.
- **Add projects**: Edit `projects.html`, follow the comments in each section.
- **Add photos**: Drop images into `assets/photos/`, then add a `<figure>` block in `gallery.html`.
- **Replace profile photo**: Save your photo as `assets/profile.jpg` and update the `<img src>` in `index.html`.

## Local Dashboard

To manage site content locally without editing HTML by hand:

```
node server.js
```

Then open **http://localhost:3001** in your browser.
Fill in the form → click **Save to site** → the HTML file updates on disk immediately.

When you're ready to publish:

```
git add .
git commit -m "your message"
git push origin main
```

> `dashboard.html`, `server.js`, and `package.json` are listed in `.gitignore` and are never pushed to GitHub.

## Deploy

GitHub Pages is configured to serve from the `main` branch root.
Push to `main` and the site updates within a few minutes.
