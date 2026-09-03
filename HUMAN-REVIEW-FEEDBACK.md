# HUMAN-REVIEW-FEEDBACK

Accumulated, binding rules distilled from human review of generated meetup materials.
**Before generating or editing any meetup material, read this file and treat every `Rule`
as binding.** This file is the evolutionary memory that prevents repeating past mistakes.

When you receive new human review feedback, add it here as a new entry (Rule / Why / Where),
then commit. Sources: session reviews, `human-review.md`, GitHub PR reviews, meetup feedback.

---

## 1. Single-meetup = demo only, no exercises

- **Rule:** A single-meetup README has **no Exercises / Role-play section**. It is a live demo (~20') + open Q&A (~10').
- **Why:** The `template` does not include exercises. A demo is always part of a meetup, so it's the section to build out.
- **Where:** Generating a single-meetup README.

## 2. Template is the schema; examples are only for voice

- **Rule:** Cite `dsincubator/template/README.md` as the authoritative structure. Use `meta/README.md` and other examples ONLY to calibrate tone/voice — never copy an example's content-specific flourishes verbatim.
- **Why:** `meta` is one concrete implementation. Copying its content-specific additions (e.g. the Teaching Tech Together quote, extra sections) treated flavor as requirement.
- **Where:** Generating or editing any meetup README.

## 3. Teaching Tech Together is a teacher resource, not a learner resource

- **Rule:** Do not put Teaching Tech Together (or other *teaching-method* resources) in a meetup's learner-facing `## Resources`. Reserve it for the teacher/materials.
- **Why:** It helps the person preparing the meetup, not the learner attending it.
- **Where:** The `## Resources` section of any meetup README.

## 4. Every objective must map to a demo item, and the demo must be unpacked materials

- **Rule:** (a) Each item under `## Objectives` must be observably covered by exactly one `## Demo` item. (b) Each demo item must be the actual materials used — links, screenshots, code blocks, commands — not abstract bullets.
- **Why:** The README is the materials presented live. Abstract descriptions force improvisation and leave gaps.
- **Where:** The `## Objectives` and `## Demo` sections of any meetup README.

## 5. Read prior human review before delegating any generation

- **Rule:** Before delegating a meetup generation/edit to a subagent, incorporate this file AND any existing `human-review.md`. Do not generate from an example alone.
- **Why:** This session's agent produced the wrong structure because prior review notes weren't in its context.
- **Where:** Any generation or edit task.

## 6. Fact-check generation as its own gate

- **Rule:** Verify every factual claim about a specific tool/library against that tool's own docs/site as a distinct pass — do not fuse it into content generation or trust a single flaky subagent for it.
- **Why:** A meetup about a specific tool must be traceable to authoritative sources; unchecked claims can ship if the check is skipped.
- **Where:** Any meetup that names a specific product, tool, or provider.