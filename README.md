# CaliMaxx website

Plain HTML and CSS. No package installation, build step, analytics, form
backend, or external font service. All runtime assets are local.

Live site: https://dipanshu08seh.github.io/calimaxx-site/
Public repository: https://github.com/dipanshu08seh/calimaxx-site

## Editing and preview

Edit the HTML pages and `assets/styles.css` in this folder. The shared CSS
palette follows the native app's `CMColor`; its spacing grid follows
`CMLayout`. Header and footer markup are repeated in each HTML document and
should stay consistent.

From the parent app repository, preview with:

```sh
python3 -m http.server 4173 --directory Website --bind 127.0.0.1
```

Open http://127.0.0.1:4173/. The 404 page uses the deployed `/calimaxx-site/`
prefix because GitHub can display it at arbitrarily nested missing URLs.
Check it under that prefix or on the deployed site.

The screenshot PNGs and full-size app icon are copies of the original app
assets. Favicon and touch-icon sizes are derived from that same icon. No
generated screenshot UI is used in the website.

## Publishing updates

Clone `dipanshu08seh/calimaxx-site` into a separate checkout and copy the
contents of this folder into its root. Review that checkout's diff, commit
only website files, and push to `main`. GitHub Pages republishes automatically.
Do not change the private app repository's remote, push its history to the
public repository, or include unrelated app files.

Pages settings: deploy from branch `main`, directory `/`, HTTPS enforced.
Keep `.nojekyll`. No custom domain or DNS configuration is required.

All normal page links and assets are relative, so they work under the
project URL. Canonical, social-preview, sitemap, and 404 URLs intentionally
include the complete public URL or `/calimaxx-site/` prefix.

## Launch wording and legal changes

Once the app listing is available, remove “Launching soon · ” from the
landing page's status line and update the launch wording in its meta tags.
The App Store button already uses app ID `6816110786`.

Update the policy date and sitemap dates when legal text changes. Its
initial effective date is October 5, 2026. Review legal text whenever data
handling, providers, intended age range, or subscription behavior changes.

Remaining dashboard setup and the HealthKit/iCloud launch finding are
documented in the app repository's `docs/WEBSITE_LAUNCH.md`.
