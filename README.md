# HIG Link Page Backup

Backup repository for the Cloudflare Workers & Pages project `links` serving:

- https://hig.tinythor.cc/
- https://links.hunterscf.workers.dev/

The live page is Hunter's Intuitive Guidance profile/link page.

## Backup method

The GitHub Actions workflow in this repository fetches the currently deployed HTML directly from `https://hig.tinythor.cc/` and saves it as `index.html`.

This keeps the GitHub backup separate from the Google Drive source-of-truth copy and does not modify the live Cloudflare deployment.

Backup established: 2026-09-19.
