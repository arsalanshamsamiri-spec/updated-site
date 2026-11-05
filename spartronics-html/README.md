# Spartronics website

Plain HTML and CSS. No build step and no JavaScript. Each page is a folder with an `index.html`, and every page links to the one stylesheet, `styles.css`.

```
index.html          Home
about/index.html    About
robots/index.html   Robots and software
history/index.html  Competition history
join/index.html     Join the team
support/index.html  Sponsorship and donations
contact/index.html  Contact
404.html
styles.css
img/                photos (placeholders for now) and the share image
vercel.json         clean URLs and redirects from the old page addresses
```

## Deploying on Vercel

Put these files at the top level of the repo, replacing the old site's files. Delete `build.js`, `package.json`, `src/` and `scripts/` if they're still there. In the Vercel project settings, set Framework Preset to "Other", leave the build command and output directory empty, and leave Root Directory empty.

## Editing

The header and footer are copied into every page. If you change a menu item or the email address, change it in all eight HTML files (find and replace works).

To replace a placeholder photo, put the photo in `img/` and change the `src` in the matching `<img>` tag. Keep the `width` and `height` attributes, setting them to the photo's real size.

## Before launch

Search the HTML for `TODO` to find the places waiting on information:

- **Email address.** `robotics@dlshs.org` is a guess. Replace it everywhere with the team's real address.
- **Meeting day and time** on the Join page.
- **Roster** on the About page. There's a commented-out example to copy.
- **Current code repository** on the Robots page.
- **Sponsor packet, donation link and tax statement** on the Support page and in the footer.
- **Photos** in `img/`.

The site's address is set to `https://robotics-bice.vercel.app` in each page's `<head>` and in `sitemap.xml` and `robots.txt`. Change it there if you move to a custom domain.
