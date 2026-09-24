# MyWebsite

Personal portfolio site for Lorenc Zhuka (AI Engineer / Founder). Single-page,
plain HTML/CSS/JS — no build step, no dependencies, no framework.

Modeled on https://www.safeerahmad.space/ (minimalist, light, numbered sections,
card-based layout).

## Structure

```
index.html      # all markup — one page, four sections (About, Experience, Projects, Contact)
deutsche-bahn.html  # case-study subpage, linked from the Innomatik AG experience entry
css/style.css   # all styling, design tokens at the top (:root)
js/main.js      # mobile nav toggle, scroll-spy, scroll-reveal animation, footer year
assets/         # images (profile photo, etc.)
```

## Conventions

- **No build tooling.** Preview by opening `index.html` directly in a browser, or
  run a static server from this directory (`python3 -m http.server`) if you need
  proper relative-path behavior.
- **Section numbering** ("01 · About", "02 · Experience", ...) is plain text in
  each `.section__label` — when adding a new section (e.g. Services), renumber
  the labels that follow it.
- Design tokens (colors, spacing, radius) live in `:root` at the top of
  `css/style.css` — change the look from one place.
- Keep everything in this one page/style/script trio unless the site grows
  enough to justify splitting into multiple pages.

## Deployment

Live at **https://lori10.github.io/MyWebsite/** via GitHub Pages (repo:
`github.com/Lori10/MyWebsite`, public).

- Pages serves directly from the `main` branch, root path — no build step,
  no CI config needed.
- **To publish changes: just `git push` to `main`.** Pages rebuilds
  automatically within a minute or two.
- Free, no usage limits relevant to a portfolio site.
- Custom domain (optional, still free hosting): add a `CNAME` file at the
  repo root with the domain and point its DNS at GitHub Pages.

## Known placeholders to fill in

- `assets/profile.jpg` — no real photo yet; hero/about currently show a CSS
  initials avatar ("LZ").
- LinkedIn and GitHub (Contact section and Projects section links) now point
  to the real profiles/repos (linkedin.com/in/lorenc-zhuka-25b642138,
  github.com/Lori10, sourced from
  https://sites.google.com/view/lorenc-zhuka-portfolio/projects). No known
  link placeholders remain.

## Planned next steps (not yet built)

- Services / Pricing section for freelance offerings.
- Project screenshots/live demos to complement the GitHub links.
