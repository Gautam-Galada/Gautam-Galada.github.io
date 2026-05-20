# Claude Code Prompt — Gautam-Galada.github.io
# Save this file and paste the contents into your Claude Code terminal session.
# Run from inside your local repo folder: ~/Gautam-Galada.github.io

---

You are building my personal portfolio website hosted at Gautam-Galada.github.io. The GitHub repo is already initialized and connected to my GitHub account. Build the entire site from scratch using only pure HTML, CSS, and minimal vanilla JavaScript. No React, no Next.js, no build tools, no npm — static files only, deployable directly via GitHub Pages.

<inspiration>
My professor's site: https://hengfan2010.github.io/
Study this site carefully before writing a single line of code. Fetch and read its HTML source.

Here is exactly what that site does that I want to replicate:
- Top horizontal nav bar with plain text links, no styling flourishes
- Two-column layout on the home page: photo on left, name/title/links on right
- A horizontal <hr> rule separating each section
- Bold section headers like "Short Bio" and "News" inline with content (not big headings)
- News items as a simple <ul> bullet list with dates prefixed in plain text (e.g. "2026-05: ...")
- A small animated GIF icon next to the "News" heading
- All links are plain blue underlined — no custom button styling
- Footer-area "Quick Links" section: plain inline links separated by spaces
- Font: system default — no web font imports whatsoever
- Background: pure white. Text: near-black. Zero decorative elements.
- Max width ~900px centered. Left-right padding ~20px.
- One shared CSS file. No JS except possibly a mobile nav toggle.
The goal is to look like a serious researcher/builder's site — clean, fast, no nonsense.
</inspiration>

<about_me>
Name: Gautam Galada
GitHub: https://github.com/Gautam-Galada
Substack: https://substack.com/@gautamgalada1
LinkedIn: [PLACEHOLDER — add your LinkedIn URL here]
Twitter/X: [PLACEHOLDER — add your Twitter/X URL here]
Email: [PLACEHOLDER — add your email here]
Affiliation/Title: [PLACEHOLDER — e.g. "MS Student, Georgia Tech"]
Bio: [PLACEHOLDER — write 2-3 sentences about yourself, your interests, and what you're working on]
CV: Will be placed at assets/cv.pdf
</about_me>

<file_structure>
Create exactly this structure at the repo root:

  index.html              ← Home
  articles.html           ← Articles (Substack)
  projects.html           ← Projects Garage
  gallery.html            ← Gallery
  assets/
    style.css             ← Single shared stylesheet for all pages
    profile.jpg           ← I will replace this; create an SVG placeholder for now
    photos/               ← Empty folder with a .gitkeep file
  README.md               ← Brief description of the site
</file_structure>

<nav>
Every page must have the same top navigation bar, identical to the professor's style:
  Home | Articles | Projects Garage | Gallery
Each link points to the corresponding .html file.
The currently active page's link should be bold or underlined to indicate active state.
No hamburger menus, no dropdowns — plain horizontal links.
</nav>

<pages>

## PAGE 0 — index.html (Home)

Layout exactly mirrors the professor's home page:

SECTION 1 — Two-column profile block:
  LEFT: Profile photo
    <img src="assets/profile.jpg" alt="Gautam Galada" style matching professor's photo size>
    Create a gray SVG placeholder at assets/profile_placeholder.svg and use it as src until I replace it.
  RIGHT: 
    Name: Gautam Galada (bold, slightly larger)
    Title/Affiliation: [PLACEHOLDER]
    Email: [PLACEHOLDER]
    Links on separate lines, plain text with hyperlinks:
      [Curriculum Vitae] → assets/cv.pdf
      [LinkedIn] → PLACEHOLDER URL
      [Twitter/X] → PLACEHOLDER URL  
      [GitHub] → https://github.com/Gautam-Galada
      [Substack] → https://substack.com/@gautamgalada1

<hr>

SECTION 2 — Short Bio:
  Bold inline label: "Short Bio:" followed by paragraph text.
  Use this placeholder: "Gautam Galada is a [PLACEHOLDER — title/role] at [PLACEHOLDER — institution]. His interests include [PLACEHOLDER]. He writes about [PLACEHOLDER] on Substack and builds [PLACEHOLDER] projects on GitHub."

<hr>

SECTION 3 — News (with small animated icon next to heading, like the professor uses):
  Bold label: "News"
  Unordered list of 10 items max, most recent first.
  Each item format: YYYY-MM: Description with links where relevant.
  Pre-populate with these 3 sample placeholder items (I will edit them):
    - 2026-05: Started building my personal website.
    - 2026-04: Published first article on [Substack](https://substack.com/@gautamgalada1).
    - 2026-03: [PLACEHOLDER — add a recent achievement, project, or event here].
  Add a clear HTML comment: <!-- ADD NEW NEWS ITEMS HERE, MOST RECENT FIRST. FORMAT: <li>YYYY-MM: Your update text with optional <a href="">links</a>.</li> -->

<hr>

SECTION 4 — Quick Links:
  Plain inline links separated by spaces/bullets, no list styling:
  GitHub | Substack | LinkedIn | Twitter/X

---

## PAGE 1 — articles.html (Articles)

This page lists my Substack articles. No iframes, no embeds — just clean links.

Page heading: "Articles"
Subheading (small, muted): "Writing on Substack — click any title to read."

Display each article as a simple block:
  [Title] ← hyperlink, opens in new tab (_blank)
  Date · One-line description

Pre-populate with ONE real example:
  Title: "A Sample Note"
  URL: https://substack.com/@gautamgalada1/note/p-198615843?utm_source=notes-share-action&r=5z100e
  Date: 2026-05
  Description: [PLACEHOLDER — add a one-line description of what this article is about]

Add a clear HTML comment:
<!-- TO ADD A NEW ARTICLE: Copy the block below and update title, url, date, and description.
<div class="article-item">
  <a href="SUBSTACK_URL" target="_blank" rel="noopener">Article Title</a>
  <span class="meta">YYYY-MM · One-line description</span>
</div>
-->

---

## PAGE 2 — projects.html (Projects Garage)

Three sections separated by <hr> rules:

SECTION A — Pinned Projects
  Heading: "Pinned Projects"
  2-3 project cards (simple bordered boxes or just bolded entries), each with:
    - Project name (links to GitHub repo, opens in new tab)
    - One-line description
    - Tags in brackets: [Python] [ML] etc.
  Placeholder entries:
    1. "Project Alpha" → https://github.com/Gautam-Galada · "Description placeholder." · [Python]
    2. "Project Beta" → https://github.com/Gautam-Galada · "Description placeholder." · [Research]

SECTION B — Recent Projects
  Heading: "Recent Projects"
  A plain list, most recent first, format: YYYY-MM — [Project Name](GitHub link) — one-line description
  3 placeholder entries.

SECTION C — Ideas
  Heading: "Ideas & Thoughts"
  Subheading: "A running log of ideas, hypotheses, and half-baked thoughts."
  Plain dated list, most recent 10, format: YYYY-MM-DD — Idea text.
  3 placeholder entries:
    - 2026-05-01 — [PLACEHOLDER idea]
    - 2026-04-15 — [PLACEHOLDER idea]
    - 2026-03-20 — [PLACEHOLDER idea]

Add clear HTML comments in each section explaining how to add new entries.

---

## PAGE 3 — gallery.html (Gallery)

Two sections:

SECTION A — Photos
  Heading: "Photos"
  CSS grid, 3 columns on desktop, 1 column on mobile.
  Each item: <img> with caption below.
  3 placeholder entries pointing to assets/photos/photo1.jpg, photo2.jpg, photo3.jpg.
  Add comment: <!-- TO ADD A PHOTO: copy an <figure> block, place your image in assets/photos/, update src and caption -->

SECTION B — Blog Posts
  Heading: "Longer Reads"
  Simple link list, same style as articles page.
  2 placeholder entries.
  Add comment explaining how to add entries.

</pages>

<css_requirements>
Single file: assets/style.css, linked from every HTML page.

Rules to follow exactly:
- background: #ffffff
- body text color: #111111
- font-family: Georgia, 'Times New Roman', Times, serif for body (academic feel, like many professor sites)
- font-size: 15px base
- Links: standard blue #0000EE, visited #551A8B — no custom link styling, just like a real academic site
- max-width: 900px on the content wrapper, centered with margin: 0 auto
- padding: 0 20px
- nav: horizontal, space-separated links at the top, padding-bottom: 10px, border-bottom: 1px solid #ccc
- hr: simple 1px solid #ccc
- .two-col: display: flex, gap: 30px, align-items: flex-start
- .two-col img: max-width: 180px, height: auto
- ul in news section: padding-left: 20px, line-height: 1.8
- @media (max-width: 600px): .two-col becomes flex-direction: column
- No box shadows, no border-radius on images, no gradients, no animations (except the news GIF icon)
- article-item and project entries: display: block, margin-bottom: 16px
- .meta: color: #555, font-size: 0.9em, display: block, margin-top: 2px
- photo grid: display: grid, grid-template-columns: repeat(3, 1fr), gap: 12px
- figure: margin: 0, figcaption: font-size: 0.85em, color: #555, text-align: center, margin-top: 4px
</css_requirements>

<github_instructions>
After building all files locally:
1. Stage all files: git add .
2. Commit: git commit -m "Initial site build — all 4 pages"
3. Push: git push origin main

Make sure the repo has GitHub Pages enabled on the main branch (Settings → Pages → Deploy from branch → main → / (root)).
The site will be live at https://Gautam-Galada.github.io within a few minutes of pushing.
</github_instructions>

<placeholders_to_fill_before_first_push>
Before pushing, search the codebase for [PLACEHOLDER] and fill in:
1. Your email address
2. Your LinkedIn URL
3. Your Twitter/X URL
4. Your title and affiliation (e.g. "MS Student, Georgia Tech")
5. Your bio paragraph
6. Replace assets/profile.jpg with your actual photo (same filename)
7. Your first 3 news items
8. Your first real article description on the Articles page

Do NOT block on these — build the full site first with placeholders clearly marked, then list all placeholder locations at the end so I can fill them in.
</placeholders_to_fill_before_first_push>

<verification>
After building, do the following to verify:
1. Open index.html in a browser locally and confirm the two-column layout renders correctly
2. Click every nav link and confirm all 4 pages load
3. Click the sample Substack article link and confirm it opens in a new tab
4. Click the GitHub links and confirm they open in a new tab
5. Resize browser to <600px width and confirm the home page stacks to single column
6. Run: grep -r "PLACEHOLDER" . to list all unfilled placeholders and print them
</verification>