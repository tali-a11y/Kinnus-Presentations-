# resources.altruicity.com

Static download gate for ALTRUICITY workshop materials. Currently serves the
Kinus 2026 Magnetic Mission slides and worksheets.

How it works

1. A shliach fills in name and email on `index.html`.
2. The page posts the form to a Zapier workflow webhook (`HOOK_URL` in `index.html`).
3. The page reveals the download buttons. Zapier records the request on the
   monday.com board "Kinus 2026 // Magnetic Mission Downloads", tags the contact
   in Mailchimp if they opted in, and emails them the links from jonah@altruicity.com.

Hosting

- GitHub Pages, deployed by `.github/workflows/pages.yml` on every push.
- Custom domain: `CNAME` holds `resources.altruicity.com`. DNS needs a CNAME
  record `resources` pointing at `tali-a11y.github.io`.

Editing

- The four PDFs live in `files/`. To update one, replace the file and keep the name. The `FILES` list in
  `index.html` holds the labels.
- Fonts are the ALTRUICITY house fonts from the design system (`fonts/`).
