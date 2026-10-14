# Compass for Windows

**Your documents, within easy reach**

Local PDF search, source verification, Deep Search, English OCR and extracted tables.

- Website: https://leapfrog7.github.io/compass/
- Latest stable release: https://github.com/leapfrog7/compass/releases/latest
- Windows installer: https://github.com/leapfrog7/compass/releases/latest/download/Compass-Setup.exe

This repository hosts the download page and release assets. Build inputs, tests,
evaluation data and private documents are not part of this distribution repository.

## Updating

Use **Help → Check for updates**, or visit the latest release. Verify the installer
against SHA256SUMS.txt, close Compass, then install over the current installation.
Portable users should close Compass and replace the extracted application files.
Leave `%APPDATA%\Compass` untouched: it contains the saved folders, database,
indexes, embeddings, OCR-derived data and settings. No blanket reindex is triggered.
A genuine future model/index incompatibility may require an explicit rebuild;
follow that release's compatibility notes. Back up AppData and PDFs separately.

## Release convention

Stable releases use `v<version>` tags and include `Compass-Setup-<version>.exe`,
`Compass-Portable-<version>.zip`, `SHA256SUMS.txt`, release notes, and
`Compass-Setup.exe` (byte-identical installer alias). The website's download link
uses GitHub's latest stable release redirect and therefore needs no per-release edit.
Experimental builds must be prereleases and must not become the latest stable.

Windows x64 builds include offline models. A compatible Microsoft Visual C++ x64
runtime is required. Current builds are unsigned; your Windows/office policies apply.
No automatic executable download or installation runs in the application.

The landing page preview is captured from the Compass production renderer using
synthetic sample documents. No personal corpus content is included. Regenerate it
with `node scripts/distribution/capture-site-preview.cjs` in the local app workspace.
