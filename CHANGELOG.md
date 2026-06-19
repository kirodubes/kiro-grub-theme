# Changelog

## 2026.06.19

### White monochrome Restart and Shutdown boot-menu icons
- Replaced the colour `icons/restart.png` (blue) and `icons/shutdown.png` (red)
  with flat white glyphs — circular-arrow for Restart, power symbol for Shutdown.
- **Why:** the colour circles clashed with the otherwise restrained boot menu;
  plain white reads cleaner on the dark background.
- **Source:** rendered at 32×32 (the theme's `icon_width`) from the **Surfn/32**
  action icons via `rsvg-convert` — `system-reboot.svg` as-is (white), and
  `system-shutdown.svg` with its red circle stripped so only the white power
  glyph remains. Both taken from the same Surfn/32 set so the ring stroke matches
  (measured 4 px wall on each); transparent background.

### Files Modified
- `boot/grub/themes/kiro/icons/restart.png`
- `boot/grub/themes/kiro/icons/shutdown.png`

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
