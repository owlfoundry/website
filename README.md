# OwlFoundry Website

The public website for [OwlFoundry](https://github.com/owlfoundry), built with Astro and deployed on Cloudflare Workers.

## Development

Requirements:

- Node.js 22.12 or newer
- pnpm 11.17.0

```bash
pnpm install
pnpm dev
```

## Quality checks

```bash
pnpm run audit
pnpm check
pnpm build
```

[Lefthook](https://github.com/evilmartians/lefthook) installs Git hooks during dependency installation. Commits run the quality suite, and pushes run a production build.

## Deployment

Pushes to `main` are checked, built, and deployed by GitHub Actions. The repository must provide these Actions secrets:

- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_ACCOUNT_ID`

The workflow intentionally uses repository-level secrets and does not select a GitHub Environment. The `owlfoundry.org` custom domain is managed separately in the Cloudflare dashboard, so Wrangler does not declare a route.

The production sitemap is available at <https://owlfoundry.org/sitemap-index.xml>.

To deploy manually:

```bash
pnpm build
pnpm deploy
```
