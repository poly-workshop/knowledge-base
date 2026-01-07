# Website

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

## Installation

```bash
pnpm
```

## Local Development

```bash
pnpm start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

## Build

```bash
pnpm build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

## Deployment

### GitHub Pages (via GitHub Actions)

1. In GitHub repo settings: `Settings` → `Pages` → `Build and deployment` → select **GitHub Actions**.
2. Ensure your default branch is `main` (or update `.github/workflows/deploy-github-pages.yml` to match).
3. If your repo is not `poly-workshop/knowledge-base`, update `SITE_URL` / `BASE_URL` in the workflow, or set them via environment variables and adjust `docusaurus.config.ts`.

Using SSH:

```bash
USE_SSH=true pnpm deploy
```

Not using SSH:

```bash
GIT_USER=<Your GitHub username> pnpm deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.
