# nyrvo.dev

The landing page for [Nyrvo](https://github.com/nyrvo-dev/nyrvo), served by
GitHub Pages from `main`.

One file. `index.html` is the whole site: no build step, no framework, no
package manager. Open it in a browser and what you see is what deploys.

## No third-party requests

The page loads nothing from anyone else — no webfonts, no icon CDN, no
analytics, no cookies. That is a constraint rather than an omission: the page
argues that Nyrvo sends nothing anywhere unasked, and it would be a poor
argument coming from a page that opens three connections to render itself. The
typography is a system stack for the same reason.

It also means the site works offline, loads on a bad connection, and has
nothing to disclose under GDPR or LGPD.

## Content rules

Two, and they are the point of the page rather than decoration on it:

1. **Terminal output is real.** The blocks are output the tool actually printed,
   copied verbatim. Where lines are cut, the cut is marked and the caption says
   so. If a number changes because the tool changed, re-run the command and
   paste the new output — do not edit the old one.
2. **Nothing claims what has not shipped.** The Nyrvo Cloud section says plainly
   that none of it is built. There is no email capture, because there is nothing
   to email anyone about yet and a form that silently discards an address would
   be the only dishonest thing here.

## Bilingual

English and Brazilian Portuguese live in one `COPY` object in `index.html`. The
toggle sets `document.documentElement.lang`, remembers the choice in
`localStorage`, and falls back to the browser's language.

The Portuguese is written, not machine-translated. Command names, flags and rule
identifiers like `runtime.requirement_unsatisfied` stay in English in both: they
are identifiers, not phrases.

## Design source

The visual design came from a Claude Design project using the Nocturne design
system. This repository holds the exported static version; the tokens are
inlined at the top of `index.html`.
