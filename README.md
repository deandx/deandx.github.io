# deandx.github.io

Personal site for Jiaming Ding — https://deandx.github.io

Plain static HTML + CSS. The layout follows
[academicpages](https://github.com/academicpages/academicpages.github.io)
— masthead nav, left author sidebar, content column — styled in Apple's design
language: SF Pro type with tight tracking, a frosted translucent nav bar,
`#f5f5f7` ground with white rounded cards that fade up as they scroll into
view. Dark mode follows the OS. No Jekyll, no build
dependencies, no external assets or fonts.

## Editing

Everything lives in two files: [`index.html`](index.html) for content and
[`style.css`](style.css) for styling. The nav links are in-page anchors
(`#about`, `#news`, `#publications`), so adding a section means adding a
`<section id="...">` and a matching nav item.

### Publication entries with a figure

Drop the teaser figure in [`figs/`](figs/), then give the `<li>` the
`has-figure` class and point `.entry-figure` at the file:

```html
<li class="has-figure">
  <img class="entry-figure" src="figs/my-paper.png" alt="" width="320" height="200">
  <div>
    <div class="entry-head">…title and year…</div>
    <div class="entry-sub">…authors and venue…</div>
    <p>One sentence on the paper.</p>
    <div class="entry-links">…links…</div>
  </div>
</li>
```

The thumbnail is 13rem wide beside the text and stacks above it under 52rem.
Entries without the class stay full-width text. `figs/placeholder.svg` is the
stand-in used by the example entry — delete it once real figures are in.

## Local preview

```bash
python3 -m http.server 8000
```

## Publishing

Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`.

## Todo

- [ ] Fill in the LinkedIn URL in the sidebar; uncomment the location line above it.
- [ ] Swap the personal email in for the work one, if you'd rather not publish the work address.
- [ ] Replace the placeholder publication entries and `figs/placeholder.svg` (News is filled in).
