# GLYSK Advisory — advisory.glysk.eu

Static site. Pure HTML/CSS/JS. No build step.

## File Structure

```
/
├── index.html          ← Main site
├── statichost.yml      ← Statichost deploy config (public: .)
├── .gitignore
├── README.md
└── assets/
    └── giuseppe.jpeg   ← Download separately (see below)
```

## Assets

The profile photo needs to be downloaded manually before going live:

```bash
curl -L "https://thegrid.capital/wp-content/uploads/2026/01/GL-Profile-Picture.jpeg" \
     -o assets/giuseppe.jpeg
```

## Deploy via statichost.eu

1. Dashboard → New Site → GitHub → `giuseppelopesme/advisory.glysk.eu`
2. Branch: `main` — the `statichost.yml` handles the rest
3. Add custom domain: `advisory.glysk.eu`

## DNS (Infomaniak)

| Type  | Name     | Value               |
|-------|----------|---------------------|
| CNAME | advisory | sites.statichost.eu |

## Theme

- Light by default
- Auto dark at 19:00, light at 07:00
- Manual toggle saved in `localStorage` as `glysk-theme`

## Contact

hello@glysk.eu
