# benchtools

A tiny, single-page sequence toolbox for the bench. Paste a DNA/RNA sequence and get the things you reach for fifty times a day — reverse complement, transcription, translation, GC%, melting temperature, molecular weight — updating live as you type.

No install, no build step, no backend. It's one `index.html` that runs entirely in your browser; your sequences never leave the page.

**▶ Live app: https://cadenzhao.github.io/benchtools/**

## Use it

**[Open the live app](https://cadenzhao.github.io/benchtools/)** — it runs instantly in your browser, nothing to install or download.

The whole thing is a single [`index.html`](index.html); you can also download that one file and open it locally, or self-host it anywhere static files are served.

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
