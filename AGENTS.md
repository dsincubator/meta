# AGENTS.md

## What this repo is

This is **not a software project**. It is the materials for a data-science meetup (`dsincubator/meta`) whose goal is to teach others how to run data-science meetups.

- The `README.md` is the unit of work: it is both the repo's purpose statement and the meetup content itself (audience, objectives, demo, exercises).
- The repo sits in the `dsincubator` GitHub org and relates to `dsincubator/template` (repo template, issue-template checklist, topics poll discussion), `2degreesInvesting/ds.testing` (example meetup series), and the `dsincubator.github.io` blog.

## Generating new meetups (why this format)

This repo is the canonical **single-meetup** example: agents may use it as a reference to generate a standalone dsincubator meetup in the same format (audience, objectives, demo, exercises, role-play). For a **series** of meetups, use `dsincubator/template` instead — the README acts as a syllabus where each `### Meeting N` section is one meetup. The template README also notes the release convention: *each item in the syllabus corresponds to a meetup and a GitHub release that preserves a snapshot of the repository exactly as it was shown during the meetup*.

Before generating anything, read the org profile README — it documents the project's **values → workflow** mapping that explains *why* the format is what it is (e.g. presentations made directly from markdown, all materials in a single public repo based on a template, meetups ≤30 min with live discussion):

- https://github.com/dsincubator/.github/blob/main/profile/README.md (raw: https://raw.githubusercontent.com/dsincubator/.github/main/profile/README.md)

### The series example

For the canonical example of the **series** format (rather than this single-meetup example), see `2degreesInvesting/ds.testing` — a series of meetups about testing R code where the README acts as a **syllabus**: each `##` section is one meetup with its own objectives, linked to a GitHub [release](https://github.com/2DegreesInvesting/ds.testing/releases) (a snapshot of the repo as shown in that meetup) and a presentation video. Example — the "Introduction" meetup's material (plus its video transcript at `/tmp/ds-testing_introduction_transcript.md`):

> This meetup covers the introduction to Testing from the book Mastering Shiny, and maybe the subsection Philosophy. The following meetups will cover the mechanical aspects of testing with testthat.
>
> Objectives: Understand why testing is useful and what is it. Introduce the basic anatomy of a testthat test. Introduce four levels of testing and announce which one level this series focuses on. Discuss when you should write tests. Discuss what we want to take away from this series.

Repo: https://github.com/2degreesInvesting/ds.testing

Follow that documented series structure when generating a multi-meetup series, and match this repo's single-meetup structure when generating a standalone meetup.

## Editing conventions

- `README.md` follows the Teaching Tech Together pedagogical structure (learner personas, objectives, exercises, role-play). Preserve this structure when editing; do not flatten it into generic prose.
- The text is deliberately authored as teaching content and contains informal phrasing. Do not silently rewrite style or "fix" prose — confirm intent before restructuring.
- Content language is mostly English, occasionally Spanish. Keep that mix.
- The `meta.Rproj` file indicates RStudio/Posit as the edit environment, but the content itself is plain Markdown. No R code lives here.

## Commands

There are no build, test, lint, or CI commands. Nothing to run; edits to `README.md` are the deliverable.

## Files

- `README.md` — the meetup materials (primary file to edit)
- `LICENSE` — MIT
- `.gitignore` — ignores `.Rproj.user` only
- `meta.Rproj` — RStudio project settings (editor preference, not code)
