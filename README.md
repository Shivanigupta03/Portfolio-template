# Portfolio Website Template

A 4-page personal portfolio template: **About Me**, **Projects**, **Research**, **Blog**.
Plain HTML/CSS/JS — no build step, no framework. Just edit the text and open the files in a browser.

## How to use this

1. **Open the site**: double-click `index.html` (it redirects to `about.html`), or open `about.html` directly.
2. **Find things to edit**: every placeholder is written in `[SQUARE BRACKETS]`, e.g. `[Your Name]`, `[Project Name]`, `[2-3 sentences describing...]`. Search each file for `[` to find every spot that needs real content.
3. **Add photos/logos**: drop your image files into `assets/images/`, then either:
   - Replace an `<img src="assets/images/logo-placeholder.png" ...>` tag's `src` with your filename, or
   - Delete a `.img-placeholder` `<div>...</div>` block entirely and replace it with an `<img>` tag (each placeholder has a comment above it showing exactly what to paste in).
4. **Add more cards/entries** (another project, award, affiliation, research paper, or blog post): find the `<!-- COPY BLOCK START -->` / `<!-- COPY BLOCK END -->` comments around the item type you want more of, copy everything between them, and paste it right after — then edit the placeholders in your new copy.
5. **Remove a card**: delete everything between its `<!-- COPY BLOCK START -->` and `<!-- COPY BLOCK END -->` comments (or the whole card `<div>` if it's a second/third copy without its own comment markers).
6. **The navbar and footer are duplicated on every page** (about.html, projects.html, research.html, blog.html, blog-post-template.html). If you change your name, links, or social handles, update it in all five files.

## File structure

```
portfolio-template/
├── index.html               → redirects to about.html
├── about.html                → About Me page (photo, bio, affiliations, awards)
├── projects.html              → Projects grid
├── research.html               → Research papers/entries list
├── blog.html                    → Blog post list
├── blog-post-template.html       → Template for a single blog post — duplicate per post
├── assets/
│   ├── css/style.css              → all styling, colors, layout
│   ├── js/main.js                  → mobile menu + auto-updating footer year
│   └── images/                      → put your photos/logos here
└── README.md
```

## Writing a new blog post

`blog.html` only lists post previews. For the full post:
1. Duplicate `blog-post-template.html`, rename it (e.g. `blog-post-my-first-hackathon.html`).
2. Fill in its title, date, cover image, and body paragraphs.
3. In `blog.html`, copy a preview card block and point its "Read More" link at your new file.

## Changing colors / fonts

All colors are defined once at the top of `assets/css/style.css` under `:root { ... }` (e.g. `--accent`, `--bg`, `--card-bg`). Change a variable there and it updates everywhere. The site currently uses a dark theme with a subtle checkered "notebook grid" texture behind the content (set on the `body` rule in the same file).

## Publishing it for free

The easiest option is **GitHub Pages**:
1. Push this folder to a GitHub repository.
2. Go to the repo's Settings → Pages → set the source branch to `main` (root folder).
3. Your site will be live at `https://[your-username].github.io/[repo-name]/`.
