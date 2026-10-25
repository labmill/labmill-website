# labmill-website

The public website of Labmill, https://labmill.org.

- `index.html`: the home page.
- `bot/index.html`: the page about LabmillBot, the crawler, with its contact address and the `robots.txt` opt-out.
- `assets/`: `site.css`, the mark `mark.svg` and the self-hosted fonts (Bricolage Grotesque, IBM Plex Mono; SIL Open Font License, files in `assets/fonts/`). The site loads nothing from other hosts, so it works when the app server is down.
- The status line on the home page shows when `app.labmill.org` does not answer (`no-cors` request, 4 s timeout; no CORS change needed).
- Add the Docs links back when `docs.labmill.org` exists.

Today the site is served from the Labmill server (static-web-server behind Traefik, files in `/opt/labmill-web/public`). It is planned to move to GitHub Pages (`gh-pages`) later; it is not on GitHub yet.

To publish a change on the server: copy the files to `/opt/labmill-web/public/` on the server. The web container reads them directly.
