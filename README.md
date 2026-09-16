# ADHD Bornholm — Website Renovation

Rebuild of the website for ADHD Bornholm, the local Bornholm chapter of ADHD-foreningen (the Danish national ADHD association, adhd.dk).

## Status

The live site (adhd-bornholm.dk) is currently a placeholder with no real content. `site/` contains a from-scratch static rebuild, styled to resemble the parent organization's site at adhd.dk. Deployment is manual: copy the contents of `site/` into the `public_html` folder over FTP when ready — no build step required.

## Scope

- Full rebuild, styled as a subsidiary of adhd.dk, using the real ADHD-foreningen brand colors sampled from the provided logos: charcoal `#292929`, cream `#FFFCFA`, plum `#4C303F`. Header uses the official combined lockup (`site/assets/logo-lokal-afd-bornholm.jpg`) — the earlier hand-built logo-image + text combo was replaced with this on 2026-09-16.
- Plain static HTML/CSS — no framework, no build step — so it can be uploaded directly over FTP.
- Content sourced from ADHD-foreningen's existing public page for the Bornholm chapter (adhd.dk/lokalafdelinger/bornholm): activities, board members, contact details. See "Content source" below.
- Deploy target: Simply.com FTP hosting the user already has access to (see legacy-site/ note below) — user uploads manually once happy with the result; this repo does not push to FTP automatically.

## Content source

Pulled from ADHD-foreningen's public Bornholm chapter page (https://adhd.dk/lokalafdelinger/bornholm) on 2026-09-16:

- **Activities**: ADHD Café 18+ (2nd Tuesday/month, 16-18, Østerlars Multihus), ADHD UNGE+ (16-30 y/o, 2nd Friday/month, 19-21), ADHD Familie+ (family network café, one Saturday/month, 13-15)
- **Board**: Selina Munch-Petersen (formand), Sophie Bidstrup Ring (næstformand), Marianne Frølich (kasserer), Cecilie Ramstedt Frølich (bestyrelsesmedlem), Julie Zeltner (bestyrelsesmedlem). Updated 2026-09-16 per user — this now differs from adhd.dk's own chapter page, which as of the scrape date still listed Cecilie as næstformand, Sophie as bestyrelsesmedlem, no Julie, and Ralf Marcoux Skovgaard as a board member. Board photos (Selina, Sophie, Marianne, Cecilie) pulled from adhd.dk/lokalafdeling/bornholm/ into `site/assets/board/`; Julie's photo was provided directly by the user (2026-09-16). All five board members now have photos.
- **Contact**: bornholm@adhd.dk, 61 45 09 02, Ølenevej 22, 3751 Østermarie
- **Meeting location**: Østerlars Multihus, Stavsdalvej 30, 3760 Gudhjem
- **Social**: Facebook group (facebook.com/groups/350894474982), Instagram @adhdbornholm

Contact details and content confirmed accurate by the user on 2026-09-16.

## Site structure

Follows a written content brief from ADHD-foreningen for chapter sites (photographed and provided by the user on 2026-09-16), which specifies this IA:

- **Forside** — intro (who we are, area covered, who it's for) + buttons to Lokale tilbud / Kontakt / Bliv medlem
- **Lokale tilbud** (`lokale-tilbud.html`, was `aktiviteter.html`) — per-group: name, audience, description, place/frequency, signup, price, status
- **Om os** (`om-os.html`) — board members (name/role/avatar) + chapter mission/volunteering
- **Arrangementer** (`arrangementer.html`, new) — upcoming one-off events with signup links, plus a "fra tidligere arrangementer" photo section
- **Medlem** (`medlem.html`, new) — membership benefits, QR code + link to adhd.dk/bliv-medlem/, links to rådgivning and nyhedsbrev, explicit note that membership is administered by ADHD-foreningen, not the local chapter
- **Kontakt** (`kontakt.html`) — email/phone/social/response time + link to the official adhd.dk chapter page

## Assumptions that need verification before going live

- **Lokale tilbud pricing/signup**: marked all three activities as "Gratis" / "Ikke nødvendig — mød bare op" — this wasn't explicitly confirmed, just inferred from how these community cafés are typically run. Please confirm or correct per activity.
- **Board bios**: the content brief also asks for a 2-4 line personal bio per board member. I don't have that yet (photos are now in place for all five) — noted as "coming soon" rather than inventing biographical text about real people.
- **Arrangementer**: has the September 2026 newsletter's three events, split by date relative to "today" (2026-09-16) — Netværkscafé 18+ (Sept 8) and ADHD UNGE+ (Sept 11) are in "Fra tidligere arrangementer" as brief recaps (no signup links/buttons, since those events already happened), while Tur til Nature Park (Sept 19, still upcoming, poster at `site/assets/events/2026-09-19.jpg`) stays in "Kommende arrangementer". This is still example content, not launch-ready — before publishing, replace with whatever month's newsletter is actually current. No past-event photos yet.
- **Kontakt "svartid"**: the brief asks for an approximate response time; I used a generic "we reply when we can, we're volunteers" line rather than inventing a number of days.
- **Medlem page QR code**: generated via a third-party QR image API (api.qrserver.com) embedded as a plain `<img>` — no JS/library, but it does mean that image depends on an external service being up when the live page loads. The QR is always paired with a normal clickable link per the brief's own guidance.

## Open decisions

- [ ] Who maintains the site long-term / whether a CMS is worth adding later
- [ ] Hosting target for adhd-bornholm.dk — the FTP account provided only serves Simply.com's default splash page (see legacy-site/ note); it's unclear if this FTP account is actually where the live domain's DNS points

## Findings

- The FTP account (Simply.com hosting) contains only the default provider splash page in both `public_html` and `testing` — no real site files, empty `.htaccess`. This does **not** match the live placeholder page shown at adhd-bornholm.dk, so it's unconfirmed whether this FTP account is the actual deployment target for the live domain. Worth confirming before the user uploads the finished site.

## Notes

See `AGENTS.md` for working conventions on this project.
