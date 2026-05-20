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

## Deploy

GitHub Pages is configured to serve from the `main` branch root.
Push to `main` and the site updates within a few minutes.
