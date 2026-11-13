# Retext

Edit the text in any PDF, right in your browser.

- **Edit text**: tap a line and type over it. Drag to move it.
- **Add text**: tap anywhere on a page.
- **Erase**: drag over anything to cover it.
- **Download** the edited PDF.

Your files never leave your device. Everything runs in the browser, so there is no server and no upload.

Works with Latin and Cyrillic text (including Mongolian).

## How it works

Retext draws each page with [PDF.js](https://mozilla.github.io/pdf.js/) and saves changes with [pdf-lib](https://pdf-lib.js.org/). When you change a line, it covers the old text with a patch in the page's background colour and writes the new text on top.

That means the original text is hidden, not deleted. It can still be found by search or copy-paste. **Do not use Retext to redact private information.**

## Limits

- The new text uses a close match (Noto Sans, Times or Courier), not the PDF's own font.
- Password-protected PDFs can't be saved.
- Lines on rotated pages can't be edited.

## Run it locally

It is one static page. Serve the folder with any static server:

```sh
npx serve .
```

## License

MIT for the code. The bundled Noto Sans fonts are under the SIL Open Font License (`fonts/OFL.txt`).
