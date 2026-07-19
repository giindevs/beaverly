<p align="center">
  <img src="assets/mascot.png" alt="Beaverly" width="140">
</p>

<h1 align="center">Beaverly Shelf</h1>

<p align="center">
  <b>Your books, your shelf — 100% on your computer.</b><br>
  A calm, local-first desktop app to organize your e-book library and read
  <b>PDF, EPUB and CBZ</b> with highlights and notes. No account required.
</p>

<p align="center">
  <a href="https://github.com/giindevs/beaverly/releases/latest"><img src="https://img.shields.io/github/v/release/giindevs/beaverly?label=version&color=C0602F" alt="Release"></a>
  <a href="https://github.com/giindevs/beaverly/releases"><img src="https://img.shields.io/github/downloads/giindevs/beaverly/total?color=6C6F43" alt="Downloads"></a>
  <img src="https://img.shields.io/badge/Windows-x64-0078D6?logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/Linux-x64-1793D1?logo=linux&logoColor=white" alt="Linux">
  <img src="https://img.shields.io/badge/offline--first-privacy-2E7D32" alt="Offline-first">
  <a href="https://github.com/giindevs/beaverly/stargazers"><img src="https://img.shields.io/github/stars/giindevs/beaverly?style=flat&color=EAB308" alt="Stars"></a>
</p>

<p align="center">
  <b>English</b> · <a href="README.pt-BR.md">Português&nbsp;(BR)</a>
</p>

---

## ⬇️ Download

Get the latest build from the **[Releases page »](https://github.com/giindevs/beaverly/releases/latest)**

| Platform | File | Notes |
| --- | --- | --- |
| **Windows 10/11 (x64)** | `beaverly-shelf-setup-<version>.exe` | Installer — no admin needed, no .NET required |
| **Linux — AppImage** | `Beaverly-Shelf-<version>-x86_64.AppImage` | Portable — `chmod +x` and run |
| **Linux — Debian/Ubuntu** | `beaverly-shelf_<version>_amd64.deb` | `sudo apt install ./beaverly-shelf_*.deb` |

> **First run on Windows:** because the installer isn't code-signed yet, Windows
> SmartScreen shows *"Windows protected your PC"*. Click **More info → Run anyway**.
> This is expected for new indie apps and is not a virus warning.

Full step-by-step: **[Install on Windows »](docs/install-windows.md)** ·
**[Install on Linux »](docs/install-linux.md)**

🛒 *Coming soon:* Microsoft Store and Ubuntu (Snap) Store — see the [roadmap](#-roadmap).

---

## ✨ Features

- 📚 **Local library** — import your e-books (files or folders), organize by author,
  series, tags and collections. Everything lives on your machine.
- 📖 **Built-in reader** — read **PDF, EPUB and CBZ** with a clean reading mode,
  table of contents, text selection and a browser-style selection toolbar
  (copy · highlight · note · search the web).
- ✍️ **Highlights & notes** — annotate as you read. Your original files are
  **never modified** (read-only, always).
- 🖼️ **Covers & metadata (opt-in)** — optionally fetch covers, synopses and author
  info online. Only the search text is sent — never your files — and you confirm
  before anything is saved.
- 🔌 **Add-ons** — extend the catalog with Stremio-style add-ons (URL-installed
  services; no code runs inside the app).
- 💾 **Backups** — back up your library to a folder you choose (e.g. a OneDrive or
  Google Drive synced folder). The app never uploads anything by itself.
- 🌍 **8 languages** — Portuguese, English, Spanish, French, German, Italian,
  Japanese, Chinese. First-run picks your language automatically.
- 🦫 **Yours, offline** — works fully offline, no sign-up, no telemetry.

---

## 🔒 Privacy — offline-first by design

Beaverly Shelf runs **100% offline and without an account**. Your library, imports,
reading, annotations and backups are all local. The only things that ever touch the
network are **things you explicitly click** — an optional online cover/metadata
lookup (which sends only the title/author/ISBN you searched, never your files), or
the reader's "search the web" button. Nothing is sent automatically, there's no
telemetry, and a Beaverly account is **optional**, never required.

📄 Read the full **[Privacy Policy »](PRIVACY.md)**

---

## 🧩 The Beaverly ecosystem

Beaverly Shelf is the desktop piece of a wider reading ecosystem. Explore the rest at
**[beaverly.com.br »](https://beaverly.com.br)**

| App | What it is | Where |
| --- | --- | --- |
| 🌐 **Beaverly** | The reading social platform — catalog, virtual shelves, reading progress, reviews, goals, clubs. | [beaverly.com.br](https://beaverly.com.br) |
| 🖥️ **Beaverly Shelf** | This app — desktop library manager + reader for Windows & Linux. | *You are here* |
| 🧭 **Beaverly Companion** | Browser extension to save books and highlights while you browse. | Chrome · Edge · Firefox |
| 🗣️ **Beaverly Voice** | Ask Beaverly on Alexa & Google Assistant. | [voice.beaverly.com.br](https://voice.beaverly.com.br) |
| 📱 **Beaverly for Android** | Read and track your books on the go. | *(coming to Google Play)* |

> ℹ️ Links and store availability are listed on **[beaverly.com.br](https://beaverly.com.br)** — the single source of truth.

---

| Library | Reader |
| --- | --- |
| ![Library](docs/screenshots/library.png) | ![Reader](docs/screenshots/reader.png) |

| Book details | First-run |
| --- | --- |
| ![Details](docs/screenshots/detail.png) | ![Onboarding](docs/screenshots/onboarding.png) |

*(If the images above are blank, they haven't been added yet — see
[docs/screenshots/](docs/screenshots/).)*

---

## 🗺️ Roadmap

- [x] Windows installer (`.exe`)
- [x] Linux packages (AppImage + `.deb`)
- [x] 8-language interface
- [ ] **Microsoft Store** listing (MSIX) — [publishing guide](docs/publishing-stores.md)
- [ ] **Ubuntu / Snap Store** listing (snap) — [publishing guide](docs/publishing-stores.md)
- [ ] Code-signed installers (removes the SmartScreen warning)
- [ ] macOS build

---

## 💬 Feedback & issues

Found a bug or have an idea? **[Open an issue »](https://github.com/giindevs/beaverly/issues/new)**
— please include your OS, the app version, and steps to reproduce.

You can also send feedback right inside the app (**"Fale conosco" / Contact us**).

---

## ❓ FAQ

**Do I need to create an account?**
No. Beaverly Shelf works fully offline; the account is optional.

**Does it upload my books anywhere?**
No. Files stay on your machine. Only optional, click-initiated online lookups send a
search term (title/author/ISBN) — never your files.

**Is it free?**
Yes — the app is free to download and use.

**Windows says the file is unsafe. Is it a virus?**
No. The installer just isn't code-signed yet, so SmartScreen warns on first run.
Click *More info → Run anyway*. Code-signing is on the roadmap.

**Where is my data stored?**
Your libraries are self-contained folders you choose. App settings live under
`~/.shelf` (or `%USERPROFILE%\.shelf` on Windows).

---

## 📝 License

Beaverly Shelf is proprietary software, free to download and use.
© Beaverly. All rights reserved. The brand, mascot and app are property of Beaverly.

---

<p align="center"><sub>Made with 🦫 by the Beaverly team.</sub></p>
