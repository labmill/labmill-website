# labmill-website

The public website of Labmill, https://labmill.org.

- `index.html`: the home page.
- `bot/index.html`: the page about LabmillBot, the crawler, with its contact address and the `robots.txt` opt-out.

Today the site is served from the Labmill server (static-web-server behind Traefik, files in `/opt/labmill-web/public`). It is planned to move to GitHub Pages (`gh-pages`) later; it is not on GitHub yet.

To publish a change on the server: copy the files to `/opt/labmill-web/public/` on the server. The web container reads them directly.
