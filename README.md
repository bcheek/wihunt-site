# WiHunt website

Static site for GitHub Pages: a landing page, the privacy policy and a support page. No build step,
no JavaScript, no tracking.

| File | URL path | Used for |
| --- | --- | --- |
| `index.html` | `/` | Landing page; marketing URL in App Store Connect |
| `privacy.html` | `/privacy.html` | Privacy policy URL in App Store Connect and Play Console |
| `support.html` | `/support.html` | Support URL in App Store Connect |
| `404.html` | any missing page | GitHub Pages' not-found page |

## Preview locally

```bash
python3 -m http.server 8123 --directory site
```

Then open http://localhost:8123.

## Publish on GitHub Pages

1. Create a new **public** repository, for example `wihunt-site`. (Pages on a private repository needs a paid plan.)
2. Copy everything in this folder, including the hidden `.nojekyll` file, to the root of that repository and push it.
3. In the repository, open Settings › Pages, set Source to "Deploy from a branch", branch `main`, folder `/ (root)`.
4. After a minute the site is at `https://<your-username>.github.io/wihunt-site/`. The privacy policy is
   `…/wihunt-site/privacy.html`. Use those URLs in App Store Connect and Play Console.

Optional: a custom domain (for example `wihunt.app`) under Settings › Pages › Custom domain, with
"Enforce HTTPS" on.

## Keeping it current

- The privacy policy text matches the "WiHunt Privacy Policy" doc. Change both together, and update the
  "Last updated" date in `privacy.html`.
- At launch, replace the two "Coming soon" boxes in `index.html` with the official App Store and Google Play
  badges and store links (Apple and Google each publish badge artwork and usage rules).
- Each January, update the © year in the footers.
