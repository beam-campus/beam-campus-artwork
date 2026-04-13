# BEAM Campus — Typography

*Provisional. Candidate typefaces below; final selection pending brand review.*

## Role allocation

| Role | Current candidate | Rationale |
|------|-------------------|-----------|
| Display / headings | **Fraunces** (SIL OFL) | Warm serif with engineering-heritage tone. Open-source. |
| Body / paragraphs | **Inter** (SIL OFL) | Humanist sans-serif, excellent legibility. Open-source. |
| Monospace / code | **JetBrains Mono** (SIL OFL) | Designed for code, ligatures, wide language coverage. Open-source. |
| Accent (presentations) | **Space Grotesk** (SIL OFL) | Distinctive geometric sans for large-format display. Open-source. |

All candidate typefaces are open-source under SIL OFL, meaning we can:
- Embed in documents and PDFs freely
- Ship in web fonts without licence fees
- Remix / subset without additional permission
- Use commercially without restriction

## Source

Google Fonts hosts all of these. For stable deployment, self-host from:

- **Fraunces** — https://fonts.google.com/specimen/Fraunces
- **Inter** — https://fonts.google.com/specimen/Inter
- **JetBrains Mono** — https://www.jetbrains.com/lp/mono/ or https://fonts.google.com/specimen/JetBrains+Mono
- **Space Grotesk** — https://fonts.google.com/specimen/Space+Grotesk

Store downloaded font files in this directory: `fonts/fraunces/`, `fonts/inter/`, etc.

## Licences

All font files stored in this directory must include their licence (SIL OFL.txt typically). See each subdirectory for the individual licence.

## Type scale

Suggested modular scale (1.25 ratio) for web and presentations:

| Size token | Value | Use |
|-----------|-------|-----|
| `text-xs` | 0.75rem (12px) | Metadata, footnotes |
| `text-sm` | 0.875rem (14px) | Secondary content |
| `text-base` | 1rem (16px) | Body |
| `text-lg` | 1.125rem (18px) | Introductory paragraph |
| `text-xl` | 1.25rem (20px) | Subheadings |
| `text-2xl` | 1.5rem (24px) | H4 |
| `text-3xl` | 1.875rem (30px) | H3 |
| `text-4xl` | 2.25rem (36px) | H2 |
| `text-5xl` | 3rem (48px) | H1 |
| `text-6xl` | 4rem (64px) | Display / hero |

## Web-font usage

```css
/* Self-hosted; adjust paths as needed */
@font-face {
  font-family: 'Fraunces';
  src: url('/fonts/fraunces/Fraunces-Variable.woff2') format('woff2');
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Inter';
  src: url('/fonts/inter/Inter-Variable.woff2') format('woff2');
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}

body {
  font-family: 'Inter', system-ui, -apple-system, sans-serif;
}

h1, h2, h3, h4, h5, h6 {
  font-family: 'Fraunces', Georgia, serif;
  font-weight: 600;
}

code, pre, kbd {
  font-family: 'JetBrains Mono', 'Fira Code', Consolas, monospace;
}
```

## Status

**Provisional.** Before finalising:

- [ ] Review candidates against actual brand voice and audience
- [ ] Verify readability across desktop / mobile / printed / presentation contexts
- [ ] Test rendering on common hex.pm documentation themes
- [ ] Consider alternatives: Libre Baskerville (classical), IBM Plex (enterprise), Source Serif (Adobe open-source)
- [ ] Finalise type scale based on actual use cases
