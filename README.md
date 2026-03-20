<h1 align="center"> X Repo</h1>

<p align="center">
  <strong>A minimalistic Linux distribution based on Arch</strong>
</p>

<p align="center">
  <a href="https://dev.xscriptor.com/x">Website</a> •
  <a href="https://dev.xscriptor.com/x/docs">Documentation</a> •
  <a href="https://dev.xscriptor.com/x/download">Download</a>
</p>

---

## About this Repository

This repository has two main purposes:

1. **X Linux Website** — The official website built with Next.js
2. **System Packages** — Configuration and branding files for the X Linux filesystem

---

## Website

The X Linux website is built with modern technologies:

- **Next.js 16** — React Framework with App Router
- **Tailwind CSS 4** — Utility-first CSS
- **Framer Motion** — Smooth animations
- **Three.js / React Three Fiber** — 3D Graphics
- **next-themes** — Light/Dark mode support

### Site Structure

```
app/
├── page.tsx          # Home page (Hero)
├── download/         # Download page
├── docs/             # Documentation
├── developers/       # Developer information
└── contact/          # Contact
```

---

## System Packages

The `packages/` directory contains the X Linux filesystem packages:

### x-release

System identity and branding package. Includes:

- **`/usr/share/x-release/os-release`** — X Linux identity template
- **`/usr/share/x-release/grub`** — GRUB defaults template
- **`/usr/share/pixmaps/x.svg`** — Distributor logo
- **`/usr/bin/x-release-apply`** — Applies branding to the running system

#### Package Installation

```bash
cd packages/x-release
xpkg build
xpm install ./out/x-release-1.0-4-any.xp

# Apply system branding (os-release, GRUB/systemd-boot updates)
sudo x-release-apply
```

`PKGBUILD` is kept for legacy Arch tooling, but `XBUILD` is the native path
for `xpkg` and `xpm`.

### Create Package Repository

The `build-repo.sh` script generates a pacman-compatible package repository:

```bash
cd packages
./build-repo.sh
```

This will create the repository structure in `packages/repo/x86_64/` with:
- Compiled `.pkg.tar.zst` files
- Repository database (`x.db.tar.gz`)



---

## Technologies

| Component | Technology |
|-----------|------------|
| Website | Next.js, React, TypeScript |
| Styles | Tailwind CSS, Framer Motion |
| 3D | Three.js, React Three Fiber |
| System | Arch Linux, pacman |
| Packaging | makepkg, PKGBUILD |

---

## License

This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](LICENSE) file for more details.
