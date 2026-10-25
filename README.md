# Compass for Windows

**Your documents. Searchable. On your computer.**

Compass searches the files already on your computer. Local document search,
source verification, Deep Search, Analytics, English OCR and PDF table extraction.

- Website: https://leapfrog7.github.io/compass/
- Latest stable release: https://github.com/leapfrog7/compass/releases/latest
- Windows installer: https://github.com/leapfrog7/compass/releases/latest/download/Compass-Setup.exe

This repository hosts the single-page download website and release assets.
Build inputs, tests, evaluation data and private documents are not distributed here.

## Website

Buildless HTML and CSS, system fonts, local SVG icons and an existing real Compass
screenshot. No JavaScript, external fonts, analytics service or tracking is needed.
GitHub Pages serves `main` from the repository root. Preserve the latest-stable
installer alias when editing the page. The displayed version is the currently
published release; update it when a newer stable release is published.

The screenshot uses public sample content captured from the production renderer.
It is not a promise that every release has exactly the same controls. Regenerate
it from the app workspace with `node scripts/distribution/capture-site-preview.cjs`.

## Updating Compass

Check for updates in Compass and follow the instructions offered by your installed
version. Versions offering **Restart and install** perform the installer handoff
from the app. The latest release remains available at the link above.

Library data is separate from the application. Keep `%APPDATA%\Compass`: it holds
saved folders, database, indexes, embeddings, OCR-derived data and settings.
Updates reuse compatible indexed content. A genuine future model/index
incompatibility may require an explicit rebuild; follow that release's notes.
Back up source files and the Compass profile separately.

Portable users should close Compass before replacing application files. The
portable ZIP does not carry the saved Library between computers.

## Release convention

Stable releases use `v<version>` tags and include `Compass-Setup-<version>.exe`,
`Compass-Portable-<version>.zip`, `SHA256SUMS.txt`, release notes and
`Compass-Setup.exe` (a byte-identical installer alias). The main website download
uses GitHub's latest stable redirect, requiring no per-release URL edit.
Experimental builds must be prereleases and must not become the latest stable.

Windows 10/11 x64 builds include offline models. A compatible Microsoft Visual C++
x64 runtime is required. Current builds are unsigned; office security policies apply.
