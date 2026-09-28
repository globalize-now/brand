# globalize.now — logo kit (F6 · Bubble fan)

## Contents

| Folder | What |
|---|---|
| `svg/symbol/` | Symbol only, main (full) version, one file per color scheme |
| `svg/symbol/{full,medium,small,tiny}/` | Size-optimized symbol variants (see *Sizes*) |
| `svg/lockup-horizontal/` | Symbol + name, side by side. `ui-sizes/` has pre-built 14/18/20/24 px versions with the simpler symbol |
| `svg/lockup-stacked/` | Symbol above name |
| `svg/wordmark/` | Name only |
| `svg/app-icon/` | Rounded and square (full-bleed) app icons, 512 grid |
| `svg/avatar/` | Circular avatars |
| `png/…` | Same assets as transparent PNGs in several sizes (`-h128` = 128 px tall) |
| `png/app-icon/{ink,violet,white}/` | 16–1024 px, `rounded/` and `square/` |
| `png/social/` | 1200×630 Open Graph cards (light, dark, violet) |
| `web/` | Drop-in favicon set: `favicon.ico`, `favicon.svg`, `apple-touch-icon.png`, `icon-192/512.png`, maskable icon, `site.webmanifest` |

All SVG text is converted to outlines, so no font is needed to display them.

## Color schemes

| File suffix | Use on | Symbol source / targets | Name / ".now" |
|---|---|---|---|
| `color-light` | White / light backgrounds | Ink / Violet | Ink / Violet |
| `color-dark` | Black / dark backgrounds | Snow / Violet | Snow / Violet |
| `mono-black` | Single-color print, light | Ink | Ink |
| `mono-white` | Photos, dark or colored backgrounds | White | White |
| `on-violet` | Violet backgrounds | White / Ink | White / Ink |

| Token | Hex |
|---|---|
| Violet | `#8B5CF6` |
| Ink | `#0A0A0A` |
| Snow | `#FAFAFA` |
| White | `#FFFFFF` |

Typeface: **Geist SemiBold (600)**, tracking −0.045em. Web buttons with white text: use `#7C3AED` for AA contrast.

## Sizes

The symbol simplifies as it gets smaller:

| Rendered symbol size | Variant |
|---|---|
| ≥ 40 px | `full` — three lines, all bubble tails |
| 28–39 px | `medium` — target tails removed |
| 20–27 px | `small` — two targets |
| < 20 px | `tiny` — no lines (favicon) |

- Minimum lockup: 14 px type size (use `svg/lockup-horizontal/ui-sizes/`).
- Minimum symbol: 16 px.
- Clear space: keep 0.45 × type size clear on every side of a lockup.

## Web setup

Copy `web/` into your public folder and add:

```html
<link rel="icon" href="/favicon.ico" sizes="48x48">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="/apple-touch-icon.png">
<link rel="manifest" href="/site.webmanifest">
<meta property="og:image" content="/og-dark-1200x630.png">
```

(Copy the OG image you want from `png/social/` next to them.)
