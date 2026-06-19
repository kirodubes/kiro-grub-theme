# CLAUDE.md

## What this is

Content repo for **`kiro-grub-theme`** — the Kiro-branded GRUB2 boot theme.
Published to GitHub as `kirodubes/kiro-grub-theme`; the PKGBUILD in
`~/KIRO-PKG-BUILD-APPS/kiro-grub-theme/` clones this via `git+` source and builds
the package into `nemesis_repo`.

## Layout

- `boot/grub/themes/kiro/` mirrors the install path. Contains `theme.txt`,
  `background.jpg`, `info.png`, `select_*.png`, `*.pf2` fonts and `icons/`.
- The theme is a rebrand of [vinceliuice/grub2-themes](https://github.com/vinceliuice/grub2-themes)
  (GPL-3.0). Icons, selection pixmaps and fonts come from there; the background,
  wordmark and `icons/kiro.png` are Kiro artwork.

## Editing

- Boot-menu icons match each GRUB `menuentry --class <name>` to `icons/<name>.png`.
- Font names referenced in `theme.txt` must match the `.pf2` internal names
  (`Unifont Regular 16`, `Terminus Regular 16`).
- After editing, rebuild via `~/KIRO-PKG-BUILD-APPS/kiro-grub-theme/build.sh` and
  re-test by booting a rebuilt ISO in a VM — GRUB themes only fully validate at
  boot.

## Push

`./setup.sh` (first time, sets the `git@github.com-kiro:kirodubes/...` remote)
then `./up.sh` to commit + push.
