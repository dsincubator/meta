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

## Workflow for generating meetups

Never draft a full README in one shot.

1. Plan first: propose the meetup topic outline (candidate topics, scope, what fits in 20 min plus Q&A). Cover only topic, scope, and repo location; do not restate the standard format, which this file already specifies. Discuss with the human and get explicit approval on topics before writing anything.
2. Co-create section by section: write one section at a time (audience, why important, objectives, then demo items), confirming each with the human before moving to the next. Tackle exactly one section per exchange; never batch multiple sections into a single interaction.
3. Gates before handoff: fact-check pass against the tool's own docs, then a Human-review feedback compliance check (objectives map to demo items, demo is unpacked materials, plain markdown headings, no inline Bold headings, no em-dash characters).

## Editing conventions

- **Read the `Human-review feedback` section below before generating or editing any meetup
  material.** Treat every `Rule` there as binding. It accumulates lessons from human review
  so past mistakes (e.g. adding exercises to a single meetup, copying example flourishes
  verbatim) are not repeated.
- `README.md` follows the Teaching Tech Together pedagogical structure (learner personas, objectives, exercises, role-play). Preserve this structure when editing; do not flatten it into generic prose.
- The text is deliberately authored as teaching content and contains informal phrasing. Do not silently rewrite style or "fix" prose — confirm intent before restructuring.
- Content language is mostly English, occasionally Spanish. Keep that mix.
- When writing prose, follow these sentence principles (from `Rscript -e "skills::learn_write()"`):
  - Follow a grammatical subject as soon as possible with its verb.
  - Place in the stress position the "new information" you want the reader to emphasize.
  - Place the person or thing whose "story" a sentence is telling at the beginning of the sentence, in the topic position.
  - Place appropriate "old information" (material already stated in the discourse) in the topic position for linkage backward and contextualization forward.
  - Articulate the action of every clause or sentence in its verb.
  - In general, provide context for your reader before asking that reader to consider anything new.
  - In general, try to ensure that the relative emphases of the substance coincide with the relative expectations for emphasis raised by the structure.
- The `meta.Rproj` file indicates RStudio/Posit as the edit environment, but the content itself is plain Markdown. No R code lives here.

## Writing

- Use sentence case for headings.
- Use US English.

### Proofreading

If the user asks you to proofread a file, act as an expert proofreader and editor with a deep understanding of clear, engaging, and well-structured writing.

Work paragraph by paragraph, always starting by making a TODO list that includes individual items for each top-level section.

Fix spelling, grammar, and other minor problems without asking the user. Label any unclear, confusing, or ambiguous sentences with a FIXME comment.

Only report what you have changed.

## Commands

There are no build, test, lint, or CI commands. Nothing to run; edits to `README.md` are the deliverable.

## Files

- `README.md` — the meetup materials (primary file to edit)
- `LICENSE` — MIT
- `.gitignore` — ignores `.Rproj.user` only
- `meta.Rproj` — RStudio project settings (editor preference, not code)

## Human-review feedback

Accumulated, binding rules distilled from human review of generated meetup materials.
Treat each `Rule` as binding. When new review feedback arrives, add it here as a new entry
(Rule / Why / Where) and commit. These rules are the evolutionary memory that prevents
repeating past mistakes.

### 1. Single-meetup = demo only, no exercises

- **Rule:** A single-meetup README has **no Exercises / Role-play section**. It is a live demo (~20') + open Q&A (~10').
- **Why:** The `template` does not include exercises. A demo is always part of a meetup, so it's the section to build out.
- **Where:** Generating a single-meetup README.

### 2. Template is the schema; examples are only for voice

- **Rule:** Cite `dsincubator/template/README.md` as the authoritative structure. Use `meta/README.md` and other examples ONLY to calibrate tone/voice — never copy an example's content-specific flourishes verbatim.
- **Why:** `meta` is one concrete implementation. Copying its content-specific additions (e.g. the Teaching Tech Together quote, extra sections) treated flavor as requirement.
- **Where:** Generating or editing any meetup README.

### 3. Teaching Tech Together is a teacher resource, not a learner resource

- **Rule:** Do not put Teaching Tech Together (or other *teaching-method* resources) in a meetup's learner-facing `## Resources`. Reserve it for the teacher/materials.
- **Why:** It helps the person preparing the meetup, not the learner attending it.
- **Where:** The `## Resources` section of any meetup README.

### 4. Every objective must map to a demo item, and the demo must be unpacked materials

- **Rule:** (a) Each item under `## Objectives` must be observably covered by exactly one `## Demo` item. (b) Each demo item must be the actual materials used — links, screenshots, code blocks, commands — not abstract bullets.
- **Why:** The README is the materials presented live. Abstract descriptions force improvisation and leave gaps.
- **Where:** The `## Objectives` and `## Demo` sections of any meetup README.

### 5. Read prior human review before delegating any generation

- **Rule:** Before delegating a meetup generation/edit to a subagent, incorporate this section. Do not generate from an example alone.
- **Why:** An earlier agent produced the wrong structure because prior review notes weren't in its context.
- **Where:** Any generation or edit task.

### 6. Fact-check generation as its own gate

- **Rule:** Verify every factual claim about a specific tool/library against that tool's own docs/site as a distinct pass — do not fuse it into content generation or trust a single flaky subagent for it.
- **Why:** A meetup about a specific tool must be traceable to authoritative sources; unchecked claims can ship if the check is skipped.
- **Where:** Any meetup that names a specific product, tool, or provider.

### 7. Use plain markdown section syntax, not inline Bold or em-dashes

- **Rule:** Structure sections with real markdown headings (`#`, `##`, `###`, ...). Never use `**Bold**` as an inline pseudo-heading, and avoid em-dashes (`—`). Both scream "AI". Put bullets under a heading, not before it.
- **Why:** `**Bold**` and em-dashes are a visible AI-tell and make the markdown read as machine-generated. Human-authored markdown uses headings for structure and reserves `*` bullets for items nested inside a section.
- **Where:** Any meetup README or markdown content.
- **Example of the correct shape:**
  ```markdown
  ### Overview

  <url>

  ### Installation

  ```
  curl -fsSL https://opencode.ai/install | bash
  ```

  More options at <url>
  ```

## Status

Periodic snapshots of what this repo is being used for. When you change the status, update
this section and commit. Pull/push before resuming to stay current.

- **Next up: validate these materials.** To test whether the instructions and templates are
  clear, generate a dsincubator meetup using ONLY `AGENTS.md` +
  `dsincubator/template/README.md` as the guide, e.g. one that produced a real single-meetup
  repo at `~/git/dsincubator/opencode` (free agentic AI with opencode). Gauge what an agent
  produces (personas, objectives, demo, role-play) and whether the checklist
  (`.github/ISSUE_TEMPLATE/meetup-checklist.md`) covers generation. Iterate on these docs if
  anything is unclear or missing.
- **Feedback loop:** human review notes are accumulated as binding rules in the
  `Human-review feedback` section above (read before generating). Keep appending new lessons
  there.
- **Deferred:** whether to wrap this guidance as a formal opencode `skill` — leaning no
  (the guidance already lives in `AGENTS.md` + the template; a skill would duplicate it).
  Optional: re-run the goal/content review agents on the final docs.
- **Known gap:** opencode `bash` permission patterns match the parsed command string, so an
  agent may phrase around a guard (e.g. `git -C <dir> push` previously bypassed `git push **`).
  Treat permission rules as guardrails, not a vault.
