# ADHD Bornholm — Website Renovation

Rebuild of the website for ADHD Bornholm, a local ADHD advocacy/support organization on Bornholm, Denmark (adhd-bornholm.dk).

## Status

The live site is currently a placeholder ("Her kommer ADHD Bornholms hjemmeside") with only a home link and a GDPR cookie banner — no real content. This project is a full rebuild, not a restyle.

## Scope

- Full rebuild: information architecture, content, and design from scratch.
- Tech stack: not yet decided.
- Content: not yet gathered — needs input from ADHD Bornholm (who they are, services/activities, contact info, meeting times, board/contacts, membership info, etc.)
- Hosting/domain: adhd-bornholm.dk — current registrar/host unknown.

## Open decisions

- [ ] Tech stack (candidates: Next.js, matching the Thomas Sørensen clinic site stack; or a simpler static site given likely modest hosting/budget/maintenance needs)
- [ ] Who maintains the site long-term (affects CMS vs. static choice)
- [ ] Content source — real copy, org info, contact details, imagery
- [ ] Hosting target and deployment approach
- [ ] Visual identity / branding (logo, colors) — does one exist already?

## Findings

- The FTP account (Simply.com hosting) contains only the default provider splash page in both `public_html` and `testing` — no real site files, empty `.htaccess`. This does **not** match the live placeholder page shown at adhd-bornholm.dk ("Her kommer ADHD Bornholms hjemmeside" + cookie banner), so the live content is coming from somewhere else — different DNS target, a separate site-builder/CMS, or a different hosting account. Needs clarifying with whoever manages the domain/hosting before assuming FTP is the deployment path for the rebuild.

## Notes

See `AGENTS.md` for working conventions on this project.
