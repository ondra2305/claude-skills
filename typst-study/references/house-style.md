# House style of this repo (statnice)

Concrete conventions of *this* study set. The general principle (workflow step 1) is
to learn the style from finished siblings; this file records what you'll find so you
don't have to rediscover it every time. If the repo evolves, trust the actual files
over this note.

## Repo layout

Questions live in topic folders: `algoritmy/`, `databaze/`, `matematika/`, `signaly/`,
`site/`, `hardware/`. Each question is one `.typ` file. Shared machinery is in
`utils/` (notably `utils/include.typ`, which exports `meta`).

## File anatomy (what the full file looks like)

You output **content only**, but the file it gets pasted into looks like this. Know
the shape so you can fill the `meta(...)` fields if asked, and so you understand why
the content must not repeat the title or add a preamble:

```typst
#import "../utils/include.typ": *
// figures only: #import "@preview/cetz:0.5.2"
#let meta = meta(
  question: [Full question text, exactly as assigned.],
  question_short: [Short title for nav/TOC],
  author: [Name],
  difficulty: 50%,   // author's subjective difficulty of the material
  ai: 40%,           // roughly how much of the content is AI-generated
)

= First real section
... your content starts here ...
```

The `= First real section` heading and everything after it is **your** output. The
import + `meta` block is added by whoever owns the file.

### meta fields

- `question` / `question_short` — assigned, don't paraphrase the long form.
- `author` — the person responsible for the write-up.
- `difficulty` — subjective difficulty of the material (0–100%).
- `ai` — rough share of AI-generated content. Bump it when you've written or
  restructured a large part; don't leave it at 0% if you authored most of it.

## Finished examples to read for style

These are substantial, validated write-ups — good style references:

- `algoritmy/jazyk_c.typ` — prose + code blocks + a `#table`.
- `algoritmy/razeni_vyhledavani.typ` — prose + tables + two cetz figures (tree, box rows).
- `algoritmy/operacni_system.typ` — prose + table + a cetz mapping diagram.
- `databaze/pohledy.typ`, `matematika/pravdepodobnost.typ` — other domains.

## Prose conventions

- **Language:** Czech, formal and factual (academic register). Full sentences, not
  telegraphic notes. No first-person, no chatty asides, no marketing superlatives.
- **Emphasis:** `*bold*` for key terms on first introduction; don't over-bold. Inline
  code in backticks for identifiers, functions, keywords.
- **Definitions:** open a section by defining the central term, then elaborate.
- **Tables** for comparisons and "vlastnosti" overviews; always wrap the header row in
  `table.header(...)`. A compact table is often better than a long bullet list.
- **Ordered procedures** use `+` (numbered); unordered facts use `-`.
- **Dashes:** `--` (en) for parenthetical dashes and ranges, `---` (em) rarely. Never
  Unicode `–`/`—`.

## Cross-references between questions

There is currently **no label/ref mechanism** between questions, so reference in prose
by name (use a real cross-reference if one is later added). When a topic is owned in
depth by another question, point there instead of duplicating, e.g.:

> Konkrétní plánovací algoritmy a synchronizační primitiva rozebírá samostatná otázka
> o programátorském rozhraní operačního systému; zde je proto jen zmiňujeme.

This keeps each answer self-contained without duplicating a sibling's depth.
