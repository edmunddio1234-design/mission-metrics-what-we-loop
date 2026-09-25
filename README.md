# Mission Metrics™ — What We Build (Conference Loop)

A single, self-contained HTML attract loop for the trade-show table monitor.

**Live:** deployed on Vercel — open it, press `F`, walk away.

## What it is

18 slides, ~4m 50s per rotation, cycling forever:

| # | Slide |
|---|---|
| 01 | See Your Impact. Grow Your Mission. |
| 02 | — THE PLATFORM — |
| 03 | Impact Operations™ Platform *(6 pages + live client instance inset)* |
| 04 | Training Academy *(6 pages)* |
| 05 | Mission Metrics Bookkeeping *(6 screens)* |
| 06 | Marketing Engine *(4 sections)* |
| 07 | Concrete Bid Copilot *(5 sections)* |
| 08 | Biblical Pathways *(4 sections)* |
| 09 | Impact Trading Academy *(6 motion clips)* |
| 10 | — THE PROOF — |
| 11 | Silverback Enterprises *(5 pages)* |
| 12 | BRBR Collection *(6 sections)* |
| 13 | Compassion for Lives *(6 sections)* |
| 14 | All is Well — Health & Wellness *(6 motion clips)* |
| 15 | Providence House — site + Leadership Dashboard *(6 motion clips)* |
| 16 | LCA Metal Services *(6 motion clips)* |
| 17 | IronBridge Medical Evidence *(6 motion clips)* |
| 18 | Let's talk at the table *(QR + contact)* |

Every product slide **cycles through the real pages of that product's site**,
cross-fading inside a browser frame while the copy holds — 52 real screenshots,
plus **30 motion clips** on the newer slides: short screen recordings of each live
site scrolling, animating and switching dashboard tabs, so the booth shows the
sites *moving*, not just still pictures.

## Media check (built in)

When the page opens it checks **every screenshot and every clip on every slide**:
images must decode to real pixels, clips must reach a playable frame. Each clip
carries a poster still — if a clip ever fails to play, it is swapped for that
still automatically, so a page can lose its motion but never go blank. The check
re-runs every 10 minutes. Press **`D`** for the slide-by-slide report (it opens by
itself if anything could not be repaired).

## The one rule it was built around

**It runs with the wifi off.** Conference networks die. So every screenshot, every
clip, the QR code, and the entire GSAP animation library are embedded directly in
`index.html`. The page makes **zero network requests** — verified by loading it
with every request blocked at the browser level.

## Controls

| Key | Action |
|---|---|
| `SPACE` / click | pause & resume |
| `←` `→` | step between slides |
| `F` | fullscreen |
| `D` | media check report |

## Editing

- **Contact details** — search `id="c-phone"` near the bottom of `index.html`.
- **Slide timing** — each `<section class="scene">` carries `data-dur` (seconds).

## Notes

- Transitions follow the HyperFrames rules: entrance animations on every scene,
  no jump cuts, no exit animations except the final slide.
- The **Bookkeeping figures are demo data**, generated for this loop. The product
  ships as a blank slate.
