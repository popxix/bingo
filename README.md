# Bingo

A tiny, dependency‑free web app (plain HTML + CSS + JS). Each click/key reveals one random image,
never repeating, until all 35 are on the board. Start a new game and the order is reshuffled.

## Files
- `index.html`  – the whole app (styles + script inline)
- `images/`     – the 35 PNGs (≈ 8 MB total)

## Host it (free options)
Upload the folder as‑is (keep `index.html` next to `images/`):
- **GitHub Pages**: push to a repo → Settings → Pages → deploy from branch.
- **Netlify Drop** (app.netlify.com/drop) or **Cloudflare Pages**: drag & drop the folder.

## Controls
| Action | Button | Key |
|---|---|---|
| Next image | Next image | Space / Enter / → |
| Undo last | Undo | Backspace / ← |
| New game (reshuffle) | New game | R (then Enter to confirm) |
| Fullscreen | Fullscreen | F |
| Hide / show top bar | Hide bar | H |
| Big reveal on/off | Big reveal | S |

URL options: `?title=My+Game`  `?spotlight=0` (no big reveal)  `?kiosk=1` (start with bar hidden)

## Embed in Canvas (iframe)
```html
<iframe src="https://YOUR-HOST/index.html" title="Bingo"
        style="width:100%;height:80vh;border:0" allowfullscreen
        allow="fullscreen"></iframe>
```
Click once inside the app so it receives keyboard focus (needed for Space/arrow keys).
If Canvas blocks fullscreen inside the embed, open the page in its own tab and press F.

## Customise
Top of the `<script>` in `index.html`: `TITLE`, `SPOTLIGHT_MS` (seconds the big image stays up), and the `IMAGES` list
(file name in `/images` + spoken name). To swap/add pictures, replace the PNG or edit the list; the board
adapts to the number of images (35 gives a clean 7×5 grid).
