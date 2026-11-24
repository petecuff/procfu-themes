# procfu-themes

Shared stylesheets and images for ProcFu App Builder portals, served by GitHub Pages at
`https://assets.futuresolutionsonline.co.uk/`.

## Hosting

- Custom domain set by the `CNAME` file in this repo (24/11/2026).
- DNS: Cloudflare, CNAME `assets` -> `petecuff.github.io`, DNS only (grey cloud). Do not proxy it, or GitHub cannot renew the HTTPS certificate.
- Why: school web filters block `*.github.io` ("Security - Domain Sharing"), so the portals lost their styling in schools.
- Do not link to `petecuff.github.io/procfu-themes/...`. It now redirects to the custom domain over http, which browsers block on https portals.

## Maths Camps

`maths-camps/theme.css` is the brand theme for the Maths Camps school portals (ProcFu apps 11975 mathsschool, 11976 mathsparent, 11979 mathstrust).

Each app's **Page Wrapper** (Configuration > Page Wrapper) links it like this. Leave **HTML Header** empty.

```html
<link rel="stylesheet" href="https://assets.futuresolutionsonline.co.uk/maths-camps/theme.css?v=1.0.16">
```

The logo in the Logged In and Logged Out headers is
`https://assets.futuresolutionsonline.co.uk/maths-camps/img/logo-header.png`.

### Releasing a change

1. Commit the change to `main`. GitHub Pages deploys it in about a minute.
2. Bump the `?v=` number in each app's Page Wrapper so browsers fetch the new file.

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
