# fe-v2-static-starter

A static starter: plain `index.html`, `styles.css` and an **empty** `script.js`. No build step, no
dependencies, nothing to install.

## Run it

Open `index.html` **directly in your browser** — double-click it, or drag it onto a browser
window. An address bar starting `file://` is correct; there is no server to run.

You should see the starting page before you change anything. Edit a file, save, reload.

Then press **F12** and leave the **Console** tab open. A JavaScript error appears there and
nowhere else, and a blank page with a red line in the console is a typo rather than a broken
machine. This is the single biggest difference between working on a page and guessing at one.

## What is in here

| File | What it is |
|---|---|
| `index.html` | The page. The panel inside `<main>` is a placeholder — replace it. |
| `styles.css` | Layout, typography and the tokens (colours, spacing, radius, type scale). |
| `script.js` | **Empty, on purpose.** Your JavaScript goes here — not in inline `onclick` attributes. |
| `data/labels.js` | ShareChat: label strings for six Indic languages. |
| `data/transactions.js` | Jupiter: three months of transactions, plus the month list. |

## Find your data

This template is shared by two projects. `index.html` loads both files; each defines one global.

| Project | File | Global |
|---|---|---|
| ShareChat — language switcher | `data/labels.js` | `LABELS` |
| Jupiter — spend insights | `data/transactions.js` | `TRANSACTIONS`, `MONTHS` |

Delete the `<script>` line for the one you are not using if you would rather have a clean page.

Two details that were put there for you, and are worth knowing:

- **`LABELS` carries the same keys in every language**, so "every visible label swaps" is
  actually achievable. Add new copy as a key in all six, never as a string typed into the HTML —
  that is the one that stays in English after a switch.
- **`MONTHS` includes September 2026, which has no transactions.** Your brief asks for a real
  empty state, and a month list derived only from the data could never reach one.

⚠️ The `<script>` tags are plain, **not** `type="module"`. A module opened over `file://` is
blocked by the browser's CORS rules, so the page would silently do nothing. If you change them,
you will need a local server.

## What is deliberately NOT in here

The thing you were asked to build. The switching, the computing, the formatting and the states
your tickets describe are the project — this repository is the starting point, not a worked
example.
