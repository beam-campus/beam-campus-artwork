# BEAM Campus — Social Media Assets

Open Graph images, banners, and platform-specific graphics.

## Structure

| Subdirectory | Purpose |
|-------------|---------|
| `og-images/` | Open Graph images for link previews (Twitter, LinkedIn, Slack, etc.) |
| `banners/` | Site banners, hexdocs banners, email headers |
| `twitter/` | Twitter / X profile images, headers, tweet cards |
| `linkedin/` | LinkedIn profile images, cover, article banners |

## Specifications

### Open Graph images (og-images/)

- **Dimensions:** 1200 × 630 pixels
- **Format:** PNG with transparency OR JPG
- **File size:** < 1 MB ideally, < 5 MB hard limit
- **Safe area:** content within centre 1000 × 524 pixels (some platforms crop)

Naming:

```
og-{project}-{purpose}.png

Examples:
og-macula-homepage.png
og-reckondb-hex-package.png
og-beam-campus-fosdem-talk.png
```

### Site banners (banners/)

- **Homepage hero:** 2400 × 1200 (retina), 1200 × 600 fallback
- **Blog post header:** 1200 × 400
- **Hexdocs package header:** 1024 × 256 (optional)

### Twitter / X (twitter/)

- **Profile image:** 400 × 400 square
- **Header image:** 1500 × 500
- **Tweet card (large):** 1200 × 628

### LinkedIn (linkedin/)

- **Profile image:** 400 × 400 square
- **Cover photo:** 1584 × 396
- **Article banner:** 1200 × 627
- **Company page cover:** 1128 × 191 (4K recommended)

## Brand application

Every social asset must include:

- BEAM Campus or project logo (appropriate variant from `../logos/`)
- Primary typography (Fraunces for display, Inter for body — per `../brand/fonts/`)
- Brand palette (sovereign blue primary, accent per project — per `../brand/palette/tokens.md`)

## Templates

Templates to be added as they're created. Use cases to build templates for:

- [ ] Generic "announcement" OG image (version release, blog post)
- [ ] Generic "talk" OG image (conference, podcast)
- [ ] Project-specific release OG (Macula v1.2, ReckonDB v2.0, etc.)
- [ ] "Hiring" OG (consulting availability, job posts)
- [ ] Event promotional (FOSDEM, CodeBEAM, NLnet review)

## Generating

Use `source/` files for template origins:

- `source/svg/og-template-*.svg` — editable SVG templates
- Export to PNG at specified dimensions

Command-line export (Inkscape):

```bash
inkscape source/svg/og-macula-homepage.svg \
  --export-type=png \
  --export-filename=og-images/og-macula-homepage.png \
  --export-width=1200 --export-height=630
```

## Accessibility

- Alt text guidance: when embedding in HTML, provide descriptive alt
- Text in social images: keep main title ≥ 36pt equivalent at 1200×630
- Contrast: minimum 4.5:1 for any text over background

## Status

Empty scaffold — assets to be added.
