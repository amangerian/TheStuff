# amangerian.github.io

The landing page that links to every site I've built. One file: `index.html`.

**Live at https://amangerian.github.io/** — the bare root, no repo path, because
the repository is named after the account.

## First-time setup (once)

1. On GitHub: **New repository**, named exactly **`amangerian.github.io`**, Public.
   The name has to match the account name — that is what makes it serve from the
   root URL instead of `/<repo>/`.
2. **Add file → Upload files**, drop in `index.html` (and this README if you want),
   **Commit changes**.
3. **Settings → Pages → Source: Deploy from a branch**, branch `main`, folder
   `/ (root)`. Save.
4. Live in a minute or two at https://amangerian.github.io/.

## Updating it

Open `index.html` on GitHub → pencil icon → paste the new contents → commit.
Or **Add file → Upload files** and drop the same filename in; GitHub replaces it.
Hard-refresh (Cmd+Shift+R) — Pages caches for a few minutes.

## Adding a project to it

Everything the page shows comes from the `SITES` array between the
`SITE REGISTRY START` / `SITE REGISTRY END` comments near the bottom of the file.
Append one object and the card, its tags, and the filter chips all follow:

```js
{
  id: 'short-slug',
  title: 'Display Name',
  kicker: 'Two-word category',
  url: 'https://amangerian.github.io/<repo>/',
  repo: '<repo>',
  icon: 'network',           // network | feed | board | dashboard | breath
  c1: '#7dd3fc', c2: '#3b82f6',   // accent gradient for the card
  blurb: 'One or two sentences on what it does.',
  topics: ['Board review'],  // drives the filter chips — reuse existing ones
  tags: ['Display', 'Chips', 'Only']
}
```

`topics` are filterable and should stay a short shared vocabulary
(Board review · Clinical · Neuroscience · Research). `tags` are decoration only,
so they can be anything.

The `new-site` skill does this for you — ask Claude to add the new site to the hub.

## Sites it links to

| Project | Repo | Live |
| --- | --- | --- |
| NeuroNet Atlas | `neuronet-atlas` | https://amangerian.github.io/neuronet-atlas/ |
| Your Journal | `yourjournal` | https://amangerian.github.io/yourjournal/ |
| Board Study Games | `MPboardstudy` | https://amangerian.github.io/MPboardstudy/ |
| MedBoard Prep | `med-board` | https://amangerian.github.io/med-board/ |
| CPAP Maintenance | `CPAPMaintain` | https://amangerian.github.io/CPAPMaintain/ |

## Notes

- No build step, no dependencies, no external requests — the fonts are system
  fonts and the favicon is an inline SVG data URI, so the page renders with no
  network at all.
- Dark and light both come from `prefers-color-scheme`; there is no toggle.
- The drifting node background is a `<canvas>` that switches itself off for
  `prefers-reduced-motion` and pauses when the tab is hidden.
