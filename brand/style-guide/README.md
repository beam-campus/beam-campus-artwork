# BEAM Campus Brand Style Guide

*Living document. Evolves as the brand system matures.*

## Purpose

This guide defines how BEAM Campus visual identity is applied across the ecosystem: logos, colours, typography, voice, and usage rules. It serves both internal projects (Macula, ReckonDB, Evoq, Hecate, Faber) and external partners (franchisees — if applicable — conference organisers, ecosystem collaborators).

## Core brand idea

**Sovereign infrastructure, European by design.**

BEAM Campus is a deep-tech company making the software layer for post-hyperscaler, post-CLOUD-Act Europe. Our visual language reflects this:

- **Engineering-native** — diagrams and technical clarity over marketing polish
- **European-rooted** — quiet confidence, not Silicon Valley bombast
- **Open and composable** — visuals read as infrastructure, not products
- **Sovereign** — independence, resilience, locality signalled through form

## Logo system

Each BEAM Campus project has its own logomark, expressing its role in the stack:

| Project | Role | Visual hint |
|---------|------|-------------|
| BEAM Campus | Umbrella | Academic / campus motif |
| Macula | Network | Mesh / graph |
| ReckonDB | Data | Stream / event |
| Evoq | Framework | Wave / invocation |
| Hecate | Runtime | Gate / threshold |
| Faber | Neural | Growth / evolution |

Logos live in `logos/{project}/`. Each project provides primary, mark-only, horizontal, vertical, and monochrome variants.

## Colour palette

Defined in [`../palette/tokens.md`](../palette/tokens.md). Key tokens:

- **Ink** — primary text and lines (dark navy, near-black)
- **Sovereign Blue** — primary brand colour (deep, quiet blue, sovereign-feel)
- **Signal Green** — success, traction, positive state
- **Warning Amber** — attention, regulatory, caution
- **Neutral Grey** (scale) — surfaces, backgrounds, UI chrome

See `tokens.md` for exact hex values, accessibility ratings, and dark-mode variants.

## Typography

Defined in [`../fonts/README.md`](../fonts/README.md). Summary:

- **Display / headings:** a serif or strong display typeface conveying academic heritage
- **Body text:** a clean humanist sans-serif
- **Monospace:** an open-source monospace for code and technical content
- **Accent (sparing):** a specimen face for presentation title slides

All font licences documented in `fonts/licences.md`.

## Voice

Defined in [`../voice/README.md`](../voice/README.md). Key principles:

- **Engineer-to-engineer register** — direct, specific, no marketing verbs
- **Avoid:** "disrupt," "revolutionary," "game-changing," "seamlessly," "unlock"
- **Favour:** "implements," "replaces," "extends," "validates," "proves"
- **Numbers over adjectives** — "300 relays across DE/FI/FR" beats "large-scale deployment"

## Usage rules

### Logo clear space

Minimum clear space around any logo equals the height of the mark's x-character. Don't crowd logos with other imagery.

### Minimum size

- Digital primary use: 40px height minimum
- Print: 10mm height minimum
- Favicon / app icon: mark-only variant, no wordmark

### What NOT to do

- Don't stretch or skew the logo
- Don't change the colour of the mark except to approved variants (primary, monochrome, inverse)
- Don't place the logo on busy backgrounds without sufficient contrast
- Don't rotate the logo
- Don't add drop shadows or glows
- Don't combine the logo with other logos in a "lockup" without explicit maintainer approval

### Co-branding

When BEAM Campus appears alongside partner / affiliation marks:

- Equal visual weight
- Clear separation (vertical bar or generous whitespace)
- Precedence: BEAM Campus brand comes first when we are the primary presenter

### Erlef affiliation mark

"Erlang Ecosystem Foundation Member" mark from `logos/erlef/` is used to signal active Erlef membership. Used only by current members. See Erlef's own brand guidelines for additional rules.

## Where to use what

| Context | Assets |
|---------|--------|
| Website hero | Primary horizontal logo, sovereign blue palette, serif display |
| Conference slide | Vertical logo top-right, monospace for code, minimal colour |
| Hex.pm package page | Mark-only icon, monochrome if package has limited colour control |
| Social media OG | 1200×630 banner, project-specific colour accent, tagline |
| Technical documentation | Monochrome horizontal logo in header, inline diagrams in sovereign blue |
| Printed materials | Minimum 10mm mark, single-colour if budget constrains |

## Evolution

This brand system is early. Expect refinement as the ecosystem matures. Changes are versioned via git; breaking changes to tokens require a pull request with rationale.

Last updated: 2026-04-13
