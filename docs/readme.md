COpyright is for uagent.app only

[https://](https://uagent.app/)





# U Agent Website Docs

This folder contains the static website pages for **U Agent**.

U Agent is positioned as an **AI Sales Execution System** that turns customer conversations into timely, personalized, human-approved sales follow-up actions.

## Files

- `index.html`  
  Main landing page for `uagent.app`.

- `privacy.html`  
  Privacy Policy page.

- `terms.html`  
  Terms of Service page.

- `support.html`  
  Support page for customer help, billing questions, bug reports, and general inquiries.

- `assets/icon.png`  
  Website favicon, Apple touch icon, and social preview image.

- `assets/splash.png`  
  Brand watermark / visual asset used inside the landing page.

## Brand Positioning

Primary brand name:

```text
U Agent
```

Primary product category:

```text
AI Sales Execution System
```

Main landing page headline:

```text
Sales
Claude Monet 1.0
```

Core positioning:

```text
U Agent helps sales professionals, founders, consultants, and growth teams turn customer conversations into clear, reviewable, and executable follow-up actions.
```

## Design Rules

Do not change the shared header or footer unless the change is intentional across all pages.

The website should avoid overly technical or debug-style UI symbols in customer-facing copy, including:

```text
//
[ ]
_
extra dots
terminal-style decorative marks
```

The design direction should stay:

```text
minimal
premium
commercial
brand-forward
clear for customers and investors
```

## Footer Links

All public pages should include footer navigation to:

```text
Terms of Service
Privacy Policy
Support
```

Each page should highlight its current page link when appropriate.

## Favicon and Social Preview

Every public page should include favicon links in the `<head>` section:

```html
<link rel="icon" href="assets/icon.png?v=2" type="image/png">
<link rel="apple-touch-icon" href="assets/icon.png?v=2">
```

The main landing page should use `assets/icon.png` for Open Graph and Twitter preview images:

```html
<meta property="og:image" content="https://uagent.app/assets/icon.png">
<meta name="twitter:image" content="https://uagent.app/assets/icon.png">
```

## SEO Notes

The main landing page title should remain:

```text
U Agent | AI Sales Execution System
```

The main landing page description should emphasize:

```text
human-approved sales follow-up actions
customer conversations
revenue execution
Gmail-connected workflow
```

After deployment, verify the live site with:

```bash
curl -L https://uagent.app | grep -E "Claude Monet|Revenue orchestration|og:image|twitter:image|icon.png|splash.png"
```

Verify the favicon file is live with:

```bash
curl -I https://uagent.app/assets/icon.png
```

Expected result:

```text
HTTP/2 200
content-type: image/png
```

## Deployment Checklist

Before publishing changes:

1. Confirm `index.html`, `privacy.html`, `terms.html`, and `support.html` render correctly locally.
2. Confirm all footer links work.
3. Confirm favicon appears in the browser tab.
4. Confirm `assets/icon.png` is deployed and reachable online.
5. Confirm `https://uagent.app` returns the latest HTML.
6. Request re-indexing in Google Search Console after SEO changes.

## Important Notes

Local file paths such as:

```text
/Users/yueli/Desktop/u-agentic-ai/your-ai-agent-clean/docs/assets/icon.png
```

must never be used inside deployed HTML.

Use web-relative paths instead:

```text
assets/icon.png
```

or absolute public URLs when required for SEO/social preview:

```text
https://uagent.app/assets/icon.png
```
