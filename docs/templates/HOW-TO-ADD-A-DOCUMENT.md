# How to add a document to the archive

Written for someone who has never done this before. Nothing here needs a
programmer.

---

## The short version

1. Copy a template out of this folder
2. Put the copy in the right archive folder
3. Rename it
4. Fill it in
5. `git add .` → `git commit -m "..."` → `git push`

That's it. The website rebuilds itself. The listing page, the date, the file
size and the TOP SECRET stamp all appear on their own.

---

## Step 1 — pick a template

| If you are writing | Use |
|---|---|
| A daily observation of a specimen | `TEMPLATE-observation-log.md` |
| Something that went wrong, reported the same day | `TEMPLATE-incident-report.md` |
| An order, instruction or notice from above | `TEMPLATE-memo.md` |
| Standing rules — how a thing is to be done | `TEMPLATE-procedure.md` |
| A person's file, duty log or evaluation | `TEMPLATE-personnel-record.md` |
| Measurements, tables, laboratory findings | `TEMPLATE-technical-report.md` |
| None of the above | `TEMPLATE-blank.md` |

Copy the file. Do not edit the ones in this folder — leave them clean so
they're there next time.

## Step 2 — where the copy goes

Into one of the six folders under `content/archive/`:

    SPECIMEN-ONE/               the organism and the animal that carried it
    RECOVERY-OPERATIONS-1961/   the flight, the recovery, the transfer
    CONTAINMENT-SECURITY/       protocols, breaches, what failed
    STATION-PROCEDURES/         how Kestrel was run
    PERSONNEL-RECORDS/          the people
    TELEMETRY-RESEARCH/         numbers, plates, laboratory work

If a document could go in two, pick the one a filing clerk would have picked.
The archive is meant to look filed, not curated.

## Step 3 — rename it

The filename is the document code, in capitals, ending in `.md`:

    PROJECT-APEX-1961-SPECIMEN-ONE-LOG-004.md
    SECURITY-INCIDENT-REPORT-14-DEC-1961.md
    EMPLOYEE-4119-MEDICAL-FOLLOW-UP-002.md

Look at what's already in the folder and follow the same pattern. Consistency
matters more than cleverness — it's meant to look like a filing system nobody
thought hard about.

## Step 4 — fill it in

Open the file in any plain text editor. Notepad works.

**Anything in `<angle brackets>` is an instruction to you.** Replace it,
brackets and all. If a line still has angle brackets when you're done, you
missed one.

At the top, between the two `---` lines, is the part the website reads:

    slug            the document code again, but in lowercase
    title           what appears in the browser tab
    date            YEAR-MONTH-DAY, e.g. 1961-11-23
    document_code   the document code, in capitals
    author          who signed it
    distribution    who was allowed to read it

The `date` controls where the file sorts in the listing. Get it right and the
archive stays chronological on its own.

Below that is the document itself. Type it as if you were typing it in 1961:
short lines, no bold, no italics, no bullet points. Plain typewriter.

## Step 5 — the black bars

Redactions are made of this character:

    █

To use one, paste a run of them where the words would have been:

    Dr. ████████████ recommends immediate review.

Longer secret, longer bar. Copy this strip and trim it to length:

    ████████████████████████████████████████████████████████████

Use `[REDACTED]` instead of bars in the header at the top, and for a name or
title inside the text — that's the convention already in use across the
archive.

**On what to redact.** Hide specifics, not substance. A page of solid bars
isn't ominous, it's unreadable — the reader skips it. Redact the name, the
number, the location. Leave the sentence that makes someone want to know what
was under the bar.

## Step 6 — publish

Open Command Prompt and run these one at a time:

    cd C:\Users\linds\incident-1961
    git add .
    git commit -m "Add <document code>"
    git push

Then wait a minute or two. The site rebuilds itself.

---

## Before you publish, three checks

**Does it contradict canon?** `CLAUDE.md` in the main folder has the list.
The big ones: the agency is OCAC and never the Department of Defense; the
place is Recovery Station Kestrel; the organism is microscopic, so there is
nothing in a chamber to watch move; Subject 7 is never distressed.

**Is it boring enough?** These are institutional documents. The horror is in
the gap between the flat voice and what it's describing. A document that
sounds frightened is a document that has done the reader's work for them.

**Does the species have a name in it?** It shouldn't. A 1961 form would carry
a designation, not a species. Keep it to "the organism", "the specimen", or a
number.
