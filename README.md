# Minna-James-Heineman-Stiftung — Website

A small static website — no build step, no dependencies. Every page is a self-contained HTML file with the logo embedded, so each one works on its own (locally or on GitHub Pages).

## Pages

| File | What it is |
|------|------------|
| `index.html` | Main page (About, History, Board, Grants, Publications, Contact) |
| `cooperative-research-projects.html` | Grants sub-page: list of cooperative research projects |
| `james-heineman-research-award.html` | Grants sub-page: award + awardees |
| `dannie-heineman-award.html` | Grants sub-page: award + awardees (bilingual citations) |

The three sub-pages are reachable from the **Grants** dropdown in the top navigation and from links within the Grants section of the main page.

## How to edit

Open any file in a text editor and search for what you want to change:

| To change... | Search for... |
|--------------|---------------|
| Contact email | `mailto:` |
| Board roster | `class="board-officers"` (officers) / `class="board-member"` (members) |
| Grant program text | `id="grants"` in `index.html` |
| An awardee or project | open the relevant sub-page and edit the entry |
| Colors and fonts | `:root {` near the top of any file |

### Board members

Each board member is a small block: the name (with optional link) on the first line, and their title/affiliation on the second. To edit one, find `class="board-member"` and change the text inside `bm-name` and `bm-affil`. The `*` (Coordination Committee marker) is the `finance-star` span.

## Links to fill in

Many links in the body text (Max-Planck-Gesellschaft, Weizmann Institute, individual awardee pages, etc.) are placeholders pointing to `href="#"`. To make one active, search for `href="#"` and replace the `#` with the real URL. The links between the main page and the three Grants sub-pages are already wired up.

## Editing note: the logo

The logo is embedded directly in every page as base64 data, so it displays with no external file and works offline. If you ever replace the logo, it has to be updated in all four files (search for `data:image/png;base64,` in each).

## Hosting on GitHub Pages

1. Upload all four `.html` files (and this README) to a GitHub repository — keep them in the same folder so the links between pages work.
2. Go to **Settings → Pages**.
3. Under **Source**, select branch `main` and folder `/ (root)`.
4. Save. The site goes live at `https://<username>.github.io/<repo-name>/`.

## A note on the Dannie Heineman Award page

Each award citation is shown in the original German first, with an English translation in italics beneath it, matching the original site. If you'd prefer English-only (or German-only), let me know and it can be simplified.

## A note on fonts

The two fonts (Fraunces and Inter) load from Google Fonts, which needs an internet connection. Offline, pages fall back to Georgia and your system's default sans-serif. Everything else, including the logo, is self-contained.
