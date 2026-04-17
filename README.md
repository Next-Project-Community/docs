# Next Project Community Docs

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

## Installation

```bash
npm install
```

## Local Development

```bash
npm start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

## Build

```bash
npm run build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

## Deployment

GitHub Actions deployment is configured in `.github/workflows/deploy-gh-pages.yml`.
Each push to `main` builds the site and publishes the generated `build` output through the official GitHub Pages Actions pipeline.

Before using it, configure GitHub Pages in the repository settings:

1. Open `Settings > Pages`.
2. Set the source to `GitHub Actions`.

Using SSH:

```bash
set USE_SSH=true
npm run deploy
```

Not using SSH:

```bash
set GIT_USER=<Your GitHub username>
npm run deploy
```

If you use the GitHub Actions workflow above, you do not need the manual `npm run deploy` flow.
