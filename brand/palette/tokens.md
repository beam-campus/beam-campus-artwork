# BEAM Campus — Colour Palette Tokens

*Provisional. Finalise with designer if this becomes the canonical system.*

## Primary brand palette

### Ink (text, lines, primary surfaces)

| Token | Hex | RGB | HSL | WCAG AA on white |
|-------|-----|-----|-----|-----------------|
| `ink-900` | `#0C1419` | 12, 20, 25 | 204° 35% 7% | ✅ 16.3:1 |
| `ink-700` | `#1F2D37` | 31, 45, 55 | 205° 28% 17% | ✅ 12.1:1 |
| `ink-500` | `#4A5B69` | 74, 91, 105 | 207° 17% 35% | ✅ 6.8:1 |
| `ink-300` | `#94A3B0` | 148, 163, 176 | 206° 14% 64% | ⚠ 2.8:1 (large text only) |

### Sovereign Blue (primary brand)

| Token | Hex | RGB | HSL | Accessibility |
|-------|-----|-----|-----|-----------------|
| `sovereign-900` | `#0A2540` | 10, 37, 64 | 210° 73% 15% | ✅ 14.7:1 on white |
| `sovereign-700` | `#143D66` | 20, 61, 102 | 212° 67% 24% | ✅ 10.8:1 on white |
| `sovereign-500` | `#2563A3` | 37, 99, 163 | 211° 63% 39% | ✅ 5.4:1 on white |
| `sovereign-300` | `#72A1CE` | 114, 161, 206 | 209° 49% 63% | ⚠ 2.4:1 (large text) |
| `sovereign-100` | `#D6E4F2` | 214, 228, 242 | 210° 53% 89% | Background only |

### Signal Green (success, traction)

| Token | Hex | RGB | HSL |
|-------|-----|-----|-----|
| `signal-700` | `#1E6F42` | 30, 111, 66 | 148° 57% 28% |
| `signal-500` | `#3A9B68` | 58, 155, 104 | 148° 46% 42% |
| `signal-300` | `#82C3A2` | 130, 195, 162 | 149° 35% 64% |

### Warning Amber (attention, regulatory)

| Token | Hex | RGB | HSL |
|-------|-----|-----|-----|
| `warn-700` | `#8C5E14` | 140, 94, 20 | 38° 75% 31% |
| `warn-500` | `#C8831C` | 200, 131, 28 | 37° 75% 45% |
| `warn-300` | `#E6B97A` | 230, 185, 122 | 33° 66% 69% |

### Neutral Grey (surfaces, UI)

| Token | Hex | RGB | HSL |
|-------|-----|-----|-----|
| `grey-50` | `#F8F9FA` | 248, 249, 250 | 210° 17% 98% |
| `grey-100` | `#E9ECEF` | 233, 236, 239 | 210° 14% 93% |
| `grey-300` | `#CED4DA` | 206, 212, 218 | 210° 14% 83% |
| `grey-500` | `#8A929C` | 138, 146, 156 | 213° 9% 58% |
| `grey-700` | `#4A5058` | 74, 80, 88 | 217° 9% 32% |

## Dark mode variants

When rendering in dark mode, swap these tokens:

| Light mode | Dark mode equivalent |
|------------|---------------------|
| `ink-900` (body text) | `grey-50` |
| `ink-500` (secondary text) | `grey-300` |
| Background white | `ink-900` |
| `sovereign-500` (primary accent) | `sovereign-300` |
| `signal-500` (success) | `signal-300` |
| `warn-500` (warning) | `warn-300` |

## Project accent colours

Each project may have one accent colour drawn from the palette:

| Project | Accent token | Rationale |
|---------|-------------|-----------|
| BEAM Campus (umbrella) | `sovereign-700` | The whole stack's primary |
| Macula | `sovereign-500` | Network = the sovereign primary |
| ReckonDB | `ink-700` | Data = deep, dense, foundational |
| Evoq | `signal-500` | Framework = alive, active |
| Hecate | `warn-500` | Runtime = at the gate, attentive |
| Faber | `signal-700` | Neural = growth, evolution |

Use accent sparingly — one accent colour per project, backed by ink/grey for structure.

## Usage rules

- **Body text on white:** `ink-900` minimum
- **Body text on `sovereign-900` backgrounds:** `grey-50`
- **Primary CTA background:** `sovereign-500` or `sovereign-700`
- **Primary CTA text:** white
- **Error / critical states:** `warn-700` text on `warn-300` / `grey-100` background
- **Success / positive:** `signal-700` text
- **Never combine:** `sovereign-300` text on white (accessibility fail)
- **Never combine:** `warn-500` text on `warn-300` background (low contrast)

## CSS variables

```css
:root {
  --ink-900: #0C1419;
  --ink-700: #1F2D37;
  --ink-500: #4A5B69;
  --ink-300: #94A3B0;

  --sovereign-900: #0A2540;
  --sovereign-700: #143D66;
  --sovereign-500: #2563A3;
  --sovereign-300: #72A1CE;
  --sovereign-100: #D6E4F2;

  --signal-700: #1E6F42;
  --signal-500: #3A9B68;
  --signal-300: #82C3A2;

  --warn-700: #8C5E14;
  --warn-500: #C8831C;
  --warn-300: #E6B97A;

  --grey-50: #F8F9FA;
  --grey-100: #E9ECEF;
  --grey-300: #CED4DA;
  --grey-500: #8A929C;
  --grey-700: #4A5058;
}

@media (prefers-color-scheme: dark) {
  :root {
    --body-bg: var(--ink-900);
    --body-fg: var(--grey-50);
    --accent: var(--sovereign-300);
  }
}
```

## Status

**Provisional.** This palette is draft for scaffolding. Finalisation needs:

- [ ] Accessibility review (run through axe-core or Stark)
- [ ] Print-colour verification (CMYK equivalents for Pantone near-matches)
- [ ] Sample application in real hex.pm doc, website, and slide template
- [ ] Feedback from at least one external designer or colour-savvy reviewer
