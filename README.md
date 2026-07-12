# FFC-EX-letspiritlead.org

Let Spirit Lead, Inc. — FFC-supported charity website (static, GitHub Pages).

This repository holds a fully localized static capture of the former WordPress site at
`letspiritlead.org`, migrated as part of the FFC Wave-1 WordPress-to-Pages program
([FFC-Cloudflare-Automation#702](https://github.com/FreeForCharity/FFC-Cloudflare-Automation/issues/702)).

## Hosting

- Deployed to GitHub Pages on the default URL:
  <https://freeforcharity.github.io/FFC-EX-letspiritlead.org/>
- Deployment runs from `.github/workflows/static.yml` on every push to `main`.
- No custom domain and no DNS changes are configured at this stage.

## Migration notes

- Captured from the live WordPress 6.8.1 site (Elementor); NitroPack CDN images and Elementor Google Fonts localized; stale freelance dev-host (mdtasnimulrizvi.com) font references neutralized.
- All CSS/JS/fonts/images are served from this repository; Google Fonts and any external
  image hosts were downloaded and localized, and WordPress analytics/tracking beacons were stripped.
- `wp-json`, XML-RPC, oEmbed, RSS feed, and comment artifacts were stripped.
- Non-functional WordPress search/contact forms were neutralized; Cloudflare-obfuscated
  emails were decoded to `mailto:` links; dead internal links/images were pruned.

## CI

- `static.yml` — deploys to Pages on every push to `main`.
- `check-assets.yml` — fails if any asset loads from an external host.
- `linkcheck.yml` — lychee link check (weekly + on push/PR).

---

Supported by [Free For Charity](https://freeforcharity.org).
