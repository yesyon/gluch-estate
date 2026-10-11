# Gluch Real Estate — Website Wireframe (Static HTML/CSS)

This is a plain, portable static site that mirrors the wireframe: 7 pages,
shared navigation/footer, and a grayscale "structural" look so the layout
and content can be reviewed before visual design.

## Files

- `index.html` — Home
- `about.html` — About Us
- `developments.html` — New Developments (listing)
- `financing.html` — Foreign Buyer Financing (the 50% + up to 20% = 70% LTV offer)
- `management.html` — Property Management service
- `market-performance.html` — Economic performance & growth in value
- `contact.html` — Contact form
- `css/styles.css` — Shared stylesheet (all layout, spacing, and component styles)

No build tools, frameworks, or dependencies — just open `index.html` in a
browser, or serve the folder with any static server.

## Suggested next steps for Claude Code

1. **Preview it**: `cd` into this folder and run a local server, e.g.
   `python3 -m http.server 8000`, then open `http://localhost:8000`.
2. **Real content**: replace every `[bracketed placeholder]` — office
   address, phone, email, team names/photos, development names, pricing,
   stats, and the market-performance figures (cite real sources).
3. **Real photography**: swap the dashed-border `.placeholder` boxes for
   `<img>` tags once photos are ready.
4. **Visual design pass**: the CSS custom properties at the top of
   `css/styles.css` (`--color-*`, `--font-family`) are the single place to
   apply a real brand palette and typography.
5. **Make the developments grid data-driven**: once there are more than a
   handful of developments, consider pulling listing cards from a small
   JSON/CSV file or a lightweight framework (Next.js, Astro, etc.) instead
   of hand-editing HTML per listing.
6. **Mobile nav**: the header nav is hidden below 900px width
   (`@media (max-width: 900px) { .main-nav { display: none; } }`) as a
   placeholder — wire up a real hamburger/mobile menu.
7. **Forms**: the contact form (`contact.html`) has no backend yet — wire
   it to an email service, CRM, or serverless function.
8. **Financing/legal copy**: have counsel review the financing-facility
   language before publishing, given it describes a lending arrangement.

## Structure notes

- Navigation and footer are duplicated across pages (plain static HTML,
  no templating). If the site grows, consider a static-site generator
  (Astro, 11ty, Next.js) so header/footer live in one shared component.
- Layout classes (`.section`, `.grid-3`, `.card`, `.stat-strip`, `.steps`,
  `.compare-table`, `.plan-card`, `.filter-bar`, `.financing-box`, etc.)
  are all defined in `css/styles.css` — reuse them for new sections rather
  than writing new inline styles.
