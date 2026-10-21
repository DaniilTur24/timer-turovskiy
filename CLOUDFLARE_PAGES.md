# Cloudflare Pages deployment

This repository is a static website. It does not need a server in production.

## Cloudflare Pages settings

- Production branch: `main`
- Build command: `exit 0`
- Build output directory: `.`

## Custom domain

Attach `timer.turovskiy.dev` in **Workers & Pages → timer-turovskiy → Custom domains**. The domain is already served through Cloudflare, so activate it in Pages before replacing its existing DNS origin.

## Cutover checklist

1. Create the Pages project from this GitHub repository and check the generated `pages.dev` URL.
2. Confirm the timer runs, audio/export controls work, and the background image loads.
3. Attach the custom domain in Pages and wait for it to become active.
4. Verify HTTPS and the timer on the custom domain.
5. Only then remove the Railway custom domain and retire its service.

Git-connected Pages builds a preview for pull requests and deploys `main` to production.
