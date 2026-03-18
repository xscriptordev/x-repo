# Changelog

All notable changes to the x-repo project will be documented in this file.

## [Unreleased]

### Added
- **xpm**: Added `xpm-0.1.0-1-x86_64.xp` package to `packages/xpm/`.

### Changed
- **Repository DB**: Updated `public/repo/x86_64/x.db.tar.gz` and `x.db` to include `xpm` metadata entry.
- **Repository Artifacts**: Added `public/repo/x86_64/xpm-0.1.0-1-x86_64.xp` for direct standard installation from repo server path.

## [2026-02-01]
### Added
- **xtop**: Added `xtop-git` package to `packages/xtop/`.
- **xfetch**: Added `xfetch-git` package to `packages/xfetch/`.
- **CI**: Updated `build.yml` workflow to automatically find and index `.pkg.tar.zst` files from all subdirectories in `packages/`.
- **Docs**: Added `ROADMAP.md` and `CHANGELOG.md`.
