# CLAUDE.md — incident-1961

Read this first in any new session.

## What this is

The public face of the **Jovian Cell** project: a Hugo site presenting Project APEX
as an exposed government archive someone was not meant to find. Companion to the
book series and to Episode One, *Contingency Film 7-A*.

Created by a child author, referred to here as **the author**. His mother produces.
All core worldbuilding is his.

Names are deliberately absent from this repository — it is public. Both are in
the production folder described below, which is not.

The production project lives separately at `Desktop/Astrophage_Project_Folder/Astrophage/`
— bible, scripts, cards, audio, tools. That folder's own `CLAUDE.md` governs the video.
This repo is only the archive site.

## Canon — do not contradict

**Canon does not live in this repository, and must not be copied into it.**
The story bible, the Episode One script and the 1961 fact-check are held in the
production folder on the producer's machine:

    Desktop/Astrophage_Project_Folder/Astrophage/

That folder has its own `CLAUDE.md`, and it is the authority. In a Cowork session
with both folders connected, read it before doing creative work.

Two reasons the canon stays out of this repo. It is public, so the bible would
name a child; and the bible contains the endings of all three books, which is the
one thing an archive built on withheld information should not publish.

The non-negotiables, restated here because the archive keeps getting them wrong:

- The agency is the **Office of Civil Aerospace Contingency (OCAC)**. Not the
  Department of Defense. A 4:11 orbital flight on 16 November 1961 is so far ahead
  of the public programme that Kestrel cannot have been NASA. One number says it.
- The facility is **Recovery Station Kestrel**. A *recovery* station — recovery is
  the vector, and that is the answer to "why 1961."
- **The Jovian Cell is microscopic.** Individual cells are single-celled and
  invisible. What occupies a host is a colony of trillions; consciousness is
  emergent from the colony. There is no creature in a chamber. Nothing paces,
  nothing scratches at a wall, nothing is fed in grams.
- **Subject 7** is a chimpanzee, and for the whole of the observation period it is
  healthy, calm and entirely ordinary. The documents stay boring while the cranial
  measurements climb 27.4 → 32.6 and then read MEASUREMENT DECLINED. That gap is
  the horror. Do not let a document panic early.
- **Employee 4119** is a technician in his fifties. Not a scientist. He took the
  sixth barb, reported no injury, completed his shift and drove home.
- Dates: capsule recovered **16 November 1961**. Terminal event **23 November 1961**,
  approximately 1400 hours. Seven days.
- In-universe register: 1961 agencies assign designations, not names —
  SUBJECT 7, EMPLOYEE 4119, CONTINGENCY FILM 7-A, PLATE 41.
- **Subject 7 is never shown in distress.** Confirmed by the author, Sept 2026 — no distress
  makes it creepier. The observation logs stay clinical and the animal stays healthy and
  ordinary in every entry while the numbers climb underneath it. Nothing in this archive
  should ever describe the animal as suffering, agitated, or unwell.
- **Employee 4119 is not the Book One protagonist.** Confirmed by the author, Sept 2026. The
  story arcs over many millennia; 4119 is an episode in it, not the vantage point. The
  archive can treat him as the first human host and nothing more.
- **APEX stands for Aerospace Primate Examination.** Named by the author, Sept 2026.
  Stated in full exactly twice in the archive: once deadpan in the station
  protocol manual, once at the close of the Specimen One analysis, where the
  irony lands — the program did precisely what it was authorised to do. Do not
  spell it out a third time. An acronym that keeps explaining itself stops
  being a designation and becomes a caption.
- **The species name never appears.** Not in Episode One and not in this archive.
  A 1961 form would not carry it. The only Jupiter reference anywhere is the
  negation on Plate 41.

## Standing decisions for the site

- **It reads as an exposed server, not a designed archive.** Raw directory listing,
  filename codes, classification stamps, visible dates. No search, no tag cloud,
  no "featured document." The author's call, and it is the right one.
- **Black bars for in-text redactions, `[REDACTED]` in headers and titles.**
  The producer's call, September 2026. Bars are `█` characters — real characters in a
  monospace column, so they align with the typewriter grid instead of floating.
- Documents are **rendered verbatim**. `single.html` prints `.RawContent` inside a
  `<pre>`, so box-drawing rules, column alignment and redaction bars survive exactly
  as typed. Do not switch these to rendered Markdown — it will eat the layout.
- Redaction should hide **specifics, not substance**. A page of solid bars is not
  ominous, it is unreadable. Each document should say enough to be worth reading.
- Media (audio, video) can be added later under `static/media/`. Documents first.

## Current state

- 29 archive documents across six sections, in `content/archive/`
- Layouts: directory listing, document page, home. `themes/incident/layouts/`
- Deploy: `.github/workflows/hugo.yml`. The old static-deploy workflow is disabled,
  not deleted — see `deploy-static.yml`, which now only runs if triggered by hand.
- The hand-written `index.html` at the repo root is left over from the static-deploy
  era. Hugo ignores it. It is not the live site any more.

## Adding a document

`docs/templates/` holds a template per document type and a plain-language
`HOW-TO-ADD-A-DOCUMENT.md` written for someone who has never used git. The
templates live under `docs/` rather than `content/` on purpose — Hugo only
builds `content/`, so they are never published. Copy one out, do not edit the
originals.

Placeholders are in `<angle brackets>`. Redaction bars are literal `█`
characters; `[REDACTED]` is used in headers and for names.

## Working notes

- The producer is new to git, Hugo and the terminal, and has said so plainly. Explain the
  why, not just the command, and do not assume a step is obvious. She debugged a
  Jekyll override for an hour and won, so the capability is there — the vocabulary
  is what is missing.
- **The child is the author.** When his idea and a more conventional choice conflict, his
  idea wins unless there is a real craft reason, and the reason gets explained rather
  than quietly applied.
