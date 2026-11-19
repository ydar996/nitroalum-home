# NitroAlum Marketing Site (nitroalum-home)

Detached, static SEO and marketing site for NitroAlum. Plain HTML/CSS,
no build step, hosted on GitHub Pages at `https://www.nitroalum.com`.

This site is intentionally separate from the application. It shares no
code, no backend, and no deployment pipeline with the app.

## Structure

| File | Purpose |
|---|---|
| `index.html` | Home: pitch, feature highlights, calls to action |
| `features.html` | Full feature catalogue by module |
| `get-started.html` | How a group onboards and how members join |
| `about.html` | Mission, principles, and the Work Chop attribution |
| `styles.css` | Shared Nitro theme styles |
| `brand/` | NitroAlum mark and lockup |
| `fonts/` | Self hosted Plus Jakarta Sans |
| `sitemap.xml` | Every public page - update on any add/rename |
| `robots.txt` | Allows all, points at the sitemap |
| `CNAME` | `www.nitroalum.com` - DO NOT DELETE |
| `dev-handoff-9x4k.html` | Noindexed developer handoff page |
| `readme-9x4k.html` | Noindexed readme rendered in a browser |

## The App Links Contract

These links appear on every page (nav and footer) and must keep working.
They are the bridge from marketing into the application:

- Find Your Group: `https://nitroalum.com/` (the app front door, group lookup)
- Create Your Group: `https://nitroalum.com/sign-up`
- Members sign in at their own group address, reached via Find Your Group.

Never point these at `www.`; the app lives on the apex domain.

## SEO Requirements

- Every page needs a unique `<title>` and `<meta name="description">`.
- Keep the canonical link, Open Graph tags, and exactly one `<h1>` per page.
- Update `sitemap.xml` whenever a page is added, renamed, or removed.
- The JSON-LD `SoftwareApplication` block on `index.html` stays; update it,
  do not delete it.
- `dev-handoff-9x4k.html` and `readme-9x4k.html` stay `noindex,nofollow`
  and are never linked from public pages or the sitemap.

## Copy Rules

- No em dashes or en dashes anywhere in copy.
- Headers, buttons, and short labels use Title Case; words of three
  letters or fewer stay lowercase mid title except the first word and
  words after separators.
- Plain language; no made up group or company names in copy.

## DNS and Hosting

- Host: GitHub Pages, deployed from `main` root on every push.
- `www.nitroalum.com` is a `CNAME` to `ydar996.github.io`.
- The app apex (`nitroalum.com`) stays on the application server; the
  marketing site does not redirect or proxy it.

## Local Preview

Open `index.html` directly in a browser, or run
`python -m http.server` in this folder and visit `http://localhost:8000`.
