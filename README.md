# Systems Design

A single-page working reference for designing, engineering, governing and analysing
systems across an enterprise estate of data and applications.

Live: <https://jameschrisa.github.io/systems-design/>  
Design system: <https://jameschrisa.github.io/systems-design/brand.html>

## What is in it

| Tab | Contents |
| --- | --- |
| Systems Design | Framing and boundaries, architecture and integration (16 cards) |
| Systems Engineering | Requirements and verification, reliability and operations (16 cards) |
| Business Systems Analysis | Process and stakeholders, data and application portfolio (16 cards) |
| Risk, Governance, Security | Risk management, governance and control, security and resilience (24 cards) |
| Process Flow | Solution lifecycle across people, deterministic, AI and hybrid modalities (24 cards) |
| AI Systems Engineering | Context and retrieval, tools and protocols, loop and control, evaluation and runtime (24 cards) |
| Design Patterns | 12 block-diagram patterns with fit and limits |
| Systems Auditing | 48 client questions in 8 sections, with answer hints |
| Mix Calculator | Interactive people / deterministic / AI distribution with generated risks and controls |
| Metrics | 36 enterprise metrics across delivery, reliability, process, operations, UX and AI |
| System Playground | Drag-and-connect canvas for sketching system diagrams, exports to SVG |
| Runbooks | 12 operational procedures: trigger, preconditions, steps, verification, rollback, escalation |
| Playbooks | 12 repeatable engagements: objective, phased plays, artifacts, success signals, failure modes |
| Glossary | 102 terms, filterable by source, search matches aliases |

Glossary, Metrics, Systems Audit, Mix Calculator, System Playground, Runbooks and Playbooks sit in the header icon bar rather than the tab strip.

Every card front carries practice steps as checkboxes and a one-line takeaway.
Flip any card for keywords, a field example and a diagnostic question.
Cards can be dragged into a different order.

## Deploying

This folder is self-contained. Two options:

**Serve `/docs` from the default branch**
1. Commit this folder as `docs/` at the repository root.
2. Settings → Pages → Source: *Deploy from a branch* → branch `main`, folder `/docs`.

**Serve the repository root**
1. Move the contents of this folder to the repository root.
2. Settings → Pages → Source: *Deploy from a branch* → branch `main`, folder `/ (root)`.

`.nojekyll` is included so Jekyll does not process the files. No build step is required.

## Before you publish

- `index.html` hard-codes the site URL in the Open Graph tags as
  `https://jameschrisa.github.io/systems-design/`. If the repository is named
  something else, update the two `og:url` and `og:image` values. Relative URLs
  do not work for social scrapers.
- Optionally set the same image as the repository social preview under
  Settings → General → Social preview.

## Files

```
index.html            the whole application, no build step
brand.html            brand and UI reference, reusable design system
favicon.ico           multi-resolution, 16 to 64px
site.webmanifest      installable metadata
.nojekyll             disables Jekyll processing
assets/
  favicon.svg         primary mark, navy tile with the 3D red box
  favicon-mono.svg    the box alone, transparent background
  icon-16…512.png     rasterised set, includes the 180px Apple touch icon
  og-image.png        1200×630 social preview
```

## Dependencies

Chart.js 4.4.1 is loaded from jsDelivr for the doughnut on the Mix Calculator tab,
with a CSS fallback bar if it cannot be reached. IBM Plex Sans and IBM Plex Mono
load from Google Fonts, falling back to a system sans stack. Everything else,
including all icons, is inlined. The page works offline apart from the webfonts
and that one chart.

## State

Ticked checkboxes and card order are held in memory for the session and reset on
reload. This is deliberate: browser storage behaves inconsistently inside embedded
previews. Served as a real page from GitHub Pages, `localStorage` would work if you
want persistence added.

## Credits

- Icons: [Lucide](https://lucide.dev) v1.45.0, ISC licence, paths inlined.
- Notion mark: [Simple Icons](https://simpleicons.org) v16.30.0, CC0-1.0.
- Palette: Alabaster Grey `#E3E4E8`, Flag Red `#C62C27`, Prussian Blue `#0C1A2F`,
  Mauve Shadow `#745863`, Cool Steel `#9098A6`, plus Signal Teal `#4E9DAE`.
