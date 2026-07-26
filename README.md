# Minna-James-Heineman-Stiftung — Website

A single-file static website. No build step, no dependencies, nothing to install. Everything — text, styling, and the logo — lives in `index.html`. Double-click it to open in any browser.

Same design system as the Heineman Foundation site.

## How to edit

Open `index.html` in any text editor and search for what you want to change:

| To change...              | Search for...                        |
|---------------------------|--------------------------------------|
| Contact email             | `mailto:`                            |
| About text                | `id="about"`                         |
| History text              | `id="history"`                       |
| Board roster              | `class="board-officers"`             |
| Grant programs            | `id="grants"`                        |
| Publications              | `id="publications"`                  |
| Colors and fonts          | `:root {` (near the top)             |

## Links to fill in

Several links in the text (Max-Planck-Gesellschaft, Weizmann Institute, "Click here" lists, etc.) are placeholders pointing to `href="#"`. To make one active, search for `href="#"` and replace the `#` with the real URL. Each placeholder sits on the text it links, so they're easy to find in order.

## Hosting on GitHub Pages

1. Create a new repository on GitHub and upload `index.html` to it.
2. Go to **Settings → Pages**.
3. Under **Source**, select branch `main` and folder `/ (root)`.
4. Save. The site goes live at `https://<username>.github.io/<repo-name>/`.

For a custom domain, add it under **Settings → Pages → Custom domain** and point your DNS at GitHub Pages.

## Notes

- The logo is embedded directly in the file, so nothing external is needed for it to display — it works offline too.
- The two fonts (Fraunces and Inter) load from Google Fonts, which needs an internet connection. Offline, the page falls back to Georgia and your system's default sans-serif.
- The bank/donation account details (IBAN, BIC) from the old site are intentionally left out. To add them, put them in the Contact section under the Donations heading.
