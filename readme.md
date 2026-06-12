<h1 align="center">
  <br>
  <a href="https://www.jhonboyy.github.io/DINO_GAME/" target="_blank"><img width="636" src="assets/preview.png"></a>
  <br>
  <br>
</h1>

> Remaking the chrome offline dinosaur game

## Development

This project uses [Vite](https://vitejs.dev/) for development and building.

### Commands

- **Install dependencies**: `pnpm install`
- **Start dev server**: `pnpm dev`
- **Build for production**: `pnpm build`
- **Preview build**: `pnpm preview`

## Deployment (Cloudflare Pages)

The project is configured for Cloudflare Pages.

- **Build output directory**: `dist`
- **Build command**: `pnpm build`

## License

[MIT](license)


## 🌍 Deployment & Branching Workflow

This project uses a two-branch workflow integrated with Cloudflare Pages:
*   **`develop`**: For ongoing features, bug fixes, and development. Pushing here automatically deploys to the **Staging/Preview** environment.
*   **`main`**: Production release branch. Pushing here automatically deploys to the **Production** environment.

### Release Workflow (Fast-Forward + Tags)
When ready to release changes from `develop` to production `main`:
1. Switch to `main` and update it:
   ```bash
   git checkout main && git pull origin main
   ```
2. Merge `develop` using fast-forward only:
   ```bash
   git merge develop --ff-only
   ```
3. Push to production `main` (triggers the production build):
   ```bash
   git push origin main
   ```
4. Create and push a tag for the release milestone (e.g., `week-6`):
   ```bash
   git tag -a week-6 -m "Release Week 6"
   git push origin week-6
   ```
5. Return to the `develop` branch to continue working:
   ```bash
   git checkout develop
   ```
