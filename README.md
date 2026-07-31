# benchtools

A tiny, single-page sequence toolbox for the bench. Paste a DNA/RNA sequence — or a whole batch — and get the things you reach for fifty times a day: reverse complement, transcription, translation, GC%, Tm, molecular weight, base composition, and concentration⇄molarity, updating live as you type.

No install, no build step, no backend. It's one `index.html` that runs entirely in your browser; your sequences never leave the page.

**▶ Live app: https://cadenzhao.github.io/benchtools/**

## Use it

**[Open the live app](https://cadenzhao.github.io/benchtools/)** — it runs instantly in your browser, nothing to install or download. Click **Load example** in either tab to fill in a worked example and see every panel populate.

The whole thing is a single [`index.html`](index.html); you can also download that one file and open it locally, or self-host it anywhere static files are served.

## What it computes

**Single mode** (one sequence, live):

- **Reverse complement**, **RNA** (transcription), **Protein** (frame +1, standard genetic code)
- **Length**, **GC%**, and **base composition** (A/C/G/T·U counts and %)
- **Tm** — Wallace rule below 14 nt, otherwise the GC-based formula `64.9 + 41·(GC−16.4)/length`
- **Molecular weight** — anhydrous ssDNA, dsDNA (both strands), and ssRNA
- **Concentration ⇄ molarity** — convert ng/µL ↔ nM for the sequence (choose ssDNA/dsDNA/ssRNA), with µM and copies/µL
- **Six-frame translation** and **longest ORF** — all three forward and reverse frames, with the longest ATG→stop ORF highlighted
- **Restriction sites** — scans common cloning enzymes (EcoRI, BamHI, HindIII, NotI, XhoI, …) and reports counts and positions

**Batch mode** — paste FASTA or one sequence per line and get a table of length, GC%, Tm, reverse complement, RNA, protein, and restriction sites for every sequence, then **download it as TSV, CSV, or Excel (`.xlsx`)**. The `.xlsx` is written in-page by a tiny built-in ZIP writer — no library, no upload — with numeric columns as real numbers so Excel, openpyxl, and pandas all read them correctly.

These are quick sanity checks (e.g. eyeballing a primer), not a replacement for a full primer-design suite.

## Why

The web has plenty of bloated, ad-heavy sequence sites. This is the opposite: one file, instant, private, readable. Fork it and add the calculation you personally keep needing.

## License

[MIT](LICENSE).
