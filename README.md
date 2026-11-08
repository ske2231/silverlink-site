# SilverLink — IT Support & Realtor Video Walkthroughs

Marketing site for SilverLink LLC (Oklahoma City, OK): friendly IT support for
small businesses, families, and seniors, plus room-to-room video walkthroughs
for Oklahoma realtors.

- **Framework:** Astro 4 (static output)
- **Hosting:** Vercel — deploys automatically from `main`
- **Canonical domain:** https://silverlinkok.com (www redirects to apex)
- **Contact:** mk@silverlinkok.com · (405) 877-2223

## Develop

```bash
npm install
npm run dev      # local preview
npm run build    # production build -> dist/
```

## Booking form

The `/book/` form posts to FormSubmit (free, no account) which emails
`mk@silverlinkok.com` and redirects to `/thanks/`. On the first real
submission FormSubmit sends an activation email to that inbox — click it once
or form mail stops. To switch providers later, change the `action` in
`src/pages/book.astro`.

## Notes

- `/it-support/` is gone: it 301-redirects to `/` via `vercel.json`. Do not
  re-add the page, the nav link, or the sitemap entry.
- The live site's Nov 2026 IT-focused homepage was rebuilt into this repo on
  2026-11-08 from the live HTML (the repo had gone stale in September).
  The pre-audit state is on branch `backup/pre-audit-2026-11-08`.
- Analytics: no GA4 ID is configured yet. Add the tag in
  `src/layouts/BaseLayout.astro` once a measurement ID exists, and verify the
  site in Google Search Console with the sitemap at `/sitemap.xml`.
- Do not re-add unverified claims: Security+ is in progress (not certified),
  no Google star rating is shown (no verified review count on file), and the
  3J number (405) 221-8900 stays off the homepage while it is dead.
