# Follow-up prompt — paste into your ACTIVE Claude Code session (do not start a new one)

The overall structure you built is good. I now have specific updates to the design system, the Articles page layout, and the Projects page layout. Do NOT rebuild from scratch — modify the existing files only.

---

## 1. DESIGN SYSTEM OVERHAUL — update assets/style.css entirely

Replace all font and color rules with the following. These apply globally across all pages.

### Fonts
Import from Google Fonts at the top of style.css:
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Lora:ital,wght@0,400;0,600;1,400&family=Hind+Madurai:wght@300;400;500&display=swap');

Apply as follows:
- Headings (h1, h2, h3, nav links, page section anchors): font-family: 'Montserrat', sans-serif; font-weight: 600;
- Subheadings (h4, h5, article titles, project titles, section labels like "Short Bio:", "News"): font-family: 'Lora', serif;
- Body text, descriptions, meta info, news list items, bio paragraph, idea entries: font-family: 'Hind Madurai', sans-serif; font-weight: 400;
- Name "Gautam Galada" on homepage: Montserrat, weight 700

### Colors
- Page background: #FAF8F5  (warm off-white, not pure white)
- Body text: #1A1A1A
- Section dividers / hr / card borders: #E3DAC9
- Subtle backgrounds (card bg, tag bg): #F5F5F5
- Link color: #2A5DB0  (readable blue, not browser default)
- Link hover: #1A3F80
- Nav active link: Montserrat bold, color #1A1A1A, border-bottom: 2px solid #E3DAC9
- Muted/meta text (.meta, captions, dates): #666666
- Tag pill text: #444444, background: #F5F5F5, border: 1px solid #E3DAC9

### Borders and dividers
- All <hr> tags: border: none; border-top: 1px solid #E3DAC9; margin: 24px 0;
- All card borders: 1px solid #E3DAC9; border-radius: 10px;
- No drop shadows anywhere

---

## 2. ARTICLES PAGE — replace articles.html layout completely

The article card layout must replicate the visual structure of Substack's own post list (see my screenshot):

Each article entry is a horizontal card with:
  LEFT side (~70% width): text block
    - Article title: Lora font, ~18px, bold, color #1A1A1A — this is the clickable link (opens in new tab)
    - Subtitle/description: Hind Madurai, ~14px, color #444, 2 lines max, display below title
    - Bottom row: "GAUTAM GALADA · X MIN READ · DATE" — Hind Madurai, 11px, uppercase, color #888, letter-spacing: 0.05em
  RIGHT side (~30% width): thumbnail image
    - <img> placeholder pointing to assets/thumbs/article1.jpg (I will replace)
    - Fixed size: ~160px wide, ~110px tall, object-fit: cover, border-radius: 6px
    - If no image, hide the right column gracefully

Between cards: a 1px #E3DAC9 horizontal rule

The cards themselves have no background fill — they sit on the page background directly, just like Substack.

On mobile (<600px): stack image below text, image goes full width.

Pre-populate with these real articles (I will keep adding more manually):

Article 1:
  Title: Adam and … Muon! (a geometric view)
  Subtitle: So, what's all the buzz about Muon (MomentUm Orthogonalized by Newton-Schulz)?
  URL: [PLACEHOLDER — add your Substack URL for this post]
  Read time: 5 MIN READ
  Date: [PLACEHOLDER]
  Thumb: assets/thumbs/article1.jpg

Article 2:
  Title: MYTH: "Some Languages are Spoken More Quickly Than Others"
  Subtitle: From my Orthoepy class......
  URL: [PLACEHOLDER]
  Read time: 2 MIN READ
  Date: MAY 20
  Thumb: assets/thumbs/article2.jpg

Article 3:
  Title: Understanding Translational Equivariance and Invariance in Convolutional Neural Networks (CNNs)
  Subtitle: The view is always a retrospect
  URL: [PLACEHOLDER]
  Read time: 2 MIN READ
  Date: MAY 20
  Thumb: assets/thumbs/article3.jpg

Article 4:
  Title: A Boring Weekend and Some Caffeine
  Subtitle: Might as well look at NLA (Natural Language Autoencoder)
  URL: https://substack.com/@gautamgalada1/note/p-198615843?utm_source=notes-share-action&r=5z100e
  Read time: 11 MIN READ
  Date: MAY 10
  Thumb: assets/thumbs/article4.jpg

Create the assets/thumbs/ folder with a .gitkeep. Add this HTML comment at the top of the article list:
<!-- TO ADD AN ARTICLE: copy one .article-card block, update title, subtitle, url, read-time, date, and thumb src. Place thumbnail in assets/thumbs/. -->

---

## 3. PROJECTS PAGE — replace the project layout sections

### Section A — Pinned Projects
Layout: 3-column CSS grid on desktop, 1-column on mobile.
Each pinned project card (matching my wireframe — image on top, description below):
  - Outer card: border: 1px solid #E3DAC9; border-radius: 10px; overflow: hidden; background: #FAF8F5;
  - TOP HALF: project screenshot/image placeholder — full width of card, ~180px tall, object-fit: cover, background: #F5F5F5 if no image
  - BOTTOM HALF (inside card, padding 12px):
    - Project name: Lora font, bold, link to GitHub repo (new tab)
    - One-line description: Hind Madurai, 13px, color #444
    - Tag pills: small inline spans, Hind Madurai 11px, background #F5F5F5, border 1px solid #E3DAC9, border-radius: 4px, padding: 2px 7px

Placeholder entries (3 cards):
  Card 1: "Project Alpha" → https://github.com/Gautam-Galada · "Description placeholder." · tags: [Python] [ML]
  Card 2: "Project Beta" → https://github.com/Gautam-Galada · "Description placeholder." · tags: [Research]
  Card 3: "Project Gamma" → https://github.com/Gautam-Galada · "Description placeholder." · tags: [NLP] [Open Source]

Image placeholders: assets/projects/pin1.jpg, pin2.jpg, pin3.jpg — create the folder with .gitkeep.

### Section B — Recent Projects
Layout: vertical list of horizontal cards (image left, description right) — exactly matching the bottom section of my wireframe.
Each row card:
  - border: 1px solid #E3DAC9; border-radius: 10px; display: flex; overflow: hidden;
  - LEFT: project image, ~160px wide, object-fit: cover, background: #F5F5F5 if no image
  - RIGHT (padding 16px):
    - Project name: Lora bold, link to GitHub (new tab)
    - Description: Hind Madurai 14px, color #444
    - Tags: same pill style as pinned cards
    - Date: Hind Madurai 12px, color #888, bottom of right section

3 placeholder row entries using same format. Image placeholders: assets/projects/proj1.jpg etc.

### Section C — Ideas (no layout change needed, just font/color update to match new design system)
Update font to Hind Madurai for idea entries, Lora for the section subheading, Montserrat bold for "Ideas & Thoughts" heading.
Date prefix: Montserrat 12px, color #888.

---

## 4. GLOBAL NAV update
Nav links: Montserrat 600 weight, font-size 14px, letter-spacing: 0.03em, color #1A1A1A, text-decoration: none.
Active page link: border-bottom: 2px solid #E3DAC9; color: #1A1A1A;
Hover: color: #2A5DB0;
Nav container: border-bottom: 1px solid #E3DAC9; padding-bottom: 12px; margin-bottom: 28px;

---

## 5. VERIFICATION after changes
1. Open articles.html — confirm cards match Substack-style layout with image on right
2. Open projects.html — confirm 3-column pinned grid and horizontal row cards below
3. Confirm all three Google Fonts load (check browser network tab or just visually inspect)
4. Confirm all #E3DAC9 borders are consistent across cards, hr, and nav
5. Mobile check at 600px: articles stack to text-only (image below), project grid goes to 1 column