# ArabDev Patch notes

What changed in each ArabDev release, in Arabic and English, filterable by type of
change (new, improved, fixed, security, developer).

Live at **https://patch.arabdev.site**

## What is here

```
index.html     opens the language the reader last used (Arabic by default)
ar/index.html  the Arabic pages
en/index.html  the English pages
assets/        stylesheet, script and self-hosted fonts
favicon.svg
```

It is a plain static site: HTML, CSS and a little JavaScript, with no build step and no
dependencies. Everything is readable without JavaScript; the script only adds conveniences such as
search, the contents list and the light/dark switch.

## Deploying

On Vercel: **Add New Project** → import this repository → Framework Preset **Other** → no build
command → Output Directory `.` → Deploy. Then add the domain `patch.arabdev.site` under
**Settings → Domains**, and point a CNAME at Vercel in Cloudflare DNS with the proxy set to
**DNS only**.

Any static host works the same way, since the files are served as they are.

## Editing

These pages live in the main ArabDev repository under `patch-notes/`
(<https://github.com/fut0r/Arabdev>), which is where changes should be made; this repository is the
deployed copy. When editing:

- Keep the Arabic and English pages in step. They use the same element ids, so links and the
  language switch land on the same section in both.
- Links to the other ArabDev sites are absolute (`https://arabdev.site/dashboard`,
  `https://wiki.arabdev.site/…`). On `localhost` the script rewrites them to local paths, so
  development never jumps to the live site.

## License

ArabDev is free software under the GNU General Public License v3 or later. See `LICENSE`.
