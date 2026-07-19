# Publishing Beaverly Shelf to the stores

The plan for listing Beaverly Shelf on the **Microsoft Store** (Windows) and the
**Snap Store** (Ubuntu). Both need a developer account and some one-time setup that
only the account owner can do; the packaging work can be prepared in advance.

> Today's downloads (the `.exe` / AppImage / `.deb` on the Releases page) already work
> for everyone. The stores add discoverability, trust badges, and auto-updates.

---

## 🪟 Microsoft Store (Windows)

You have two routes. Start with **Route A** — it's dramatically simpler and reuses the
installer you already ship.

### Route A — list the existing installer ("EXE/MSI app")

The Microsoft Store now accepts traditional Win32 installers directly.

1. Create a **[Microsoft Partner Center](https://partner.microsoft.com/dashboard)**
   developer account (individual, **~US$19 one-time**).
2. In Partner Center → **Apps and games → New product → EXE or MSI app**.
3. Reserve the name **Beaverly Shelf**.
4. Provide the **installer URL** — point it at the GitHub Release asset
   (`beaverly-shelf-setup-<version>.exe`) or a URL on beaverly.com.br.
5. Fill the listing: description, **screenshots** (1366×768+), **category** (Productivity),
   **age rating** (IARC questionnaire), and a **privacy policy URL**
   (a page on beaverly.com.br — the app is offline-first, so it's short).
6. For the trust/verification step, the Store strongly prefers a **code-signed**
   installer (see below). Submit for certification.

**Code signing** removes the SmartScreen warning *and* smooths Store certification. It
needs an **Authenticode certificate** (OV ~US$100–200/yr, or EV for instant reputation)
from a CA (Sectigo, DigiCert…). Then sign both the app `.exe` and the setup:
`signtool sign /fd sha256 /tr http://timestamp.digicert.com /td sha256 setup.exe`.
Inno Setup can sign automatically via its `SignTool` directive.

### Route B — MSIX (full Store integration, auto-update)

For the best Store experience (clean install/uninstall, auto-update, no SmartScreen):

1. Package the self-contained publish as **MSIX**. Easiest options:
   - the **MSIX Packaging Tool** (from the Store), pointed at the existing installer; or
   - a **Windows Application Packaging Project** in the solution wrapping the published `.exe`.
2. Author the **AppxManifest** (identity, display name, logos from `assets/`, capabilities —
   this app needs only `runFullTrust`).
3. Test-install the `.msix` locally, then submit the **MSIX** in Partner Center
   (**New product → MSIX/PWA app**). The Store signs it for you on submission.

**Recommendation:** ship **Route A** first (fast), move to **Route B/MSIX** once there's
demand for auto-update.

---

## 🐧 Snap Store (Ubuntu)

Free. Snaps auto-update and appear in **Ubuntu Software / App Center**.

1. Create a free **[Snapcraft developer account](https://snapcraft.io/)** (Ubuntu One).
2. Install tooling on a Linux box: `sudo snap install snapcraft --classic` (+ LXD).
3. Add a `snap/snapcraft.yaml` (starter below), building from the same self-contained
   `linux-x64` publish this project already produces.
4. Build: `snapcraft`. Test locally: `sudo snap install ./beaverly-shelf_*.snap --dangerous`.
5. Register the name and publish:
   ```bash
   snapcraft register beaverly-shelf
   snapcraft upload beaverly-shelf_*.snap --release=stable
   ```

### Starter `snapcraft.yaml`

```yaml
name: beaverly-shelf
base: core22
version: '0.1.0'
summary: Local e-book library manager and reader
description: |
  Organize your e-book library and read PDF, EPUB and CBZ with highlights and notes.
  Works 100% offline; no account required.
grade: stable
confinement: strict
compression: lzo

apps:
  beaverly-shelf:
    command: bin/Beaverly.Shelf.Desktop
    extensions: [gnome]          # brings X11/Wayland + fonts + GL runtime
    plugs:
      - home                     # read your e-book folders
      - removable-media          # send to USB e-readers
      - network                  # optional online cover/metadata lookup
      - opengl

parts:
  beaverly-shelf:
    plugin: dump
    # Publish first:  dotnet publish apps/Beaverly.Shelf.Desktop -c Release \
    #                   -p:PublishProfile=linux-x64 -o publish
    source: publish/
    organize:
      Beaverly.Shelf.Desktop: bin/Beaverly.Shelf.Desktop
    stage-packages:
      - libfontconfig1
      - libicu70
```

> The `gnome` extension supplies fontconfig, fonts, and the GL/X11/Wayland runtime, so a
> snap is often the **most reliable** way to run the app on any Ubuntu without the user
> installing `apt` dependencies. Verify fonts (incl. CJK) render inside the confined snap.

---

## What each step needs from you (the owner)

| Step | Only you can do | I can prepare |
| --- | --- | --- |
| Partner Center / Snapcraft accounts | ✅ create + verify | — |
| Code-signing certificate | ✅ buy (paid) | wire signing into the build |
| Store listing text, screenshots, privacy URL | ✅ approve | draft it |
| MSIX manifest / packaging project | — | ✅ build |
| `snapcraft.yaml` + snap build | — | ✅ build (needs a Linux box to compile) |

When you're ready, say the word and we'll do them one at a time.
