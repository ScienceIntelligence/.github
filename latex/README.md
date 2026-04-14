# OpenScientists LaTeX Sources

Four parts, one per deliverable.

## [`01_external_blurb/`](01_external_blurb/) — External Blurb

Mass-sendable, non-confidential, 2-page project brief for VCs, token/API sponsors, agent-startup partners, and community collaborators (e.g., ADA / 积极之心). Poster-style layout (HTML + CSS → PDF via headless Chrome) with hero header, pull-quote, two-column sections, milestone cards, asks grid, and dark "Why now" footer banner.

- `blurb_external.html` · `blurb_external.pdf`

Rebuild:

```
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --no-pdf-header-footer \
  --print-to-pdf=blurb_external.pdf blurb_external.html
```

## [`02_internal_tracker/`](02_internal_tracker/) — Internal Tracker

Founding-team-only operational tracker: projects, owners, drivers, status; partnerships to close; people to recruit; academic-support triage; this-week action items; open decisions; risks. To be mirrored into Notion/Wiki.

- `internal_tracker.md`

## [`03_nature_perspective/`](03_nature_perspective/) — Nature Perspective Proposal

~3-page academic memo proposing a Perspective in *Nature*. Five pillars (tacit knowledge, agent runtime, benchmark, model development, **metascience**), tailored asks for Phil and Dashun.

- `nature_perspective.tex` · `nature_perspective.pdf` · `refs.bib`

## [`04_original_paper/`](04_original_paper/) — Original Long Paper

The earlier manifesto-voice paper and its 2-page condensed proposal, together with the tonal-change notes and the prior blurb PDF.

- `paper.tex` · `paper.pdf` — 9-page manifesto
- `proposal.tex` · `proposal.pdf` — 2-page condensed proposal
- `blurb(1).pdf` — prior blurb
- `MANIFESTO_PASS.md` — rewrite notes
- `refs.bib`

## Compilation

```
cd <folder>
pdflatex <file>.tex
bibtex   <file>         # if refs.bib is used
pdflatex <file>.tex
pdflatex <file>.tex
```
