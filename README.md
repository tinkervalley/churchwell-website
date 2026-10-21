# Churchwell public website

Buildless HTML/CSS/JavaScript, published to `tinkervalley/churchwell-website` using branch-based GitHub Pages (`main`, `/`). No GitHub Actions workflow is required or enabled by this source.

- Website: https://churchwell.ca
- App: https://app.churchwell.ca
- Privacy: https://churchwell.ca/privacy
- Support: https://churchwell.ca/support
- Contact/invites: hello@churchwell.ca

Both website and app domains returned HTTPS 200 on October 21, 2026. The website's sign-in links now use the verified app domain. This does not remove the old app domain or rewrite existing public-form links.

Preview: `python3 -m http.server 5174 --directory site` from the application repository. The support/privacy paths are directories with index files so direct links work on GitHub Pages.

## Screenshots

`assets/screenshots/` contains actual captures of the current SwiftUI app in the iPhone 14 Plus simulator and the running web interface, captured October 21, 2026. These use fictional sample people and event data, not private church records. No synthetic product UI or generated replacement screenshot is used. The desktop captures retain the sample-data preview notice. Rounded device frames are CSS surrounding the original image.

Web captures use the existing `VITE_DEMO_MODE=true` local preview. Native captures use a separately installed simulator bundle with empty Supabase configuration and existing debug section-preview routing; fixture event dates are moved forward in that temporary app bundle. The live app's session, data and backend are untouched. The debug-only section preview also runs after initial layout so child view initialization cannot reset the requested section. Original screenshots are unretouched PNGs.

## Pricing and copy

Planned starting price: CAD $40/month after beta; invited churches test free. No website billing or automatic conversion is implemented. Dedicated branded apps are arranged separately. Competitor sources and date are visible beside the comparison. Breeze currently lists US$72/month, and Planning Center has free core tools plus usage-priced products; no misleading combined total is used.

App Store copy and remaining submission requirements are in `docs/app-store/` in the private application repository. Do not publish private credentials, source files outside `site/`, or review-account secrets to this public repository.
