# ADHD Bornholm — Website Renovation

Rebuild of the website for ADHD Bornholm, the local Bornholm chapter of ADHD-foreningen (the Danish national ADHD association, adhd.dk).

## Status

The live site (adhd-bornholm.dk) is currently a placeholder with no real content. `site/` contains a from-scratch static rebuild, styled to resemble the parent organization's site at adhd.dk. Deployment is manual: copy the contents of `site/` into the `public_html` folder over FTP when ready — no build step required.

## Scope

- Full rebuild, styled as a subsidiary of adhd.dk (green/white palette, similar structure).
- Plain static HTML/CSS — no framework, no build step — so it can be uploaded directly over FTP.
- Content sourced from ADHD-foreningen's existing public page for the Bornholm chapter (adhd.dk/lokalafdelinger/bornholm): activities, board members, contact details. See "Content source" below.
- Deploy target: Simply.com FTP hosting the user already has access to (see legacy-site/ note below) — user uploads manually once happy with the result; this repo does not push to FTP automatically.

## Content source

Pulled from ADHD-foreningen's public Bornholm chapter page (https://adhd.dk/lokalafdelinger/bornholm) on 2026-09-16:

- **Activities**: ADHD Café 18+ (2nd Tuesday/month, 16-18, Østerlars Multihus), ADHD UNGE+ (16-30 y/o, 2nd Friday/month, 19-21), ADHD Familie+ (family network café, one Saturday/month, 13-15)
- **Board**: Selina Munch-Petersen (formand), Cecilie Ramstedt Frølich (næstformand), Marianne Frølich (kasserer), Sophie Bidstrup Ring, Ralf Marcoux Skovgaard
- **Contact**: bornholm@adhd.dk, 61 45 09 02, Ølenevej 22, 3751 Østermarie
- **Meeting location**: Østerlars Multihus, Stavsdalvej 30, 3760 Gudhjem
- **Social**: Instagram @adhdbornholm (Facebook group mentioned on adhd.dk but no confirmed URL found — left off the site rather than guessing)

This should be verified/updated with ADHD Bornholm directly before going live — it was scraped from the parent org's site, not provided first-hand.

## Open decisions

- [ ] Real logo/visual identity — site currently uses a text wordmark + adhd.dk-style green palette, no actual logo asset
- [ ] Confirm/replace Facebook link (couldn't verify a real URL)
- [ ] Who maintains the site long-term / whether a CMS is worth adding later
- [ ] Confirm content above is accurate and current with ADHD Bornholm directly
- [ ] Hosting target for adhd-bornholm.dk — the FTP account provided only serves Simply.com's default splash page (see legacy-site/ note); it's unclear if this FTP account is actually where the live domain's DNS points

## Findings

- The FTP account (Simply.com hosting) contains only the default provider splash page in both `public_html` and `testing` — no real site files, empty `.htaccess`. This does **not** match the live placeholder page shown at adhd-bornholm.dk, so it's unconfirmed whether this FTP account is the actual deployment target for the live domain. Worth confirming before the user uploads the finished site.

## Notes

See `AGENTS.md` for working conventions on this project.
