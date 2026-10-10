# QR Studio

Generate QR codes for text or URLs in the browser. Size selector (256 / 512 / 1024 px), dark/light style toggle, one-click **Download PNG**.

## How to use

Open `index.html`, type text or a URL — the QR code renders live as you type. Pick a size and style, then hit **Download PNG**.

## How it works

- Encoding uses `qrcode-generator` (kazuhikoarase, MIT) — the single-file library lives at the top of `app.js`; there are no CDN or network requests.
- Version is auto-detected, error correction level M, quiet zone included.
- Rendering draws modules onto a `<canvas>` at the exact requested pixel size; the PNG download is the canvas bitmap, so it's pixel-perfect.
- Overly long input shows a clear error instead of a broken code.

## Files

- `index.html` — the page markup (title, text box, size/style controls, preview, download button)
- `styles.css` — all the styling (colors, card, controls, preview frame, mobile tweaks)
- `app.js` — the code in two parts: the inlined QR library (section comments explain it) and our own app code (line-by-line plain-English comments)
