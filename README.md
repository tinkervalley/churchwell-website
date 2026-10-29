# Churchwell public website

Buildless HTML/CSS/JavaScript, published to `tinkervalley/churchwell-website` using branch-based GitHub Pages (`main`, `/`). No GitHub Actions workflow is required or enabled by this source.

- Website: https://churchwell.ca
- App: https://app.churchwell.ca
- Privacy: https://churchwell.ca/privacy
- Support: https://churchwell.ca/support
- Contact/invites: hello@churchwell.ca

Both website and app domains returned HTTPS 200 on October 21, 2026. The website's sign-in links now use the verified app domain. This does not remove the old app domain or rewrite existing public-form links.

Before previewing or publishing, run `node scripts/prepare-site.mjs` from the application repository. It generates content-hashed CSS/JS filenames and updates all three pages. Keep prior generated files so cached HTML continues to find its matching assets; publish the entire `site/` directory together. This avoids Cloudflare/browser caches pairing new HTML with an older stylesheet. Edit `style.css` and `site.js`, not generated copies.

Preview: `python3 -m http.server 5174 --directory site` from the application repository. The support/privacy paths are directories with index files so direct links work on GitHub Pages.

## Screenshots and typography

The October 29 code-first Around the table redesign uses current actual sample-data web Groups, People and Chats captures and native Home, Groups and People screens. Staff & pastors appears before My family. The kiosk and label captures remain the authentic October 24 examples. Responsive WebP exports preserve the interface content; original PNG sources remain available. The source/export manifest is `docs/landing-page-fixes/2026-10-29/assets.json` in the private application repository.

Fonts are locally hosted Figtree and Libre Caslon, with OFL licenses alongside. The social preview is a browser-rendered composition of real product screens; its source is `design-assets/marketing/social-preview.html` in the private repository. It contains no generated application UI.

## Pricing and copy

Planned starting price: CAD $40/month after beta; invited churches test free. No website billing or automatic conversion is implemented. Dedicated branded apps are arranged separately. The page focuses on Churchwell’s own features rather than competitor comparisons. iOS and Android apps, group and direct chats, Android kiosk check-in, optional Bluetooth thermal labels, and YouTube/podcast media are the main product stories.

App Store copy and remaining submission requirements are in `docs/app-store/` in the private application repository. Do not publish private credentials, source files outside `site/`, or review-account secrets to this public repository.

## Visual verification — October 21, 2026

The live audit found newer HTML paired with a cached, older stylesheet. The old stylesheet had no rules for the screenshot wrappers: at a 1280px viewport the page overflowed to 1894px, with a hero over 3800px tall. Content-hashed asset URLs now keep each page paired with its own CSS/JS version, including privacy and support pages.

Reviewed the hero, feature explorer, app showcase, pricing, support and privacy layouts. Checked page/header width at 320, 375, 390, 768, 900, 1024, 1280 and 1440px; no horizontal overflow. Mobile navigation supports links, Escape dismissal and focus return. Feature tabs retain keyboard navigation. Animations enhance visible content instead of hiding it until a script runs. Static asset references, fingerprints and JavaScript syntax are validated before publication.

## Kiosk and printer compatibility

The Android kiosk screenshot and sample label were produced by the isolated synthetic kiosk test build on October 24, 2026. They contain sample data only. The MUNBYN ITPP130B is listed as confirmed over Bluetooth LE based on physical printing tests; other Bluetooth thermal printers require compatibility verification. Designs are available for 4 × 6 in and 2.25 × 1.25 in stock. This is not a claim that every Bluetooth printer or paper size has been physically tested.

The Chats screenshot was captured from the sample-data web app on October 24, 2026. The media feature illustration is an editorial graphic, not a fabricated application screenshot.

## Visual verification — October 29, 2026

Checked the redesigned page at 320, 390, 768, 900, 1024, 1280 and 1440px without horizontal document overflow. Exercised feature-tab keys, mobile menu Enter/Escape/focus return, native FAQ disclosure and Copy email success feedback. Support checked at phone width and privacy at desktop width. Static references and generated fingerprints checked. See `docs/landing-page-fixes/2026-10-29/README.md` in the private repository for evidence and limitations. This redesign has not been published.
