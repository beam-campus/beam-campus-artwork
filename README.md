# BEAM Campus — Artwork

Visual identity, diagrams, presentation templates, and brand assets for the BEAM Campus ecosystem.

## Projects covered

- **BEAM Campus** — the umbrella
- **Macula** — federated HTTP/3 relay mesh
- **ReckonDB** — BEAM-native event store
- **Evoq** — CQRS/ES framework
- **Hecate** — sovereign application platform
- **Faber** — neuroevolution on BEAM

## Repository layout

```
artwork/
├── logos/              Per-project logomarks (SVG primary, PNG exports)
│   ├── beam-campus/
│   ├── macula/
│   ├── reckondb/
│   ├── evoq/
│   ├── hecate/
│   ├── faber/
│   └── erlef/          Erlang Ecosystem Foundation (affiliation marks)
├── diagrams/           Architecture and protocol diagrams (SVG)
│   ├── architecture/
│   ├── sequence/
│   ├── deployment/
│   └── network/
├── social/             Social-media assets
│   ├── og-images/      Open Graph images for link previews
│   ├── banners/        Site / hexdocs banners
│   ├── twitter/
│   └── linkedin/
├── presentations/      Slide templates
│   ├── fosdem/
│   ├── codebeam/
│   ├── nlnet/
│   └── internal/
├── brand/              Brand system
│   ├── style-guide/    Usage rules, clear space, minimum sizes
│   ├── palette/        Colour tokens (hex, RGB, HSL, Pantone)
│   ├── fonts/          Font specimen and licensing notes
│   └── voice/          Tone, vocabulary, writing guidelines
└── source/             Source files (non-exported originals)
    ├── svg/
    ├── excalidraw/
    ├── drawio/
    ├── figma/          Links + export instructions
    ├── affinity/       Affinity Designer files (.afdesign)
    ├── sketch/
    └── raster/         Original raster sources (PSD, XCF, etc.)
```

## Conventions

### File naming

```
{project}-{variant}-{size}.{ext}

Examples:
macula-logo-horizontal.svg
macula-logo-horizontal-256.png
reckondb-logo-mark-only.svg
beam-campus-og-image-1200x630.png
```

Keep names **kebab-case**, lowercase, no spaces, no trailing zeros. Include size in filename only for raster exports.

### Formats

- **Primary format: SVG** — for logos, diagrams, social assets
- **Raster exports: PNG** — always derived from SVG, committed alongside
- **Source files:** kept in `source/` — these are the "project files" (Excalidraw `.excalidraw`, drawio `.drawio`, Affinity `.afdesign`, etc.)
- **Excalidraw** is preferred for quick architecture sketches — text-based, diffable, open-source
- **drawio / diagrams.net** for more formal deployment/sequence diagrams

### Export checklist

When you add a logo or diagram:

- [ ] SVG source in the project's `logos/` or `diagrams/` subdirectory
- [ ] PNG exports at common sizes (256, 512, 1024 for logos; 1200×630 for OG)
- [ ] Transparent background where appropriate
- [ ] Source file in `source/` (the editable original if different from SVG)
- [ ] Licence headers / credits in file metadata where meaningful

### Hexdocs asset integration

Many of these assets end up in hex.pm documentation. Follow the project-level rule:

> Asset paths in markdown guides MUST use `assets/filename.svg`, NOT `../assets/filename.svg`.

See any project's `CLAUDE.md` / publishing notes for full hexdocs rules.

## Contributing

### Who can contribute

- BEAM Campus maintainers and collaborators
- External designers who submit work under this repository's licence

### What to contribute

- New logo variants (compact, monochrome, animated)
- Architecture diagrams for existing or new documentation
- Presentation templates for upcoming conference talks
- Brand-system refinements (palette tokens, typography, voice guide)

### Workflow

1. Branch: `feature/{project}-{asset-type}` — e.g. `feature/macula-sequence-diagram`
2. Commit message: `[project] description` — e.g. `[macula] add Routing V2 architecture diagram`
3. Open pull request with preview images rendered in the PR description
4. Merge after review by a maintainer

## Licence

All visual work in this repository is released under **Creative Commons Attribution-ShareAlike 4.0 International (CC-BY-SA 4.0)**, unless individual files include a different notice.

See [`LICENSE`](./LICENSE) for the full text.

Trademark usage of "BEAM Campus," "Macula," "ReckonDB," "Evoq," "Hecate," and "Faber" is governed separately. Using the logos in a way that implies endorsement or official affiliation requires permission. Using them to refer to the projects (e.g. "I'm using Macula in my stack") is always fine.

## Contact

- **Maintainer:** Raf Lefever — raf.lefever@erlef.org
- **Website:** https://macula.io
- **Umbrella:** BEAM Campus — sovereign infrastructure for the post-cloud era

## Related repositories

| Repo | Role |
|------|------|
| [macula](https://github.com/beam-campus/macula) | Federated HTTP/3 relay mesh portal |
| [ex-esdb](https://github.com/beam-campus/ex-esdb) | BEAM-native event store |
| [ex-esdb-gater](https://github.com/beam-campus/ex-esdb-gater) | Gateway API for ex-esdb |
| [bc-utils](https://github.com/beam-campus/bc-utils) | Utility library collection |
| [bc_apis](https://github.com/beam-campus/bc_apis) | BEAM Campus API clients |

Artwork should prefer to ship asset references *from* those repos *to* this one, keeping graphics centralised.
