# RumboRide Technologies LLC

A responsive corporate website built with plain HTML, CSS, and JavaScript. No build step, package dependencies, backend, external fonts, or analytics are required.

## Files

- `index.html`: Home, Services, Products, About Us, and Contact sections.
- `privacy.html` and `terms.html`: dedicated website policy pages.
- `assets/css/styles.css`: shared responsive styling.
- `assets/js/main.js`: accessible mobile menu, email copying, and footer year.
- `assets/images/`: placeholder brand favicon and Open Graph artwork.
- `CNAME`: custom domain `rumboride.com`.
- `robots.txt` and `sitemap.xml`: crawler discovery.
- `.nojekyll`: serves the site as static files without Jekyll processing.

## Preview locally

From the repository root run:

```sh
python3 -m http.server 8000
```

Visit `http://localhost:8000`. Use a local server rather than opening HTML directly: asset and navigation paths intentionally start at `/` for the custom domain root.

## Deploy on GitHub Pages

1. Push these files to the root of your repository's deployment branch (for example, `main`).
2. In the repository's **Settings → Pages**, select **Deploy from a branch**, then your deployment branch and **/(root)**. Save.
3. Set **Custom domain** to `rumboride.com`. The committed `CNAME` preserves this setting.
4. At your DNS provider, configure the apex domain using the records in GitHub's [custom domain instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site). Remove conflicting records. If you also want `www.rumboride.com`, configure its CNAME as described there.
5. After DNS verification and certificate provisioning, enable **Enforce HTTPS** in Pages settings.
6. Visit `https://rumboride.com/` and check the navigation, both legal pages, email links, and mobile menu.

All paths and canonical URLs are configured for `https://rumboride.com/`. A repository subpath such as `username.github.io/repository/` is not the intended deployment URL. To use a different domain, update `CNAME`, canonical and social metadata, `robots.txt`, and `sitemap.xml`.

## Content and maintenance

Contact links open an email application addressed to `admin@rumboride.com`; no form submission or message delivery is simulated. Copying the email uses the Clipboard API, with a readable fallback when unavailable.

The current `r.` mark is a brand placeholder. Replace it and the favicon with the approved company logo. The product panels explicitly label screenshot placeholders; replace them with real optimized images and descriptive alternative text. There are no claims about product release status, app-store availability, customer results, certifications, or clients.

The Privacy Policy and Terms describe this static corporate website. The company should review them against its actual hosting, email, data retention, and business practices before publication. Product-specific policies must be supplied separately when products launch. If analytics, cookies, forms, or other data collection are added, update the policy accordingly.

Open Graph metadata uses a local 1200 × 630 PNG social preview. Its editable SVG source is also included. Replace the artwork with approved branding as needed, keeping the metadata image URL in sync.

Accessibility includes semantic landmarks, a skip link, labeled navigation, visible keyboard focus, reduced-motion support, descriptive link text, a keyboard-operable mobile menu with Escape support, and live copy feedback. Navigation also remains available without JavaScript.
