# Owner Guide - NitroAlum Marketing Site

Day to day care of the marketing site. No developer needed for edits.

## What Lives Where

| Thing | Location |
|---|---|
| The site files | This GitHub repo `ydar996/nitroalum-home` |
| The live address | `https://www.nitroalum.com` |
| The app | `https://nitroalum.com` (completely separate) |
| The domain DNS | DigitalOcean, `www` CNAME to `ydar996.github.io` |

## Routine Tasks

### Edit a Page

1. Open the file on github.com, click the pencil, make the change,
   commit to `main`.
2. GitHub Pages republishes within about a minute.
3. Check the page on `https://www.nitroalum.com` and the copy rules below.

### Add a New Page

1. Copy an existing page so the header, footer, meta block, and fonts
   come along.
2. Give it a unique `<title>`, meta description, canonical URL, and one
   `<h1>`.
3. Add it to `sitemap.xml` and to the nav and footer on every page.

### Give Someone Edit Access

Repo Settings, Collaborators, add their GitHub username. They get this
repo only: never the app repo or the server.

## Things That Must Not Break

- `CNAME` file: deleting it disconnects `www.nitroalum.com`.
- The app links: every page keeps working links to
  `https://nitroalum.com/` (Find Your Group) and
  `https://nitroalum.com/sign-up` (Create Your Group).
- `sitemap.xml`: every public page is listed; handoff pages are not.
- `dev-handoff-9x4k.html` and `readme-9x4k.html`: stay unlinked and
  `noindex`; share them by URL only.
- Copy rules: no em or en dashes; Title Case headers with the three
  letter rule; plain language.

## If the Site Goes Down

- Check GitHub Pages status on the repo Settings, Pages tab.
- Check the `www` DNS record still points at `ydar996.github.io`.
- The app at `nitroalum.com` is independent; it is unaffected either way.
