# Install Beaverly Shelf on Linux

Beaverly Shelf runs on **64-bit Linux** (tested target: Ubuntu). You do **not** need to
install .NET — it's bundled. Pick **AppImage** (portable, works everywhere) or the
**`.deb`** (integrates with Ubuntu/Debian and pulls dependencies automatically).

---

## Option A — AppImage (portable, any distro)

1. Download `Beaverly-Shelf-<version>-x86_64.AppImage` from the
   **[Releases page](https://github.com/giindevs/beaverly/releases/latest)**.
2. Make it executable and run it:

   ```bash
   chmod +x Beaverly-Shelf-*-x86_64.AppImage
   ./Beaverly-Shelf-*-x86_64.AppImage
   ```

On a normal Ubuntu **desktop**, that's all. On a **minimal** install (server/WSL/Docker),
install the runtime libraries first:

```bash
sudo apt update && sudo apt install -y \
  libx11-6 libice6 libsm6 libxi6 libxrandr2 libxcursor1 libxext6 libx11-xcb1 \
  libfontconfig1 libgl1 libicu74 libssl3 \
  fonts-dejavu-core fonts-liberation fonts-noto-core fonts-noto-cjk
```

> `fonts-noto-cjk` is what makes the **Japanese/Chinese** interface show real characters
> instead of boxes. Adjust `libicu74` to your release (`libicu70` on Ubuntu 22.04).

---

## Option B — `.deb` (Debian / Ubuntu)

```bash
# from the folder where you downloaded it
sudo apt install ./beaverly-shelf_<version>_amd64.deb
```

`apt` installs the app **and** its dependencies automatically. Then launch **Beaverly
Shelf** from your app menu, or run `beaverly-shelf` in a terminal.

Update: download the newer `.deb` and `sudo apt install ./…` again.
Remove: `sudo apt remove beaverly-shelf`.

---

## Where is my data?

- **Your libraries**: the folders you chose when creating them (each self-contained).
- **App settings**: `~/.shelf`.

## Troubleshooting

- **`error while loading shared libraries: libfontconfig.so.1`** (or `libX11`, `libICU`) —
  install the runtime libraries listed above.
- **Window opens but text is missing / boxes** — install the font packages
  (`fonts-dejavu-core fonts-liberation fonts-noto-core fonts-noto-cjk`).
- **Wayland session** — the app runs through XWayland automatically (installed by default
  on Ubuntu); nothing extra needed.
