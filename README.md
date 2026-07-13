# Mission Metrics™ — What We Build (Conference Loop)

A single, self-contained HTML attract loop for the trade-show table monitor.

**Live:** deployed on Vercel — open it, press `F`, walk away.

## What it is

13 slides, ~2m 15s per rotation, cycling forever:

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
| 09 | — THE PROOF — |
| 10 | Silverback Enterprises *(5 pages)* |
| 11 | BRBR Collection *(6 sections)* |
| 12 | Compassion for Lives *(6 sections)* |
| 13 | Let's talk at the table *(QR + contact)* |

Every product slide **cycles through the real pages of that product's site**,
cross-fading inside a browser frame while the copy holds — 52 real screenshots
in total, captured live from each deployment.

## The one rule it was built around

**It runs with the wifi off.** Conference networks die. So every screenshot, the
QR code, and the entire GSAP animation library are embedded directly in
`index.html`. The page makes **zero network requests** — verified by loading it
with every request blocked at the browser level.

## Controls

| Key | Action |
|---|---|
| `SPACE` / click | pause & resume |
| `←` `→` | step between slides |
| `F` | fullscreen |

## Editing

- **Contact details** — search `id="c-phone"` near the bottom of `index.html`.
- **Slide timing** — each `<section class="scene">` carries `data-dur` (seconds).

## Notes

- Transitions follow the HyperFrames rules: entrance animations on every scene,
  no jump cuts, no exit animations except the final slide.
- The **Bookkeeping figures are demo data**, generated for this loop. The product
  ships as a blank slate.
