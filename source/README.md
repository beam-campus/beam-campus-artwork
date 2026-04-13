# BEAM Campus Artwork — Source Files

Editable original files for all artwork, organised by tool.

## Structure

| Subdirectory | Tool | Extensions |
|-------------|------|-----------|
| `svg/` | Raw SVG (hand-edited or exported) | `.svg` |
| `excalidraw/` | Excalidraw | `.excalidraw`, `.excalidrawlib` |
| `drawio/` | drawio / diagrams.net | `.drawio`, `.drawio.xml` |
| `figma/` | Figma (links + export notes) | `.md` reference files |
| `affinity/` | Affinity Designer | `.afdesign` |
| `sketch/` | Sketch | `.sketch` |
| `raster/` | Raster source files | `.psd`, `.xcf`, `.krita`, `.procreate` |

## Why keep sources

Exported SVGs and PNGs are the consumable artefacts, but sources are necessary for:

- Editing a diagram without rebuilding from scratch
- Maintaining layer structure (important for complex logos)
- Evolving a design family (applying tweaks across variants)
- Reverting accidental destructive changes

## Tools recommended

### Excalidraw (primary for sketches)

- Free, open-source, collaborative
- Browser-based or VS Code extension or self-host
- Source files are plain JSON — diff-friendly in git
- Native SVG export
- Available at https://excalidraw.com

### drawio (primary for formal diagrams)

- Free, open-source, works offline
- Desktop app or browser
- Source files are XML — diff-friendly in git
- Native SVG export
- Available at https://www.drawio.com

### Affinity Designer

- Commercial (one-time purchase, no subscription)
- Excellent SVG capabilities
- Good for complex logo design and brand system development
- Platform: macOS, Windows, iPad

### Figma (for collaborative design)

- Cloud-based (no local source file possible)
- Store reference markdown files here with:
  - Figma file URL
  - Export instructions
  - Version control notes
- Exported SVGs go to main artwork directories

### Inkscape (command-line friendly)

- Free, open-source, cross-platform
- Excellent for programmatic export / batch operations
- Can read/write SVG directly

## File size guidance

- **Vector source files** (SVG, .excalidraw, .drawio, .afdesign): commit directly to git
- **Raster sources** over 10 MB: use Git LFS (Large File Storage)
- **PSD / XCF / Procreate** files can be large; always use Git LFS

To set up Git LFS for raster:

```bash
git lfs install
git lfs track "source/raster/*.psd"
git lfs track "source/raster/*.xcf"
git add .gitattributes
```

## Metadata

For source files, ideally include in file metadata or accompanying markdown:

- Original designer / author
- Creation date
- Last significant revision date
- Licence (default CC-BY-SA 4.0 unless specified)
- Notes on intended use
- Known issues or limitations

## Status

Empty scaffold — sources to be added as artwork is created.
