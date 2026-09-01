# MUS 10 — Module 10 Interactives

Self-contained HTML activities for *American Popular Music*, Module 10 (soul, country
crossover, Broadway, the counterculture). Each file embeds into a Canvas page via `<iframe>`.

## Publishing

1. Create a **public** repo named `mus10-interactives` and push these files to `main`.
2. Repo **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)`.
3. Wait for the green check, then visit <https://dartpac.github.io/mus10-interactives/>.

The Canvas pages already point at that address — each activity is referenced as:

```
https://dartpac.github.io/mus10-interactives/<activity>.html
```

The repo name matters. If you call it anything other than `mus10-interactives`,
the Canvas embed URLs will need updating to match.

## Why GitHub Pages rather than Canvas pages

Canvas strips `<script>` and `<style>` from its rich content editor, so interactive
activities cannot run inside a native Canvas page. Hosting them here and embedding by
iframe keeps the lesson text native to Canvas — searchable, mobile-app friendly — while
the activities keep their JavaScript.

## Accessibility

Every activity was verified with axe-core against `wcag2a, wcag2aa, wcag21a, wcag21aa`
on its initial state *and* after interaction, and completed using the keyboard alone.

- All controls are real `<button>` and `<select>` elements — no click handlers on `<div>`s.
- State is never signalled by colour alone (WCAG 1.4.1): every correct/incorrect and
  selected/unselected state carries a glyph, border change, or text label as well.
- Feedback is announced through an `aria-live="polite"` region.
- Focus is preserved across DOM updates rather than resetting to the top of the page.
- `prefers-reduced-motion` is respected.
- "Find the One" is audio-based, so the same rhythm is also shown visually as bar heights
  and described in text — it is completable with no audio at all.

## Files

| File | Lesson | Type |
|---|---|---|
| `chart-sorter.html` | 10.1 | Two-bin sorting |
| `nashville-cloze.html` | 10.2 | Dropdown cloze |
| `soul-timeline.html` | 10.3 | Stepped timeline |
| `aaba-form.html` | 10.4 | Click-to-label |
| `find-the-one.html` | 10.5 | WebAudio rhythm |
| `broadway-match.html` | 10.7 | Matching pairs |
| `counterculture-marks.html` | 10.9 | Mark the statements |
| `module-review.html` | Review | Flashcards with self-rating |

## Branding

Dartmouth Green `#00693E`, Forest Green `#12312B`, white. Type is
`"National 2", Aptos, "Helvetica Neue", Arial`. National 2 is licence-restricted and is
never embedded — the stack degrades cleanly.
