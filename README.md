# procfu-themes

Shared stylesheets for ProcFu App Builder portals, served through jsDelivr.

## Maths Camps

`maths-camps/theme.css` is the brand theme for the Maths Camps school portals.

Paste this into each app's **Page Wrapper** (Configuration > Page Wrapper). Leave **HTML Header** empty.

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500;600;700&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&family=Work+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/petecuff/procfu-themes@COMMIT/maths-camps/theme.css">
<style>
/* App-specific overrides go here */
</style>
```

### Versioning

Each app links to a fixed commit (`@<sha>`), so a change reaches an app only when that app's link is updated. To release a change:

1. Commit the change to `main`.
2. Replace the commit SHA in each app's Page Wrapper with the new one.

For a link that follows `main` instead, use `@main` and purge the cache after each push: `https://purge.jsdelivr.net/gh/petecuff/procfu-themes@main/maths-camps/theme.css`.

### Utility classes

For screen headers and footers (use these instead of inline styles, which ProcFu's markdown parser can break):

- `mc-hero`: dark hero band
- `mc-band`: yellow call-to-action band
- `mc-panel`: cream panel with a dark top rule
- `mc-callout`: callout with a yellow left bar (`is-info`, `is-error`, `is-success`)
- `mc-btn`: link styled as a button (`is-dark`, `is-outline`)
- `mc-eyebrow`: small uppercase label (`is-yellow`)
- `mc-stats`, `mc-stat`, `mc-stat-value`, `mc-stat-label`: big-number stats
- `mc-pill`: status pill (`is-yellow`, `is-ink`, `is-green`, `is-red`, `is-plum`)
- `mc-hl`: yellow highlighter behind text
- `mc-nav`, `mc-logo`, `mc-nav-links`, `mc-nav-cta`: nav bar in the Logged In / Logged Out Header
- `mc-footer`, `mc-footer-grid`: black footer for the HTML Footer
- Add `mc-login` to `body` (from the login screen's header script) for the card-style login page.
