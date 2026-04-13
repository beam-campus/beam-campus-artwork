# Contributing to BEAM Campus Artwork

Thanks for considering a contribution. This repository is the central store for visual identity, diagrams, and brand assets across the BEAM Campus ecosystem.

## Before you start

Check the project's [`README.md`](./README.md) for repository layout and conventions. Open an issue before large contributions (new logo family, major diagram set) so we can align on direction.

## What's in scope

- **Logos and logomarks** for BEAM Campus projects
- **Architecture diagrams** for documentation (SVG preferred)
- **Sequence diagrams** for protocol documentation
- **Deployment diagrams** for infrastructure references
- **Social media assets** (OG images, banners, conference promotional)
- **Presentation templates** for conferences (FOSDEM, CodeBEAM, NLnet, etc.)
- **Brand-system additions** (new palette tokens, typography refinements, voice-guide entries)

## What's out of scope

- Code (goes to the respective project repos)
- User-facing product UI mockups (should live closer to the product repo)
- Stock imagery or photographic sources without clear licence (confirm CC-BY or public domain first)
- Marketing copy / sales material (that lives elsewhere)

## How to contribute

### For small additions (1-2 files)

1. Fork the repository
2. Branch: `feature/{project}-{asset-type}` — e.g. `feature/macula-og-image`
3. Commit message format: `[project] description` — e.g. `[macula] add OG image for macula.io`
4. Open pull request with:
   - Screenshots / renders of the asset in the PR description
   - Source file location (e.g. `source/svg/macula-og.svg`)
   - Licence confirmation (CC-BY-SA 4.0 default, else specify)
5. Merge after review

### For large additions (new logo family, diagram set, presentation template)

1. Open an issue first with proposed direction and drafts
2. Discuss scope and style fit with maintainers
3. Produce final artwork
4. Pull request as above

## File standards

### Logos

Required variants per project:

- **Primary** (full logomark + wordmark)
- **Mark-only** (icon, no text) — for app icons, favicons, social profile
- **Horizontal** (side-by-side arrangement)
- **Vertical / stacked** (wordmark under mark)
- **Monochrome** (single colour, for dark/light backgrounds)

Required formats:

- SVG source (primary — scalable, editable)
- PNG exports at 256, 512, 1024 pixels
- ICO or favicon exports (for browser tabs) when the mark stands alone

Optional:

- Animated SVG or Lottie for motion applications
- App icon exports (512×512, 1024×1024, Apple / Android sizes)

### Diagrams

- **SVG preferred** for all diagrams
- **Excalidraw (.excalidraw)** in `source/excalidraw/` for the editable original when sketched there — commit both the .excalidraw and the exported SVG
- **drawio (.drawio)** in `source/drawio/` for more formal diagrams — commit both the .drawio and the exported SVG
- **PNG exports** for when SVG rendering is unavailable (rare)

### Colour palette

When adding a new palette entry:

- Provide hex, RGB, HSL
- Note accessibility contrast rating (WCAG AA minimum)
- Include light-mode and dark-mode variants if relevant
- Add to `brand/palette/tokens.md`

## Licence for contributions

By submitting a pull request, you agree that:

1. Your contribution is licensed under **CC-BY-SA 4.0** (same as this repository)
2. You have the right to license the contribution (own work, or properly licensed re-use)
3. You credit any third-party components within the file metadata

If you are submitting on behalf of an organisation, confirm in the PR description that you have authorisation.

## Review criteria

Maintainers will review for:

- **Fit with existing brand system** (consistent palette, typography, voice)
- **Technical quality** (clean SVG code, exports at right sizes, no unnecessary raster embedding)
- **Licence compliance** (source files properly licensed)
- **Accessibility** (colour contrast, alt text where applicable)

## Questions

Open an issue with the `question` label, or email the maintainer: raf.lefever@erlef.org
