# Changelog

## 2026.06.19

### What Changed
- Initial release of the Kiro-branded GRUB2 boot theme.
- Dark 1920×1080 background with the centred Kiro logo + KIRO wordmark.
- Full colour OS icon set for boot-menu entries plus a custom `kiro.png` for
  Kiro install entries.

### Technical Details
- Forked the icon set, selection pixmaps and Terminus/Unifont `.pf2` fonts from
  [vinceliuice/grub2-themes](https://github.com/vinceliuice/grub2-themes)
  (GPL-3.0); rebranded the background and `theme.txt`.
- Installs to `/boot/grub/themes/kiro/` so the theme is readable by GRUB even on
  a LUKS-encrypted root (BIOS installs).

### Files Modified
- `boot/grub/themes/kiro/theme.txt`
- `boot/grub/themes/kiro/background.jpg`
- `boot/grub/themes/kiro/icons/*` (incl. `kiro.png`)
- `boot/grub/themes/kiro/select_*.png`, `info.png`, `*.pf2`
- `LICENSE`, `README.md`
