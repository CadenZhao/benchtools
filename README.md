# benchtools

A tiny, single-page sequence toolbox for the bench. Paste a DNA/RNA sequence and get the things you reach for fifty times a day — reverse complement, transcription, translation, GC%, melting temperature, molecular weight — updating live as you type.

No install, no build step, no backend. It's one `index.html` that runs entirely in your browser; your sequences never leave the page.

## Use it

Open [`index.html`](index.html) — that's the whole app. Or host it for free on GitHub Pages and bookmark it next to your bench.

## What it computes

- **Reverse complement** and **RNA** (transcription)
- **Protein** — translation in frame +1, standard genetic code
- **GC%**, **length**
- **Tm** — Wallace rule below 14 nt, otherwise the GC-based formula `64.9 + 41·(GC−16.4)/length`
- **Molecular weight** — anhydrous single-stranded DNA approximation

These are quick sanity checks (e.g. eyeballing a primer), not a replacement for a full primer-design suite.

## Why

The web has plenty of bloated, ad-heavy sequence sites. This is the opposite: one file, instant, private, readable. Fork it and add the calculation you personally keep needing.

## License

[MIT](LICENSE).
