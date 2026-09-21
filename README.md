# Sandarbh — Releases

Downloads for **Sandarbh**, an offline-first citation manager that works inside
Microsoft Word, LibreOffice Writer, ONLYOFFICE Desktop Editors and WPS Writer.

Free to use. **No warranty, and no liability on the author** — please read
[NO-LIABILITY.md](NO-LIABILITY.md) and the [EULA](EULA.txt) before installing.

This repository carries **binaries only**; the source is not public.

## Download

Get the latest from the [**Releases**](../../releases/latest) page.

| Platform | File | |
|---|---|---|
| Windows 10/11 (64-bit) | `Sandarbh-<version>-Setup.exe` | Installer |
| Linux (x86-64, glibc 2.35+) | `Sandarbh-<version>-x86_64.AppImage` | Portable, no install |

Each file ships with a `.sha256` alongside it. Verify before running:

```bash
sha256sum -c Sandarbh-1.5.0-x86_64.AppImage.sha256
```

```powershell
Get-FileHash .\Sandarbh-1.5.0-Setup.exe -Algorithm SHA256
```

### Running the AppImage

```bash
chmod +x Sandarbh-1.5.0-x86_64.AppImage
./Sandarbh-1.5.0-x86_64.AppImage
```

## What it does

* **Cite while you write** in Word, Writer, ONLYOFFICE and WPS — insert, edit,
  renumber and reformat citations, with a reference list that rebuilds itself.
* **Any CSL style.** APA, IEEE, Vancouver, Nature, Chicago and thousands more,
  with the style's own layout — hanging indent, line and entry spacing —
  applied to the page, or overridden per library.
* **Offline first.** Your library is a local file. Nothing is uploaded, and
  there is no account.
* **Import** from EndNote (RIS, XML, `.enw`, `.enl`), Zotero (RDF, BibTeX,
  CSL-JSON, `zotero.sqlite`), Mendeley, RefWorks and more.
* **Look up by DOI, PubMed ID, ISBN or arXiv ID**, or search Crossref,
  OpenAlex, PubMed and others.
* **PDFs** attached to references — stored or linked — with highlighting and
  sticky notes.
* **`{Author, Year #45}`** temporary citations, converted on demand.

## Editor support

| | Word | LibreOffice | ONLYOFFICE | WPS |
|---|---|---|---|---|
| Windows | ✅ ribbon tab | ✅ menu | ✅ panel | ✅ via the app's menu |
| Linux | — | ✅ menu | ✅ panel | — |

The Word and WPS connectors are Windows-only: they drive the editor through
COM, which does not exist on Linux.

## Requirements

* **Windows** 10 or 11, 64-bit.
* **Linux** x86-64 with glibc 2.35 or newer (Ubuntu 22.04+, Fedora 36+,
  Debian 12+). FUSE is used to mount the AppImage; if it is unavailable, run it
  with `--appimage-extract-and-run`.

## Third-party components

Sandarbh bundles open-source components, including Qt (via PySide6) under the
LGPL v3. Their licences and notices are in
[THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt) and [licenses/](licenses).

## Author

Dr. Shilpam Sharma
