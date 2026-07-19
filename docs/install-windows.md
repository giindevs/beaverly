# Install Beaverly Shelf on Windows

Beaverly Shelf runs on **Windows 10 and 11 (64-bit)**. You do **not** need to install
.NET or anything else — everything is bundled.

## 1. Download

Go to the **[Releases page](https://github.com/giindevs/beaverly/releases/latest)** and
download:

```
beaverly-shelf-setup-<version>.exe
```

(about 37 MB).

## 2. Run the installer

Double-click the file.

> **"Windows protected your PC"** may appear (blue window). This is **SmartScreen**,
> shown because the app isn't code-signed yet — it is **not** a virus warning.
> Click **More info**, then **Run anyway**.

The installer is **per-user**: it does **not** ask for administrator rights.

## 3. Choose options

- It installs to your user profile by default.
- A **Start Menu** shortcut is always created.
- Tick **"Create a desktop shortcut"** if you want one.
- Leave **"Launch Beaverly Shelf"** ticked to open it right after install.

That's it — Beaverly Shelf opens and walks you through a short first-run screen
(language + how it works). No account needed.

## Updating

Download the newer `beaverly-shelf-setup-<version>.exe` and run it — it upgrades in
place and keeps your libraries and settings.

## Uninstalling

Open **Settings → Apps → Installed apps**, find **Beaverly Shelf**, and choose
**Uninstall**. Your library folders are **not** deleted (they live wherever you chose
to create them); only the app is removed.

## Where is my data?

- **Your libraries**: the folders you picked when creating them (each is self-contained).
- **App settings**: `%USERPROFILE%\.shelf` (e.g. `C:\Users\you\.shelf`).

## Troubleshooting

- **The window doesn't open / nothing happens** — make sure you're on 64-bit Windows 10/11.
  Try running from a terminal to see any message: `"%LOCALAPPDATA%\Programs\Beaverly Shelf\Beaverly.Shelf.Desktop.exe"`.
- **Antivirus flagged it** — unsigned indie apps are sometimes flagged by heuristics.
  You can verify the download came from this Releases page. Code-signing is on the roadmap.
