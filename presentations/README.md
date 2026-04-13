# BEAM Campus — Presentation Templates

Templates for conference talks, NLnet reviews, and internal presentations.

## Structure

| Subdirectory | Target audience |
|-------------|-----------------|
| `fosdem/` | FOSDEM / FOSDEM BEAM devroom |
| `codebeam/` | CodeBEAM EU, CodeBEAM Lite |
| `nlnet/` | NLnet grant reviews, NGI Forum |
| `internal/` | BEAM Campus internal, informal |

## Supported formats

- **Reveal.js** — markdown → HTML slides. Works with the Marp CLI.
- **Google Slides** — export to PDF for submission; source as `.gsd` shared link reference
- **Keynote** (`.key`) — for macOS users
- **LibreOffice Impress** (`.odp`) — for cross-platform editing
- **PDF only** — final deliverable form, always produced from source

## Brand application in slides

- **Title slide:** BEAM Campus logo + talk title, Fraunces serif (from `../brand/fonts/`), sovereign blue accent
- **Body slides:** Inter sans-serif, ink-900 on white (or grey-50 on ink-900 for dark mode)
- **Code snippets:** JetBrains Mono, ink-900 on grey-100 background
- **Diagrams:** from `../diagrams/` — embed as SVG
- **Footer:** talk title | author | handle | date

## Title slide template (Marp)

```yaml
---
marp: true
theme: default
style: |
  section {
    font-family: 'Inter', sans-serif;
    color: #0C1419;
  }
  h1, h2 {
    font-family: 'Fraunces', Georgia, serif;
    color: #143D66;
  }
  code {
    font-family: 'JetBrains Mono', monospace;
    background: #E9ECEF;
  }
---

# Talk Title

## Subtitle

Speaker name — speaker handle — event date

---

# Section break

---

## Agenda

1. First point
2. Second point
3. Third point

---

## Conclusion

Thank you.
```

## Talk conventions

### Speaker information block (always on title slide)

```
Raf Lefever
@beamologist — raf.lefever@erlef.org
BEAM Campus / Macula / ReckonDB
```

### Preparation checklist

- [ ] 1-hour talk → 30-50 slides max
- [ ] Lightning talk (5 min) → 10 slides max, 1 idea per slide
- [ ] Code on slides: use JetBrains Mono, ≥ 24pt for back-of-room readability
- [ ] Diagrams: use diagrams from `../diagrams/` (don't re-invent per talk)
- [ ] Screenshots: 2× resolution, export as PNG or WebP
- [ ] Colours: avoid red/green distinction without shape reinforcement (colourblind viewers)
- [ ] Final export: PDF for submission, editable source kept here

## Status

Empty scaffold — templates to be added.
