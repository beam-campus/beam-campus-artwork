# BEAM Campus — Diagrams

Architectural, sequence, deployment, and network diagrams for BEAM Campus projects.

## Structure

| Subdirectory | Purpose |
|-------------|---------|
| `architecture/` | High-level system architecture diagrams |
| `sequence/` | Sequence diagrams for protocols, interactions |
| `deployment/` | Infrastructure / deployment topology |
| `network/` | Network mesh, relay topology, routing visualisations |

## Tools

**Preferred creation tools (in order):**

1. **Excalidraw** — for quick sketches and technical drawings. Output: `.excalidraw` source + `.svg` export. Good for rapid iteration.
2. **drawio / diagrams.net** — for more formal diagrams. Output: `.drawio` source + `.svg` export.
3. **Structurizr DSL** — for C4 model diagrams (context, container, component, code). Output: `.dsl` + `.svg`.
4. **D2 (Terrastruct)** — for text-based diagrams with auto-layout. Output: `.d2` + `.svg`.
5. **Mermaid** — for diagrams-as-code inside markdown. Used directly in docs.

## Conventions

### File naming

```
{project}-{diagram-type}-{variant}.{ext}

Examples:
macula-architecture-routing-v2.svg
macula-sequence-realm-join.svg
hecate-deployment-bare-metal-cluster.svg
reckondb-network-khepri-cluster.svg
```

### Colour usage

Follow the brand palette in `../brand/palette/tokens.md`. For diagrams:

- **Primary lines and nodes:** `ink-700`
- **Accent / highlight:** project-specific colour from brand palette
- **Success path:** `signal-500`
- **Warning / failure path:** `warn-500`
- **Background / secondary:** `grey-100`

### Typography in diagrams

- **Labels:** Inter (sans-serif, from `../brand/fonts/`) — 12-16pt
- **Code / identifiers in diagram:** JetBrains Mono — 10-14pt
- **Titles:** Fraunces (serif) — 20-28pt

### Accessibility

- Minimum 4.5:1 contrast on labels
- Label all shapes with text; don't rely on colour alone
- Keep diagrams readable at 50% zoom in a browser
- Export at 2× resolution for retina displays

## Source files

Always commit BOTH:

1. The editable source (`.excalidraw`, `.drawio`, `.dsl`, `.d2`) in `../source/{tool}/`
2. The exported `.svg` in the appropriate `diagrams/{category}/` subdirectory

This way, future edits don't require reverse-engineering the SVG.

## Embedding in documentation

For hex.pm docs (project-specific README or guides):

```markdown
![Macula Routing V2 Architecture](../../artwork/diagrams/architecture/macula-architecture-routing-v2.svg)
```

OR copy the SVG into the project's own `assets/` directory (per hexdocs path rules).

**Important:** hexdocs requires `assets/filename.svg` paths, not `../../assets/filename.svg`. See each project's publishing rules.

## Status

Empty scaffold — diagrams to be added as they're created.
