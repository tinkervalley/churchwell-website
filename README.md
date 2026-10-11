# Churchwell landing page

Buildless HTML/CSS/JavaScript. Publish these files at the root of the `tinkervalley/churchwell-website` repository. GitHub Pages serves `main` `/` without a custom Actions workflow.

- Website: `https://churchwell.ca` (set as the Pages custom domain after domain ownership/DNS is confirmed)
- App: `https://app.churchwell.ca` (Cloudflare Worker custom domain)
- Invite requests: `hello@churchwell.ca`

Interface artwork is illustrative sample content, not private church data. The page does not collect or store visitor submissions. Invite links open the visitor's email client.

For local preview: `python3 -m http.server 5174 --directory site` from the platform repository.

Sign-in links currently use the working `https://churchwell.tinkervalley.ca` address until `app.churchwell.ca` is connected. Then replace both `data-app-link` targets.

## Domain setup

After confirming ownership of churchwell.ca:
1. Configure GitHub Pages custom domain `churchwell.ca` and commit a `CNAME` file containing that hostname.
2. At the DNS provider, add apex A records to 185.199.108.153, 185.199.109.153, 185.199.110.153 and 185.199.111.153. Add `www` CNAME to `tinkervalley.github.io`. Leave these DNS-only while GitHub provisions HTTPS, then enable Enforce HTTPS in Pages.
3. In Cloudflare → Workers & Pages → churchwell → Settings → Domains & Routes, add custom domain `app.churchwell.ca`. Cloudflare must manage the domain’s zone; it provisions the DNS record and certificate. Keep the existing app hostname available.
4. Update the landing page sign-in links and iOS CHURCHWELL_WEB_URL after the new app hostname works. Retain old form URLs; do not redirect them until the new route is verified.

No registration, nameserver, email/MX, or live DNS changes have been made by this source configuration.
