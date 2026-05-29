# JXC Website

Public one-page website for JXC.

Live site: https://jxc.global/

## Stack

- Astro static site
- GitHub Pages hosting
- GitHub Actions deploys from `main`
- Custom domain: `jxc.global`

## Local Development

Install dependencies:

```bash
npm ci
```

Start the local dev server:

```bash
npm run dev
```

Build the production site:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## Project Structure

- `src/pages/index.astro` - homepage content, layout, and styles
- `public/favicon.svg` - site favicon
- `public/CNAME` - GitHub Pages custom domain
- `.github/workflows/deploy.yml` - build and deploy workflow

## Deployment

Every push to `main` runs the GitHub Actions workflow:

1. Install dependencies with `npm ci`
2. Build the static site with `npm run build`
3. Upload `dist/` as a GitHub Pages artifact
4. Deploy to GitHub Pages

Manual deploys can also be started from the `Deploy website` workflow in GitHub Actions.

## Domain And HTTPS

GitHub Pages is configured for:

- Apex domain: `jxc.global`
- HTTPS enforcement: enabled

DNS records for the apex domain should point to GitHub Pages:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

The `www` host should point at:

```text
jxc-global.github.io
```

## Repository Access

This repository is public because the current GitHub plan does not support GitHub Pages from private repositories.

Public visibility means anyone can read or fork the source. It does not grant write access. Only users with write/admin permissions on `jxc-global/website` can push changes or modify the live site.
