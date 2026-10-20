# Mazin & Tibyan wedding invitation

Single-page Arabic (RTL) invitation for Friday 30 October 2026, City Mark Resort (Kempinski Hall), Al Haram, Giza.

## Files
| File | Purpose |
|---|---|
| `index.html` | The invitation |
| `og-image.png` | WhatsApp / social link preview (1200x630) |
| `favicon.ico`, `favicon-32.png`, `favicon-192.png`, `apple-touch-icon.png` | Icons |
| `music.mp3` | Optional. Add any track under ~2 MB; the music button appears only when this file exists |

## Before going live
1. Replace `SITE_DOMAIN` (4 places in `index.html`) with the final domain, e.g. `mazin-tibyan.com`.
2. Add a file named `CNAME` containing just the domain.

## Settings (top of the script in `index.html`)
```js
var WEDDING     = new Date("2026-10-30T20:00:00+02:00"); // start, Cairo time
var WEDDING_END = new Date("2026-10-31T01:00:00+02:00"); // end
var TIME_TEXT   = "من الساعة 8:00 مساءً";
var TIME_PILL   = "8:00 م ← 1:00 ص";
```
Egypt leaves summer time at midnight on 30 Oct 2026, so the wedding night is UTC+02:00, not +03:00.

## GitHub Pages
1. New **public** repo, upload all files, Settings → Pages → Deploy from branch `main` / root.
2. Domain DNS (GoDaddy): A records `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`; CNAME `www` → `<github-user>.github.io`.
3. Settings → Pages → Custom domain → enter the domain, wait for the certificate, tick **Enforce HTTPS**.

## Personal guest links
`https://<domain>/?guest=اسم%20الضيف` greets the guest by name on the envelope and header.
