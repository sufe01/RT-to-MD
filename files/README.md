# Rich Text to Markdown Editor

A free, browser-based editor. Write or paste formatted text, then download it as **Markdown, PDF, Word, HTML or plain text**. No server and no sign-up: everything runs in the visitor's browser.

## Features

- Paste from Google Docs, Word and web pages, or open a `.docx` / `.html` file
- Floating toolbar on text selection, plus a full top toolbar
- Headings 1 to 3, bold, italic, underline, strikethrough, highlight, links, quotes
- Bullet, numbered and nested lists (Tab / Shift+Tab)
- Text color, background color, bigger / smaller text, alignment
- Tables with a chosen number of rows and columns, and add / remove rows and columns afterwards
- Pictures from a link, an upload or the clipboard, with rounded corners, size and alignment
- Code blocks with a Copy button, and inline code
- Fonts: Google Sans Flex (default), Poppins, Montserrat, Inter, Roboto, Arial, Georgia, Consolas, any installed font by name, or your own uploaded font file
- Live Markdown panel (hidden until you press **Show Markdown**)
- Downloads: PDF, Word (.doc), Markdown (.md), HTML, TXT

## Files

| File | Purpose |
|------|---------|
| `index.html` | The editor |
| `how-to-use.html` | Step-by-step guide for visitors, linked from the editor |
| `README.md` | This file |

## Run it locally

Open `index.html` in a browser. An internet connection is needed because the libraries and fonts load from CDNs. To serve it locally instead:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`. This command starts Python's built-in web server in the current folder and serves only the files in it.

## Publish on GitHub Pages

1. Create a new repository on GitHub and upload `index.html`, `how-to-use.html` and `README.md` to its root.
2. Open **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select the `main` branch and the `/ (root)` folder, then **Save**.
4. After a minute your site is live at `https://<your-username>.github.io/<repository-name>/`.

## Libraries used

[Turndown](https://github.com/mixmark-io/turndown) and its GFM plugin (HTML to Markdown), [Mammoth](https://github.com/mwilliamson/mammoth.js) (.docx import), [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) (PDF), [Tom Select](https://tom-select.js.org/) (dropdowns), [SweetAlert2](https://sweetalert2.github.io/) (dialogs), [Lucide](https://lucide.dev/) (icons).

## Known limits

- Markdown cannot hold colors, font sizes, fonts, alignment or rounded pictures. Those appear in PDF, Word and HTML only.
- The Word export is an HTML-based `.doc` file. Word and Google Docs open it, but it is not a native `.docx`.
- Loading a picture link into the Markdown as embedded data only works for sites that allow cross-site requests.
- The editor uses the browser's `contenteditable` and `execCommand`, so small differences between browsers are possible.

## License

Add the license of your choice (for example MIT) before publishing.
