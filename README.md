# olyra-landing

Simple landing page served at every olyra-themed outreach domain. Single source of truth; deployed via Cloudflare Pages, attached to all olyra domains as custom domains.

## Why this exists

When a prospect receives cold email from `ana@workwitholyra.com` (or any other olyra sending domain) and types the URL into their browser, this is what they land on. Without something at the domain, deliverability and reply rate take a measurable hit.

## What's served

A single `index.html` with:

- Olyra branding
- Two-sentence value prop
- Primary CTA to [olyra.ai](https://olyra.ai)
- Contact email link

No nav, no footer crap, no tracking scripts. Pure trust signal.

## How it's deployed

1. Push changes to `main` of this repo.
2. Cloudflare Pages auto-builds and deploys to `<project>.pages.dev`.
3. Custom domain CNAMEs route every olyra outreach domain (workwitholyra.com, getolyra.com, etc.) through that Pages project.

## Adding a new sending domain

When a new olyra sending domain comes online for outreach:

1. Add the domain as a custom domain on the Cloudflare Pages project.
2. Cloudflare provisions SSL automatically.
3. Verify the domain serves this page over HTTPS.

## Maintenance

Update copy or styling in `index.html` and push. That's it. One file, everywhere.
