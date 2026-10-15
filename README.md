# VOIDNET v1.0 — Browser foundation (development build 0.1)

This is the **first implementation milestone**, not the completed VOIDNET release.

## Run locally

```bash
npm install
npm run dev
```

Open the local URL printed by Vite. To make a production build:

```bash
npm run build
```

Deploy the contents of `dist/` to GitHub Pages. The Vite relative base path supports project subpaths. Because this is a single-page browser with internal `.void` routes, it does not need server-side routing.

## Included now

- Registry with **all 251 approved original `.void` addresses in their approved order**.
- Browser shell with multiple tabs, back/forward, home, address entry and refresh-view control.
- `search.void` foundation search with exact/partial/fuzzy matching and **10 random discoverable results if there are no matches**. No all-sites directory is exposed by search.
- Separate developer-only website registry panel, **not** a public VOIDNET website.
- Local bookmarks, timestamped browser history, visited-site tracking, theme, browsing mode and tab persistence.
- Free Browse / Story Mode preference (story progression and endings **not yet implemented**).
- Early `voidai.void` prototype: scripted Dave chat and simulated local install/uninstall with floating widget.
- Responsive desktop/mobile navigation.

## Not included yet

- The 251 completed websites and their approved content, games, videos, interactions and secrets.
- Finished Dave response corpus, contextual reactions, installation wizard and polished controls.
- Story objectives, V1 ending and V2 access entitlement.
- Supabase authentication, verification, sync and account deletion.
- Automated test suite and full accessibility/security audits.

**Important:** All unimplemented websites display a clear development placeholder. They are not represented as finished. `endofinternet.void` is not a functioning ending in this milestone.

## Development structure

- `src/registry.ts`: canonical site address registry and discovery helpers.
- `src/main.tsx`: current browser shell and prototype screens. Split into modules as foundation expands.
- `src/style.css`: responsive theme and browser UI.

## Approved future rules

- Free Browse: unrestricted access to all **released** sites, no V1/V2 story endings.
- Story Mode: progression-gated access to expansion sites; V1 ending unlocks V2 when released.
- V3 `nottheend.void`: available in both modes; Dave reviews exactly 10 selected timestamped memorable visits. Not part of V1 build.
- No real `.void` DNS domains, real downloads, system modifications or paid AI service.

## Security and privacy notes

Current prototype uses `localStorage` for guest browser data. Do not store passwords or sensitive information here. The later Supabase stage will require a proper security design and row-level policies. This is not a security-audited production release.


## Public GitHub Pages deployment

See **GITHUB-PAGES-SETUP.md**. The repository includes `.github/workflows/deploy.yml`, which builds with Node.js 22 and deploys `dist/` automatically on pushes to `main`. In GitHub Settings > Pages, choose **GitHub Actions** as the deployment source.
