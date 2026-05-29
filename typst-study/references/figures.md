# Figures (cetz) — when and how

Figures are **optional** and should be used **sparingly**. Add one only when a diagram
genuinely makes an idea clearer than prose would — a tree, a mapping, a sequence of
states. Most questions need none, and different topics suit different (or no) diagrams,
so pick what fits and don't add a figure for its own sake.

Don't build a canvas from scratch. Copy the closest working figure from a sibling file
and change the data — they already compile and match the house look:

- **Box rows** (arrays, sorting steps, memory layout) — see `algoritmy/razeni_vyhledavani.typ`.
- **Trees** (BST, heap, decision tree) — see `algoritmy/razeni_vyhledavani.typ`.
- **Mapping / translation** (A→B relations, lookup, address translation) — see `algoritmy/operacni_system.typ`.

Keep them small: when a figure is too big, reduce the number of elements (fewer
nodes/rows) before shrinking text. cetz figures need `#import "@preview/cetz:0.5.2"` in
the host document's preamble — since the snippet is content-only, mention this to the
user rather than putting it in the snippet.
