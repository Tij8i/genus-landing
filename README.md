# genus-landing

Public landing site for the [Genus](https://github.com/Tij8i/Genus) protocol.

- **Canonical URL:** [https://genus.work](https://genus.work)
- **Repo:** `Tij8i/genus-landing`
- **License:** MIT

## What this is

A 1-page static landing site for the Genus Agent Operating Model. Explains
what Genus is, names the three archetypes (Virgil, Stewart, Mason), and points
visitors at the spec repo `Tij8i/Genus`.

This is deliberately separate from `Tij8i/Genus` (which holds the spec docs and
the internal dashboard at `genus-v06.pages.dev`) so the public marketing
surface can evolve independently of the protocol repo.

## Layout

```
/
├── index.html      Single-page landing
├── styles.css      Stylesheet (Hanken Grotesk + JetBrains Mono)
├── _headers        Cloudflare Pages security headers + cache rules
├── LICENSE         MIT
└── README.md       This file
```

No build step. Cloudflare Pages serves files directly from the repo root.

## Deploy (one-time setup, in Cloudflare dashboard)

1. **Workers & Pages → Create application → Pages → Connect to Git**
2. Pick repo `Tij8i/genus-landing`, branch `main`
3. **Build settings:** all defaults — framework `None`, build command blank,
   output directory blank (Pages serves from repo root)
4. Save & deploy — you'll get a `*.pages.dev` URL
5. **Settings → Custom domains:** add `genus.work`

DNS is managed automatically when the domain is registered via Cloudflare
Registrar and bound to the Pages project.

## Editing

Open `index.html` / `styles.css`, push to `main`. Pages auto-deploys.
Keep changes light — this is a marketing landing, not the protocol spec.
The source of truth for the protocol stays in
[`Tij8i/Genus`](https://github.com/Tij8i/Genus).
