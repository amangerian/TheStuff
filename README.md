# TheStuff

The landing page that links to every site I've built. One file: `index.html`.

**Live at https://amangerian.github.io/TheStuff/**

## Updating it

On GitHub: **Add file → Upload files**, drop in `index.html`, commit. GitHub
replaces the old one. Hard-refresh (Cmd+Shift+R) — Pages caches for a few minutes.

## Adding a site

Append one line to the `SITES` array between the `SITE REGISTRY START` /
`SITE REGISTRY END` comments:

```js
{ title: 'Display Name', what: 'Three-word description', url: 'https://amangerian.github.io/<repo>/', icon: 'network', color: '#7dd3fc' },
```

`icon` is one of: `network` · `feed` · `board` · `dashboard` · `paw` · `breath` · `heart`.

## Sites

| Site | Repo | Live |
| --- | --- | --- |
| NeuroNet Atlas | `neuronet-atlas` | https://amangerian.github.io/neuronet-atlas/ |
| Your Journal | `yourjournal` | https://amangerian.github.io/yourjournal/ |
| Board Study Games | `MPboardstudy` | https://amangerian.github.io/MPboardstudy/ |
| MedBoard Prep | `med-board` | https://amangerian.github.io/med-board/ |
| 3D Zoo | `3DZoo` | https://amangerian.github.io/3DZoo/ |
| CPAP Maintenance | `CPAPMaintain` | https://amangerian.github.io/CPAPMaintain/ |
| A Love Quest | `Wedding-Quest` | https://amangerian.github.io/Wedding-Quest/ |
