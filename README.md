# Mizpah Shrine Circus website

Static site for mizpahshrinecircus.com, hosted on GitHub Pages. Built by Creative Tone Media.

- `index.html`: the whole site. Season facts (on-sale date, first show, last show end, Ticketmaster link, promo code) live in the `FACTS` block at the bottom of the script and in the Event JSON-LD in the head. Update both each season. The page picks its season mode from the clock: before `onSale` the ticket buttons already open Ticketmaster (Tony, Nov 18 2026) with a note that tickets go on sale Nov 26, from `onSale` to `showEnd` they link to Ticketmaster, after `showEnd` the page says see you next year. No edit is needed on on-sale day.
- `assets/`: WebP images. Files ending in `-AI` are AI placeholders; replace with real show photos.
- `404.html`, `privacy.html`, `accessibility.html`: companion pages.
- `home.html`, `get-tickets.html`, `attractions.html`, `faqs.html`, `about-us.html`, `contact-us.html`, `2026-circus.html`: redirects from the old Squarespace URLs.
- `robots.txt`, `sitemap.xml`, `og-image.jpg`, `favicon.ico`, `apple-touch-icon.png`, IndexNow key file.

Preview mode (current): `<meta name="robots" content="noindex">`, placeholder tags visible, season-mode panel in the footer. Before cutover: build with `--live` (removes noindex and the panel, hides placeholder tags), add the `CNAME` file, paste the Meta domain-verification tag, swap the Ticketmaster artist link for the 2027 event links, and confirm the promo code.


Nov 18 2026: elephants are off the site for the time being (photos, hero loop shot, share image, icon, wording, elephant rides). It is one commit; `git revert` it to bring them back.
