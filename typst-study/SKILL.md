---
name: typst-study
description: >
  Draft, restructure, and polish Typst content for study materials and exam-prep
  answers — státnice/exam question write-ups, lecture summaries, cheat sheets, and
  structured notes. Use this whenever the user wants to write up or clean up a study
  question, "zpracovat otázku", turn a messy braindump of notes into a coherent
  answer, summarize material, or fill gaps in study content — even if they don't say
  "Typst" explicitly. The output is content-only Typst source (headings + body, no
  preamble) meant to be pasted into an existing document. The skill's value is the
  workflow: learn the house style from finished siblings, check coverage against the
  source material, avoid duplicating sibling questions, write in a matching register,
  add figures by reusing working patterns, and keep within a page budget.
---

# Typst study materials

Generate or clean up **content-only** Typst source for study materials — most often
a written-up answer to a státnice/exam question, but also lecture summaries, cheat
sheets, or notes. The output gets pasted into an existing Typst document that already
has the preamble and a `meta(...)` header, so the source you produce must contain
**no preamble**: no `#set`, `#show`, `#import`, no top-level `#let`, no `meta(...)`.
Just headings and content.

The real work isn't typing markup — it's making the write-up match the rest of the
document set in **structure, depth, register, and length**, while covering the topic
completely and not repeating what a neighboring question already handles. That
workflow is below.

## Output contract

These keep the output paste-ready and consistent with the surrounding document.

1. **Content only.** No preamble of any kind. The file starts directly with content.
   The one exception is advanced figures — see *Figures* below for how to handle the
   import they need without putting it in the snippet.
2. **Headings: levels 1–3.** `= Chapter` / `== Section` / `=== Subsection`. Avoid
   `====` or deeper — if you need it, the structure is probably too granular.
3. **Don't repeat the topic title as the first heading.** The surrounding document
   already prints the question title. Dive straight into the first real section. If a
   short framing sentence or definition belongs at the very top, emit it as plain text
   before the first heading — don't invent a heading for it.
4. **Dashes:** use `--` for en dash and `---` for em dash. Never paste Unicode `–`/`—`.
   This is a repo convention; matching it avoids visual inconsistency with siblings.
5. **No placeholders.** Every section has real, substantive content. If you can't fill
   a section, drop it or flag it to the user rather than emit "TODO".

These are sensible defaults, not laws. If the author has a good reason to deviate — an
explicit request, or a topic that genuinely needs something different (deeper nesting,
a non-standard structure) — honor it rather than enforce a rule against their wishes.
The defaults exist to keep the set consistent, not to override the author's judgment.

## Workflow

The steps are ordered, but adapt to where the user already is — they may hand you a
braindump to restructure (start at step 2) or an existing answer to extend/trim.

### Before you start: build on quality material, not a blank prompt

The best answers come from *enhancing an existing base*, not one-shotting from a single
prompt — output quality tracks input quality. So unless the author says otherwise,
**recommend they first put together at least a rough base** of what the question should
contain (a skeleton of the key points and facts), and then have you structure, polish,
and fill it. If they give you only a one-line topic, suggest this first; if they'd
rather you draft from scratch, go ahead, but tell them that supplying source material
would raise the quality.

Source priority for that base:

1. *Our own FM TUL materials* (lecture notes, slides, course skripta) — the primary
   source, and what the exam is actually based on.
2. If ours are missing or weak on a subtopic, a *reputable external source* (another
   university's materials, a solid textbook or reference site). Mention in passing where
   you leaned on an external source, so the author can sanity-check it against the
   syllabus.

### 1. Learn the house style first

Before writing anything, read **2–3 already-finished documents** in the same set plus
any shared include/util file, and mirror what you find: heading depth, prose register
(formal/academic vs. casual), how `*bold*`/`_italic_`/tables/code/figures are used,
sentence rhythm, and language. You are matching an existing voice, not imposing your
own. See `references/house-style.md` for the concrete conventions of *this* repo
(the `meta(...)` header, which finished files to read, what `difficulty`/`ai` mean).

Authors vary in small ways, so where they differ, lean toward the conventions in
`references/house-style.md`. The point is just that a new question shouldn't look
out-of-place next to the others — house consistency, not robotic rule-following. Don't
agonize over small stylistic choices.

### 2. Gather and organize the material

If the user pasted raw notes, OCR dumps, or bullets, your job is to **restructure**,
not invent: group related facts under sensible `=`/`==` headings, merge duplicates,
fix broken list markers and OCR artifacts, and turn fragments into clean prose. Keep
the user's facts; don't silently add claims you can't support.

### 3. Check coverage against the source material

If there's a textbook, skripta, or syllabus, **skim its structure** (table of
contents / chapter list) and make sure every core subtopic the question implies is
covered to a depth similar to the finished siblings. Name the gaps explicitly and
fill them. This is how an answer goes from "a pile of notes" to "complete".

### 4. Avoid duplicating sibling questions

Study sets split topics across questions. Before going deep on a subtopic, check
whether a **neighboring question owns it**. If it does, keep your treatment brief and
point the reader there instead of duplicating its depth. Use a real cross-reference if
the document set has one; if not, just name the other question in prose (e.g. "podrobně
viz otázka o …"). The goal is simply *don't duplicate* — reference and move on. Flag any
overlap you can't resolve to the user; the division of labor may be theirs to decide.

### 5. Propose the outline, get approval

Present a short headings-only outline in chat and ask the user to confirm or adjust.
Only write full content once they approve. This is cheap and catches structure
problems before you've written paragraphs.

### 6. Write the content

Match the style learned in step 1. Favor clear, factual prose with key terms in
`*bold*`. Use tables for comparisons (wrap headers in `table.header`), code blocks for
code, and numbered lists (`+`) for ordered procedures.

**Match depth, not just structure.** Reading a sibling tells you the *granularity*
expected, and it's usually deeper than a first draft. Finished answers here typically
illustrate each mechanism with a short **code/SQL snippet** and cover the standard
sub-mechanisms and edge cases — not just the headline concept. For SQL views that
means `INSTEAD OF` triggers and `WITH CHECK OPTION`; for access rights `DENY`,
`WITH GRANT OPTION`, and grant granularity; for transactions the lost-update anomaly,
locking vs. MVCC, and deadlock. Aim for: *a concept, a concrete example, and the
gotchas a teacher would expect you to know.* When the user gives you source material
(braindump, skripta), mine it for exactly these specifics rather than settling for the
textbook headline.

But depth means the *right* content, not more words — a brief example beats a long
paragraph, and a table beats a bullet pile. Keep every point tight; the overall length
is bounded (step 9).

### 7. Figures and diagrams (optional)

A diagram can help, but use figures **sparingly** — add one only when it genuinely
clarifies an idea better than prose, and pick the type that fits the topic. Most
questions need none; don't add a diagram for its own sake. When you do want one, reuse a
working figure from a sibling rather than inventing. `references/figures.md` notes which
sibling has which kind of figure and the import they need.

### 8. Match the register and avoid AI tells

Study answers must read like a knowledgeable person wrote them, not like an LLM or
marketing copy. Keep a **formal, factual register matching the siblings** and actively
avoid the usual AI tells *as you write* — a clean first draft is the goal, not one that
needs rescuing afterwards:

- no chatty personality, first-person asides, or rhetorical questions;
- no marketing superlatives or empty intensifiers (*klíčový*, *zásadní*, *revoluční*);
- no filler openers/closers (*V dnešní době…*, *Závěrem lze konstatovat…*);
- no nominalizations where a verb is clearer (*došlo k realizaci* → *provedli jsme*);
- no compulsive rule-of-three or tautological pairs (*různé a rozmanité*);
- no `—` em dash in prose — use the repo's `--` / `---` convention;
- vary sentence length; avoid a monotone wall of equal-length clauses.

As an **optional last touch**, the author can run the Czech humanizer skill
(`humanizer-czech`, https://github.com/bejek/humanizer-czech) for a final polish.
Suggest it only if they'd like it — it isn't required — and on technical text apply it
lightly: fix awkward phrasing without disturbing precise terminology or the `--`
convention.

### 9. Hit the right length — calibrate to the finished questions

The finished questions are the yardstick: they land roughly in the **2–5 page** range.
Both failure modes are bad and symmetric — *a page of shallow bullets* is too thin (no
real understanding shown), *five-plus pages of prose* is too much (nobody revises from
that). Aim for **complete but tight**: every core subtopic covered, each with a concrete
example, nothing padded.

If you're running long, tighten before you cut: prefer a compact **table over verbose
bullets**, fold peripheral lists into a sentence, simplify or drop a figure, and delete
restated points. Only if still over, reconsider whether a subtopic really belongs here
or in a sibling question. Don't pad a thin answer to look thorough, and don't bloat a
complete one — match the siblings.

## Validating and presenting

Detect the environment and act accordingly:

**Claude Code / local repo** (you can edit files in the repo directly): Write or edit
the target `.typ` file in place. **Don't auto-compile to "verify"** — the user builds
locally, and content-only snippets can't compile standalone anyway (no preamble).
Ensure correctness by mirroring known-good sibling patterns. If you genuinely need to
check a tricky figure, ask first, then validate in a throwaway file that wraps the
snippet with the needed preamble — don't touch the user's build.

**Claude.ai web sandbox** (`present_files` available, `/mnt/user-data/` exists):
Write the source to `/home/claude/<topic-slug>.typ`, ensure `typst` is installed
(`typst --version 2>/dev/null || install it`), and compile to PDF to validate; fix
errors and retry until clean. Then copy to `/mnt/user-data/outputs/`, renaming the
source to `.txt` (the app doesn't render `.typ`), and call `present_files` with the
PDF first, the `.txt` second. Note: pure content-only Typst compiles fine standalone;
only cetz figures need the `#import "@preview/cetz:0.5.2"` line added for the
validation compile (and mentioned to the user).

## Minimal example of correct output

Starts with a real section (not the topic title), content-only, repo dash convention:

```typst
Relační databáze ukládají data do tabulek (relací) propojených přes klíče.

= Klíče

*Primární klíč* jednoznačně identifikuje řádek tabulky. *Cizí klíč* odkazuje na
primární klíč jiné tabulky a tím realizuje vztah mezi relacemi.

== Typy klíčů

#table(
  columns: (auto, 1fr),
  table.header([*Klíč*], [*Význam*]),
  [Primární], [Jednoznačná identifikace řádku, nesmí být prázdný.],
  [Cizí],     [Odkaz na primární klíč jiné tabulky.],
)
```
