# HIG Link Page

GitHub is the source of truth for the live Hunter's Intuitive Guidance link page served at:

- https://hig.tinythor.cc/
- https://links.hunterscf.workers.dev/

## Production source

- `index.html` is the live public page.
- `wrangler.jsonc` targets the existing Cloudflare Worker named `links`.
- `.assetsignore` keeps repository-only files out of the public static deployment.
- `.github/workflows/deploy-hig.yml` deploys changes from `main` to Cloudflare and smoke-tests the live page.

## Safety

The pre-migration state is preserved on the rollback branch:

`backup/before-github-deploy-2026-09-19`

Do not commit passwords, Cloudflare API tokens, private recovery files, or other credentials to this repository. Deployment credentials belong in GitHub Actions secrets/variables only.

## Future link editor

The current page remains visually unchanged. A future authenticated editor can move the button/link data into structured storage (for example Cloudflare D1) while keeping this repository as the source of truth for the public design and application code.
