# Cell Hub - releases

Installers only. No source code lives here.

This repository is the auto-update feed for Cell Hub desktop builds. Each shop's
build reads only its own manifest, so a release can never hand one shop another
shop's branding:

| Shop | Manifest |
|---|---|
| Cell Hub | `cell-hub.yml` |

## Rules

- Every release must contain, for each shop: `<channel>.yml`, the installer
  `.exe`, and the `.exe.blockmap`. A missing `.yml` means that shop never
  updates, and the release still looks complete.
- Never delete or re-tag a published release. Shops compare their installed
  version against the newest published one.
- To fix a bad release, publish a higher version. Downgrades are refused by the
  app on purpose.
- This repo must stay public. The app downloads from it with no credentials, and
  a private repo would require shipping a token to every client's PC.

See `UPDATES.md` in the Cell Hub source repo for the full release process.