# QIX

A self-contained HTML5 reconstruction of the 1981 Taito America arcade game **Qix** (pronounced “kicks”), built for [deepbreath.space](https://deepbreath.space).

Fan reconstruction — not affiliated with Taito. Original geometry, rules, and scoring; no ROM data, cabinet art, or sampled sound.

Play it by opening [`index.html`](index.html) in a browser, or embed it:

```html
<iframe src="/qix/index.html" width="100%" height="720" style="border:0;max-width:960px;" allow="fullscreen" title="Qix"></iframe>
```

## Controls

| Action | Keys / input |
| --- | --- |
| Move | Arrows or WASD · on-screen pad |
| Fast Draw | Z, left-click, or **FAST** |
| Slow Draw | X, right-click, or **SLOW** |
| Pause | P, Esc, or Pause |
| Start | Enter |
| Mute | M |

## Rules (factory Qix)

- Claim empty space by drawing a Stix from the border back to the border. The side **without** the Qix fills.
- Reach **75%** to clear a level. Slow fill scores double; Fast fill is quicker.
- From level 3, two Qixes appear. Splitting them into separate empty regions also clears the level and raises the multiplier (max ×9).
- Sparx patrol the **live edge** of unclaimed space only. Buried Stix inside filled land are not roads. Super Sparx can run up an open line.
- Stand still on an open line and a Fuse burns it. The Qix kills you if it touches that line.
- Extra lives at 50,000 and 150,000. High scores stay in `localStorage` (top 8).

## Skins

Switch from the title screen or pause menu:

- **Coffee Current** (default) — espresso field, cream borders, latte Fast / amber Slow
- **Classic** — black field, cyan Fast, orange-red Slow
- **Neon** — violet field, electric-blue Fast, magenta Slow

## Technical

Single file: vanilla JavaScript, Canvas 2D, Web Audio. No frameworks, no CDN, no build step. Works as a static file and inside an iframe.
