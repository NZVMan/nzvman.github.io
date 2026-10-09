# Apps by Vaughan Mitchell: support site

Support pages and privacy policies for my iPhone apps, published with GitHub Pages at
**https://nzvman.github.io/**.

Plain HTML with one shared stylesheet (`assets/site.css`), so there's nothing to build or install.

| App | Support URL | Privacy Policy URL |
|---|---|---|
| AstroTonight | https://nzvman.github.io/astrotonight/ | https://nzvman.github.io/astrotonight/privacy.html |
| Ownsmart | https://nzvman.github.io/ownsmart/ | https://nzvman.github.io/ownsmart/privacy.html |

Paste these into App Store Connect: **Support URL** on the app version page, and **Privacy Policy URL**
under App Privacy.

## Adding a new app

1. Copy the `_template` folder and rename the copy to the app's name in lowercase with no spaces,
   e.g. `mynewapp`. That becomes its web address: `https://nzvman.github.io/mynewapp/`.
2. Add the app icon as `icon.png` in that folder (256 × 256 is plenty), e.g.
   `sips -Z 256 path/to/AppIcon.png --out mynewapp/icon.png`.
3. In the copy's `index.html` and `privacy.html`, replace every `APP NAME`, `TAGLINE` and `TODO`.
4. **Check the privacy policy against what the app really does.** The template assumes the app
   collects nothing. If the new app uses the internet, accounts, iCloud sync, analytics, ads or
   purchases, the policy must say so, and must match your App Privacy answers in App Store Connect.
5. On the home page (`index.html`), copy the AstroTonight `<li class="app">…</li>` block and change it
   for the new app.
6. Add a row to the table above, then commit and push:
   ```
   git add -A
   git commit -m "Add MyNewApp"
   git push
   ```
   The site updates about a minute later.

`_template` and this README are not published (GitHub Pages skips folders starting with `_`, and
`_config.yml` excludes the README).
